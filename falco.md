Falco 


Bookmark Link:

    https://falco.org/docs/
    https://falco.org/docs/examples/
    https://falco.org/docs/rules/supported-fields/


Points:

1. `/etc/falco/` is the location of falco specific rules. `falco.yaml` has the list of configured rule files. 
2. for adding any new rules, got to the docs examples, copy an example rule and modify it as you see it. example below
```yaml
   - rule: run_shell_in_container
     desc: a shell was spawned by a non-shell program in a container. Container entrypoints are excluded.
     condition: container and proc.name = bash and spawned_process and proc.pname exists and not proc.pname in (bash, docker)
     output: "Shell spawned in a container other than entrypoint (user=%user.name container_id=%container.id container_name=%container.name shell=%proc.name parent=%proc.pname cmdline=%proc.cmdline)"
     priority: WARNING
```
3. Output can be modified with supported fields reference.
4. and restart the falco service once modified. `sudo service falco restart `
