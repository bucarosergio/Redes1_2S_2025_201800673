Diga

sw 6 - 4 - 3
enable
configure terminal
vtp mode client
vtp domain 201800673
vtp password usac2025

se configuran los puertos trunk y los access segun la vlan
enable
configure terminal
interface f0/1 o interface range 0/1-3
switchport mode trunk

o 

enable
configure terminal
interface f0/1 o interface range 0/1-3
switchport mode access
switchport access vlan xx

sw5
enable
configure terminal
vtp mode server
vtp domain 201800673
vtp password usac2025
vlan 10
 name ESTUDIANTES
exit
vlan 20
 name DOCENTES
exit
vlan 30
 name VIGILANCIA
exit
vlan 40
 name ADMIN
exit

ms 2 - 1
modo cliente y sus trunk





enable
configure terminal
vtp mode client
vtp domain 201800673
vtp password usac2025
interface f0/1
switchport mode trunk
exit
exit
show vlan brief
