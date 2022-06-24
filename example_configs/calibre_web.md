# Configuration for Calibre-Web

Replace `dc=example,dc=com` with your LLDAP configured domain.


### Login type

```
Use LDAP Authentication
```

### LDAP Server Host Name or IP Address

```
lldap
```

### LDAP Server Port

```
3890
```

### LDAP Encryption

```
none
```

### LDAP Authentication

```
simple
```

### LDAP Administrator Username

```
uid=admin,ou=people,dc=example,dc=com
```

### LDAP Administrator Password

```
CHANGE_ME
```

### LDAP Distinguished Name (DN)

```
dc=example,dc=com
```

### LDAP User Object Filter

```
(&(objectclass=person)(uid=%s))
```

### LDAP Server is OpenLDAP?

```
yes
```

### LDAP Group Object Filter

```
(&(objectclass=groupOfUniqueNames)(cn=%s))
```

### LDAP Group Name

```
calibre_web
```

Note: Create a group in lldap and add users to it that will have access to your Calibre-Web instance

### LDAP Group Members Field

```
uniqueMember
```

### LDAP Member User Filter Detection

```
Custom Filter
```

### LDAP Member User Filter

```
(&(objectclass=person)(uid=%s))
```
Note: lowercase the word "person" until this bug is fixed
