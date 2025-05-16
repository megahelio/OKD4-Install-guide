[root@odk4-services ~]# oc get machineconfig
NAME                                               GENERATEDBYCONTROLLER                      IGNITIONVERSION   AGE
00-master                                          fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
00-worker                                          fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
01-master-container-runtime                        fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
01-master-kubelet                                  fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
01-worker-container-runtime                        fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
01-worker-kubelet                                  fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
97-master-generated-kubelet                        fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
97-worker-generated-kubelet                        fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
98-master-generated-kubelet                        fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
98-worker-generated-kubelet                        fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
99-master-generated-registries                     fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
99-master-ssh                                                                                 3.2.0             12h
99-worker-generated-registries                     fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
99-worker-ssh                                                                                 3.2.0             12h
rendered-master-45d0805af6c835ef4fae764dbcbc1acb   fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
rendered-worker-c4efe16c34baa6609b5a987ac187d39c   fe6668121f9136881f41d9ae99c02fe37589182e   3.4.0             12h
[root@odk4-services ~]# oc get mcp
NAME     CONFIG                                             UPDATED   UPDATING   DEGRADED   MACHINECOUNT   READYMACHINECOUNT   UPDATEDMACHINECOUNT   DEGRADEDMACHINECOUNT   AGE
master                                                      False     True       False      1              0                   0                     0                      12h
worker   rendered-worker-c4efe16c34baa6609b5a987ac187d39c   False     True       False      1              0                   0                     0                      12h