```
{
    "apiVersion": "v1",
    "items": [
        {
            "apiVersion": "certificates.k8s.io/v1",
            "kind": "CertificateSigningRequest",
            "metadata": {
                "creationTimestamp": "2025-05-02T09:39:21Z",
                "generateName": "csr-",
                "name": "csr-c7mw4",
                "resourceVersion": "3179",
                "uid": "f510bc4a-3d97-4e45-a4e5-b369978e65ae"
            },
            "spec": {
                "groups": [
                    "system:nodes",
                    "system:authenticated"
                ],
                "request": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURSBSRVFVRVNULS0tLS0KTUlJQlVUQ0IrQUlCQURCUU1SVXdFd1lEVlFRS0V3eHplWE4wWlcwNmJtOWtaWE14TnpBMUJnTlZCQU1UTG5ONQpjM1JsYlRwdWIyUmxPbTlyWkRRdFkyOXVkSEp2YkMxd2JHRnVaUzB4TG14aFlpNXZhMlF1Ykc5allXd3dXVEFUCkJnY3Foa2pPUFFJQkJnZ3Foa2pPUFFNQkJ3TkNBQVNQa2VHMS8rS2xGbE84N0h5NVFlS3M0ZjBMUSswQ3ZTSmQKRjFCaXBSR0h2TUNaa2w1SHRvODVubU0wRUFuMnFNaENhT0JqdFMwdXErNEcraWNqZnpwa29FWXdSQVlKS29aSQpodmNOQVFrT01UY3dOVEF6QmdOVkhSRUVMREFxZ2lKdmEyUTBMV052Ym5SeWIyd3RjR3hoYm1VdE1TNXNZV0l1CmIydGtMbXh2WTJGc2h3VEFxSEJuTUFvR0NDcUdTTTQ5QkFNQ0EwZ0FNRVVDSVFETGpMNGdRRzRCWmd5cFpZNngKeUVoZFhXdkoxSzBRdlRCUzdLM3dVend1ZXdJZ2R5dlY3ZUozUGdBa1JkYkptUHRLYlpsS24rZUJ1aWN0L2ExRgpHRzIwWHY0PQotLS0tLUVORCBDRVJUSUZJQ0FURSBSRVFVRVNULS0tLS0K",
                "signerName": "kubernetes.io/kubelet-serving",
                "usages": [
                    "digital signature",
                    "server auth"
                ],
                "username": "system:node:okd4-control-plane-1.lab.okd.local"
            },
            "status": {
                "certificate": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUN5akNDQWJLZ0F3SUJBZ0lSQU9HYkNBRitLUDFrWGR3RHVmaWlnS0l3RFFZSktvWklodmNOQVFFTEJRQXcKTFRFU01CQUdBMVVFQ3hNSmIzQmxibk5vYVdaME1SY3dGUVlEVlFRREV3NXJkV0psYkdWMExYTnBaMjVsY2pBZQpGdzB5TlRBMU1ESXdPVE0wTkRCYUZ3MHlOVEExTURNd09URTJNek5hTUZBeEZUQVRCZ05WQkFvVERITjVjM1JsCmJUcHViMlJsY3pFM01EVUdBMVVFQXhNdWMzbHpkR1Z0T201dlpHVTZiMnRrTkMxamIyNTBjbTlzTFhCc1lXNWwKTFRFdWJHRmlMbTlyWkM1c2IyTmhiREJaTUJNR0J5cUdTTTQ5QWdFR0NDcUdTTTQ5QXdFSEEwSUFCSStSNGJYLwo0cVVXVTd6c2ZMbEI0cXpoL1F0RDdRSzlJbDBYVUdLbEVZZTh3Sm1TWGtlMmp6bWVZelFRQ2Zhb3lFSm80R08xCkxTNnI3Z2I2SnlOL09tU2pnWXd3Z1lrd0RnWURWUjBQQVFIL0JBUURBZ2VBTUJNR0ExVWRKUVFNTUFvR0NDc0cKQVFVRkJ3TUJNQXdHQTFVZEV3RUIvd1FDTUFBd0h3WURWUjBqQkJnd0ZvQVU4bSsxR25Cdk5KaWpNSUdYVUtSTQpLVDFEK1Nvd013WURWUjBSQkN3d0tvSWliMnRrTkMxamIyNTBjbTlzTFhCc1lXNWxMVEV1YkdGaUxtOXJaQzVzCmIyTmhiSWNFd0tod1p6QU5CZ2txaGtpRzl3MEJBUXNGQUFPQ0FRRUFadW1wZ25mdXZWaWdkRjNxVmdPeE1JV0gKZ0IyWnM4TTA1anJnV0dOaGhmT2I2Rmw0VmtkdHdmOWxnVmRKbDNVd2h1Yy83STVIT0RzRndQMWxwM1E4NkdnYQp5SjVGbmJYVHdwSTh1Y1NvZ2VEUmVzN1k1VDFQSmhZTkhnV25OYWZURG54UlpRVi9FMjZuU3FOUlp2eW50RU4zCnZKb0RmSWxjWlpaMWNCeWlQaUxxeTY2ZVJGM3Z2TE5wZFEzTTV1VUpBQmtXcWUxcGxKZnhXeU5odmRYM3BmangKaFhrcXZ6Y29xWVBmWFFUNDQzNmV2MnRrRmpuaWpjdkVRazloL28vUFZFZ0xzeVdDSnBDT3FjY0xtM01GTlVCZgpjdUYydUNGaUNEaFN5ZW1aR002aldhREtTWjg4QngrSnRuNDBMamdjejVDMTZYTVVucC9hcHJWdUxvUHQydz09Ci0tLS0tRU5EIENFUlRJRklDQVRFLS0tLS0K",
                "conditions": [
                    {
                        "lastTransitionTime": "2025-05-02T09:39:40Z",
                        "lastUpdateTime": "2025-05-02T09:39:40Z",
                        "message": "This CSR was approved by kubectl certificate approve.",
                        "reason": "KubectlApprove",
                        "status": "True",
                        "type": "Approved"
                    }
                ]
            }
        },
        {
            "apiVersion": "certificates.k8s.io/v1",
            "kind": "CertificateSigningRequest",
            "metadata": {
                "creationTimestamp": "2025-05-02T09:45:51Z",
                "generateName": "csr-",
                "name": "csr-c7v77",
                "resourceVersion": "4946",
                "uid": "e028a880-e45e-4cb8-8b8f-ca023e2e7ed3"
            },
            "spec": {
                "expirationSeconds": 86400,
                "groups": [
                    "system:nodes",
                    "system:authenticated"
                ],
                "request": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURSBSRVFVRVNULS0tLS0KTUlJQkZEQ0J1Z0lCQURCWU1Sa3dGd1lEVlFRS0V4QnplWE4wWlcwNmIzWnVMVzV2WkdWek1Uc3dPUVlEVlFRRApFekp6ZVhOMFpXMDZiM1p1TFc1dlpHVTZiMnRrTkMxamIyNTBjbTlzTFhCc1lXNWxMVEV1YkdGaUxtOXJaQzVzCmIyTmhiREJaTUJNR0J5cUdTTTQ5QWdFR0NDcUdTTTQ5QXdFSEEwSUFCT2pFUS93NjdGNGRFKy9kd1hkVzd5VFgKbDNiMnJiV3FNbWRLbFkvM05TTmxWNXh3Mmk0dXRjSGdCZkpwM3ZnWjhGN0hKbldEUzliM24xNUxiZGdHVzB5ZwpBREFLQmdncWhrak9QUVFEQWdOSkFEQkdBaUVBLzBYekdqcndqR1U5Vjg1SUd1VnBxeWpOQmNCTElvUmt4MVZlCnFQS28xUUlDSVFEV0dPamZNZGloUWo0OW1zaXpRZ2hNbTBqQXFoNkV1cDZKcTF1a3pyL2lIQT09Ci0tLS0tRU5EIENFUlRJRklDQVRFIFJFUVVFU1QtLS0tLQo=",
                "signerName": "kubernetes.io/kube-apiserver-client",
                "usages": [
                    "digital signature",
                    "client auth"
                ],
                "username": "system:node:okd4-control-plane-1.lab.okd.local"
            },
            "status": {
                "certificate": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUNtekNDQVlPZ0F3SUJBZ0lSQU1rbzFCbDJhZEpWMHpJaUJucmRqcmt3RFFZSktvWklodmNOQVFFTEJRQXcKTFRFU01CQUdBMVVFQ3hNSmIzQmxibk5vYVdaME1SY3dGUVlEVlFRREV3NXJkV0psYkdWMExYTnBaMjVsY2pBZQpGdzB5TlRBMU1ESXdPVFF3TlRGYUZ3MHlOVEExTURNd09URTJNek5hTUZneEdUQVhCZ05WQkFvVEVITjVjM1JsCmJUcHZkbTR0Ym05a1pYTXhPekE1QmdOVkJBTVRNbk41YzNSbGJUcHZkbTR0Ym05a1pUcHZhMlEwTFdOdmJuUnkKYjJ3dGNHeGhibVV0TVM1c1lXSXViMnRrTG14dlkyRnNNRmt3RXdZSEtvWkl6ajBDQVFZSUtvWkl6ajBEQVFjRApRZ0FFNk1SRC9EcnNYaDBUNzkzQmQxYnZKTmVYZHZhdHRhb3laMHFWai9jMUkyVlhuSERhTGk2MXdlQUY4bW5lCitCbndYc2NtZFlOTDF2ZWZYa3R0MkFaYlRLTldNRlF3RGdZRFZSMFBBUUgvQkFRREFnZUFNQk1HQTFVZEpRUU0KTUFvR0NDc0dBUVVGQndNQ01Bd0dBMVVkRXdFQi93UUNNQUF3SHdZRFZSMGpCQmd3Rm9BVThtKzFHbkJ2TkppagpNSUdYVUtSTUtUMUQrU293RFFZSktvWklodmNOQVFFTEJRQURnZ0VCQUpPdFJ1dHV1ZEJIZElWVzc5UVJ2Z0llCjJyNnVMa0pyWjNqY1RxMnIxbnQ2cjdaVnl2dTRkQ2FWaW1WR0ovejFiSTZ0REdJb05oYnVkU1g0VGZyY2lQVkgKdUlqM3grWFhDd0ovcEpOaC8vek1YVzhYMGI3QldwZmUrQnVNUmFiNzlhQUUrdWRydDE1YW9KeDVVajM1VThRYwpZdFpKL1dwWmxpTEJIeDB6OTB5QW9GMzB6dS9wUStsblBDNzhwYVVmSjBCYjY3TGVBSUIzOXdFT0NQSWdPeWthCm5obEwxN2l4ZGYwNzhwMmdGVG45OU5ObmJUdmN6T3R6d1RybXR4THhINTRWUlRJUXk4WVVBQWRsaWRzS1VzQTkKUkYzU080blkzeGk2V3dlZUhOeU1YeEdJUnhBeDEwczZ6ZVBMWkc4VUhFMkM0UmEycVRLdHRmM2hOZkFuejNrPQotLS0tLUVORCBDRVJUSUZJQ0FURS0tLS0tCg==",
                "conditions": [
                    {
                        "lastTransitionTime": "2025-05-02T09:45:51Z",
                        "lastUpdateTime": "2025-05-02T09:45:51Z",
                        "message": "Auto-approved CSR \"csr-c7v77\"",
                        "reason": "AutoApproved",
                        "status": "True",
                        "type": "Approved"
                    }
                ]
            }
        },
        {
            "apiVersion": "certificates.k8s.io/v1",
            "kind": "CertificateSigningRequest",
            "metadata": {
                "creationTimestamp": "2025-05-02T09:39:07Z",
                "generateName": "csr-",
                "name": "csr-dxbnz",
                "resourceVersion": "3116",
                "uid": "e99c0953-bae4-4a10-8be8-af52085ee445"
            },
            "spec": {
                "groups": [
                    "system:serviceaccounts",
                    "system:serviceaccounts:openshift-machine-config-operator",
                    "system:authenticated"
                ],
                "request": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURSBSRVFVRVNULS0tLS0KTUlJQkN6Q0JzZ0lCQURCUU1SVXdFd1lEVlFRS0V3eHplWE4wWlcwNmJtOWtaWE14TnpBMUJnTlZCQU1UTG5ONQpjM1JsYlRwdWIyUmxPbTlyWkRRdFkyOXVkSEp2YkMxd2JHRnVaUzB4TG14aFlpNXZhMlF1Ykc5allXd3dXVEFUCkJnY3Foa2pPUFFJQkJnZ3Foa2pPUFFNQkJ3TkNBQVFxbkxSaGFXY0ZvZ29xMHBBeE1SRTRqbXA3SXRPeTNIWmIKUGwyQUM2ZUZLYkxwWFk2VG9uVkorOGR2S3hod0dIWUFFdWdIS3ZQVGVlSCs3dFBUZGJFSW9BQXdDZ1lJS29aSQp6ajBFQXdJRFNBQXdSUUloQUpHNGpucjdKSENhSDhCbHVubmppUmhYSnR0emp2WGlZQmx5NXlaSExBeDRBaUJ5Cm1FR25iTGNUeGpHS2JzUWx0TDFFN1ZZWENtR3YvSDcxamxyNlRleUtEdz09Ci0tLS0tRU5EIENFUlRJRklDQVRFIFJFUVVFU1QtLS0tLQo=",
                "signerName": "kubernetes.io/kube-apiserver-client-kubelet",
                "usages": [
                    "digital signature",
                    "client auth"
                ],
                "username": "system:serviceaccount:openshift-machine-config-operator:node-bootstrapper"
            },
            "status": {
                "certificate": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUNrakNDQVhxZ0F3SUJBZ0lRQjhHYlVtb2pXbjRxQ0V4aU80R29vekFOQmdrcWhraUc5dzBCQVFzRkFEQXQKTVJJd0VBWURWUVFMRXdsdmNHVnVjMmhwWm5ReEZ6QVZCZ05WQkFNVERtdDFZbVZzWlhRdGMybG5ibVZ5TUI0WApEVEkxTURVd01qQTVNelF5TUZvWERUSTFNRFV3TXpBNU1UWXpNMW93VURFVk1CTUdBMVVFQ2hNTWMzbHpkR1Z0Ck9tNXZaR1Z6TVRjd05RWURWUVFERXk1emVYTjBaVzA2Ym05a1pUcHZhMlEwTFdOdmJuUnliMnd0Y0d4aGJtVXQKTVM1c1lXSXViMnRrTG14dlkyRnNNRmt3RXdZSEtvWkl6ajBDQVFZSUtvWkl6ajBEQVFjRFFnQUVLcHkwWVdsbgpCYUlLS3RLUU1URVJPSTVxZXlMVHN0eDJXejVkZ0F1bmhTbXk2VjJPazZKMVNmdkhieXNZY0JoMkFCTG9CeXJ6CjAzbmgvdTdUMDNXeENLTldNRlF3RGdZRFZSMFBBUUgvQkFRREFnZUFNQk1HQTFVZEpRUU1NQW9HQ0NzR0FRVUYKQndNQ01Bd0dBMVVkRXdFQi93UUNNQUF3SHdZRFZSMGpCQmd3Rm9BVThtKzFHbkJ2Tkppak1JR1hVS1JNS1QxRAorU293RFFZSktvWklodmNOQVFFTEJRQURnZ0VCQUM5MTdPUmt0NGYwOTI5UVlIeE84RlV0MFJNWmh5aFdmcDVSCjdxcEpnM2RDR0swVnVXUmU2Z2E1MW8wS1UwRy9PR0pRZlk3a1hWZWtQT1J3bU4xZ0VaNjdUajdENzlRTnNyeGEKaytWM0ZFTFR3YnprbVM3b3BXWE5XVnJYYzJvRks3RVFtMHB2UDRsVkFSSDZjbHl4STU1WkxvMWFNYzc3TjdiUQpaYXFqNmlUT1VwOXNkOVBSWlVSUElMblJBUGZ4Zy9vLzFoN3VRMy95c0dOVWpmdHozYk9LT2l5RmdOeElwL1MvCmo4OXc0SGwvWXhjNy9nMmZmNzVvcHEySTIwQVo5THM3QVBRZHY1UXp2QTZPaVFSRG1XUS9VNThaTWVvaTFQSGQKejE3ODZDYW9QK0dYNDd0K2Q4b3diVnVzOGNVWCtWZi93cVd0cnFLTjdjM1pYdGthVlpjPQotLS0tLUVORCBDRVJUSUZJQ0FURS0tLS0tCg==",
                "conditions": [
                    {
                        "lastTransitionTime": "2025-05-02T09:39:20Z",
                        "lastUpdateTime": "2025-05-02T09:39:20Z",
                        "message": "This CSR was approved by kubectl certificate approve.",
                        "reason": "KubectlApprove",
                        "status": "True",
                        "type": "Approved"
                    }
                ]
            }
        },
        {
            "apiVersion": "certificates.k8s.io/v1",
            "kind": "CertificateSigningRequest",
            "metadata": {
                "creationTimestamp": "2025-05-02T09:45:56Z",
                "generateName": "csr-",
                "name": "csr-ld2rp",
                "resourceVersion": "4970",
                "uid": "1a361f2b-cd21-49f5-8ef2-38ad3a357b27"
            },
            "spec": {
                "expirationSeconds": 86400,
                "groups": [
                    "system:nodes",
                    "system:authenticated"
                ],
                "request": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURSBSRVFVRVNULS0tLS0KTUlJQkRUQ0J0UUlCQURCVE1SWXdGQVlEVlFRS0V3MXplWE4wWlcwNmJYVnNkSFZ6TVRrd053WURWUVFERXpCegplWE4wWlcwNmJYVnNkSFZ6T205clpEUXRZMjl1ZEhKdmJDMXdiR0Z1WlMweExteGhZaTV2YTJRdWJHOWpZV3d3CldUQVRCZ2NxaGtqT1BRSUJCZ2dxaGtqT1BRTUJCd05DQUFRTE1EUEpqYVJnR3JZR1NpUXBuZytndVpGMkM2WWgKbHFyaEpXS2NDNmZ1V1R1UUIyYmNVQWExa0R1bzJTL2VYWUp4bWRpWXdteTNrRjcwVTNXZm9pazNvQUF3Q2dZSQpLb1pJemowRUF3SURSd0F3UkFJZ1hxZFFkaWFZMi9sbXZKRVRSRFVIRWFOb1IramkyeHltN3RSQ3Y0WXFNbjBDCklGL2Nna2tob0xSNTFFVmVTcUk4Zzd1cUJsRE5BbnV0eWx4M1NPRHlWMU42Ci0tLS0tRU5EIENFUlRJRklDQVRFIFJFUVVFU1QtLS0tLQo=",
                "signerName": "kubernetes.io/kube-apiserver-client",
                "usages": [
                    "digital signature",
                    "client auth"
                ],
                "username": "system:node:okd4-control-plane-1.lab.okd.local"
            },
            "status": {
                "certificate": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUNsVENDQVgyZ0F3SUJBZ0lRQ29pK2tDc3hiMmtOa2E4VnpFOURiREFOQmdrcWhraUc5dzBCQVFzRkFEQXQKTVJJd0VBWURWUVFMRXdsdmNHVnVjMmhwWm5ReEZ6QVZCZ05WQkFNVERtdDFZbVZzWlhRdGMybG5ibVZ5TUI0WApEVEkxTURVd01qQTVOREExTmxvWERUSTFNRFV3TXpBNU1UWXpNMW93VXpFV01CUUdBMVVFQ2hNTmMzbHpkR1Z0Ck9tMTFiSFIxY3pFNU1EY0dBMVVFQXhNd2MzbHpkR1Z0T20xMWJIUjFjenB2YTJRMExXTnZiblJ5YjJ3dGNHeGgKYm1VdE1TNXNZV0l1YjJ0a0xteHZZMkZzTUZrd0V3WUhLb1pJemowQ0FRWUlLb1pJemowREFRY0RRZ0FFQ3pBegp5WTJrWUJxMkJrb2tLWjRQb0xtUmRndW1JWmFxNFNWaW5BdW43bGs3a0FkbTNGQUd0WkE3cU5rdjNsMkNjWm5ZCm1NSnN0NUJlOUZOMW42SXBONk5XTUZRd0RnWURWUjBQQVFIL0JBUURBZ2VBTUJNR0ExVWRKUVFNTUFvR0NDc0cKQVFVRkJ3TUNNQXdHQTFVZEV3RUIvd1FDTUFBd0h3WURWUjBqQkJnd0ZvQVU4bSsxR25Cdk5KaWpNSUdYVUtSTQpLVDFEK1Nvd0RRWUpLb1pJaHZjTkFRRUxCUUFEZ2dFQkFNL2Y0N1pEdVF3eTBZSzF2R1BLaWFJZmdjZ0JEZEtZCkMyVFlqVmxMTXlNM0V6YStwME5PMTYxNHE1MmdONFl4WU1KMHE5RmNKSGh2cEFROFEwOHh4Q2szdjY2MGVUczMKY2Y1M1JDbzB3WFhrWndSaDhHSENIVUg1OEFaL2dTVVdkalpFTE9GU2RCaXkzL2NKUUhvVHU4V3NMU0I5RUFYUwo1RkI5bUx2Zkwxd05HNHdqdE14U0IvNkV5VlRRb3VmOXVuOWFqUTlmZWNmbTBieVNYNEwzTTZSaXI1UHJHaCt3CkZDRFRQS2FTNURQbzRnWVdVUWN0ZDlwS2tacFNqWUlTQklmdWRDZFlQclVQTC9pcmZkeGt6WE42VXc5SkVtV0sKQ3VPRER5RUlmS0RDMUx1bmhRSEdOYi96eVJScjRMMlFyYVJqRC9CU0ZOUS9kbkxMbTFlaEZOWT0KLS0tLS1FTkQgQ0VSVElGSUNBVEUtLS0tLQo=",
                "conditions": [
                    {
                        "lastTransitionTime": "2025-05-02T09:45:56Z",
                        "lastUpdateTime": "2025-05-02T09:45:56Z",
                        "message": "Auto-approved CSR \"csr-ld2rp\"",
                        "reason": "AutoApproved",
                        "status": "True",
                        "type": "Approved"
                    }
                ]
            }
        },
        {
            "apiVersion": "certificates.k8s.io/v1",
            "kind": "CertificateSigningRequest",
            "metadata": {
                "creationTimestamp": "2025-05-02T09:39:17Z",
                "generateName": "csr-",
                "name": "csr-q84gw",
                "resourceVersion": "3117",
                "uid": "77864359-186c-4866-8f18-f60db9d6c713"
            },
            "spec": {
                "groups": [
                    "system:serviceaccounts",
                    "system:serviceaccounts:openshift-machine-config-operator",
                    "system:authenticated"
                ],
                "request": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURSBSRVFVRVNULS0tLS0KTUlJQkN6Q0JzZ0lCQURCUU1SVXdFd1lEVlFRS0V3eHplWE4wWlcwNmJtOWtaWE14TnpBMUJnTlZCQU1UTG5ONQpjM1JsYlRwdWIyUmxPbTlyWkRRdFkyOXVkSEp2YkMxd2JHRnVaUzB4TG14aFlpNXZhMlF1Ykc5allXd3dXVEFUCkJnY3Foa2pPUFFJQkJnZ3Foa2pPUFFNQkJ3TkNBQVJIdmQ1anpIRE1kTnJ0WGxOdW9rL21CNmU1N0w2bUxJRWMKL1o5bTRJcFRQZ2RGYk9jbld3U3JmaDFtamF0UkJTazNwQWVJeTBZKzVMVzRJamJRNm5nSW9BQXdDZ1lJS29aSQp6ajBFQXdJRFNBQXdSUUlnREFEZm9Zc29XMDRRcDBCcmMrd0NhYUF0dzlYZFY4MmN3a0VWRWtuc3RMRUNJUURVCjEwRmUrOG5zaGlPL1BGcVlHdXAwL0o0UmlFZmRuZ2drZXJaRFRnSXFaZz09Ci0tLS0tRU5EIENFUlRJRklDQVRFIFJFUVVFU1QtLS0tLQo=",
                "signerName": "kubernetes.io/kube-apiserver-client-kubelet",
                "usages": [
                    "digital signature",
                    "client auth"
                ],
                "username": "system:serviceaccount:openshift-machine-config-operator:node-bootstrapper"
            },
            "status": {
                "certificate": "LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUNrekNDQVh1Z0F3SUJBZ0lSQU1EdmJxV29OYVRjaUthVUVRanR0cUV3RFFZSktvWklodmNOQVFFTEJRQXcKTFRFU01CQUdBMVVFQ3hNSmIzQmxibk5vYVdaME1SY3dGUVlEVlFRREV3NXJkV0psYkdWMExYTnBaMjVsY2pBZQpGdzB5TlRBMU1ESXdPVE0wTWpCYUZ3MHlOVEExTURNd09URTJNek5hTUZBeEZUQVRCZ05WQkFvVERITjVjM1JsCmJUcHViMlJsY3pFM01EVUdBMVVFQXhNdWMzbHpkR1Z0T201dlpHVTZiMnRrTkMxamIyNTBjbTlzTFhCc1lXNWwKTFRFdWJHRmlMbTlyWkM1c2IyTmhiREJaTUJNR0J5cUdTTTQ5QWdFR0NDcUdTTTQ5QXdFSEEwSUFCRWU5M21QTQpjTXgwMnUxZVUyNmlUK1lIcDduc3ZxWXNnUno5bjJiZ2lsTStCMFZzNXlkYkJLdCtIV2FOcTFFRktUZWtCNGpMClJqN2t0YmdpTnREcWVBaWpWakJVTUE0R0ExVWREd0VCL3dRRUF3SUhnREFUQmdOVkhTVUVEREFLQmdnckJnRUYKQlFjREFqQU1CZ05WSFJNQkFmOEVBakFBTUI4R0ExVWRJd1FZTUJhQUZQSnZ0UnB3YnpTWW96Q0JsMUNrVENrOQpRL2txTUEwR0NTcUdTSWIzRFFFQkN3VUFBNElCQVFBWVFZRC9CckppU081YW9La0h0ZTZNZW9LSWIrNTN4U3FHCkVtVEVvUkJ2QWF3M05YdzY2TEdrY2hteWdUblBkTExWNG56MVFyWVVEaStRM1VOajcxVXB0cm12UWdPU3JXcncKMG1wa3ZIWWx1S0VKQVdiN09YZ21wRW5wMWMyZFp0NFBjc1VzeW5ONWdNUTVrUGZtQklINUt2Y0daTGl0Ry9ldwowNjFnM2MrNUNQR3g4eDF0aVh1b0x4d2YzR3h4UzY1enNNZ3poWjNUSlhVaXBETmZFUHIyek96R1lnd3hYRjVzCnNhRTZvQTd3UXhlWjBFSXk1N1pEL2p6c1RMT3BEQ2hsU2tVNWMwT0hTVkkwUENhbkJJT1BtSWtoa0xtcDE3a1kKVDdxclpkanIvVUQ3L2dhdDNSdzBHTjlVdXJBOUNPMWl5L3N3UHBVSEx0U1V3bGs3VzFiZQotLS0tLUVORCBDRVJUSUZJQ0FURS0tLS0tCg==",
                "conditions": [
                    {
                        "lastTransitionTime": "2025-05-02T09:39:20Z",
                        "lastUpdateTime": "2025-05-02T09:39:20Z",
                        "message": "This CSR was approved by kubectl certificate approve.",
                        "reason": "KubectlApprove",
                        "status": "True",
                        "type": "Approved"
                    }
                ]
            }
        }
    ],
    "kind": "List",
    "metadata": {
        "resourceVersion": ""
    }
}

```