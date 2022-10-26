## How to use it

### Init role

In the example code bellow we used `my-ansible-role` as directory name and `my_ansible_role` as role name. 
Use your own naming for role name and containing directory. See Ansible document about [Role names](https://galaxy.ansible.com/docs/contributing/creating_role.html#role-names). 

```bash
mkdir my-ansible-role && cd my-ansible-role
curl -L https://github.com/martinboy/ansible-skeleton-role/tarball/master -o master.tar.gz && \
tar -xzf master.tar.gz  --strip-components=1 && \
rm -rf master.tar.gz
```

Rename role names
```bash
find . -type f -exec  sed -i  's/skeleton_role/my_ansible_role/g' {} \; 
find . -type f -exec  sed -i  's/skeleton-role/my-ansible-role/g' {} \; 
```

**Note**: On macOs use [gnu-sed](https://formulae.brew.sh/formula/gnu-sed) vesrion of sed command

### Generate LICENSE file

Use `lice` command line utility as [license generator](https://www.npmjs.com/package/lice). Alternatively, you can generate license file while creating a repository on GitHub.


### Build Role

Build the role functionality into the folder structure, or migrate an existing role into it.

### Write tests
Populate .travis.yml with tests which confirm that your role produces the desired effect on a target system.

### Document role

After the role is complete fill out *meta/main.yml*. The Ansible Galaxy looks for metadata found in this file.

Document role in *role-README.md* file and rename it to *README.md*
```bash
mv role-README.md README.md
```

### Role cleanup

- Delete any empty or unused directories and YAML files
- Make sure that your role files doen't contain skeleton_role