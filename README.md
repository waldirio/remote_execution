# remote_execution

Just to test the paramiko module/library.

https://github.com/paramiko/paramiko/


Below the simple example showing us the cpuinfo

```
(remote_execution) [wpinheir@ironman remote_execution]$ ./demo_simple.py 
Hostname: 192.168.56.215
Username [wpinheir]: root
Password for root@192.168.56.215: 
/home/wpinheir/.virtualenvs/remote_execution/lib/python3.6/site-packages/paramiko/ecdsakey.py:164: CryptographyDeprecationWarning: Support for unsafe construction of public numbers from encoded data will be removed in a future version. Please use EllipticCurvePublicKey.from_encoded_point
  self.ecdsa_curve.curve_class(), pointinfo
*** Connecting...
/home/wpinheir/.virtualenvs/remote_execution/lib/python3.6/site-packages/paramiko/kex_ecdh_nist.py:39: CryptographyDeprecationWarning: encode_point has been deprecated on EllipticCurvePublicNumbers and will be removed in a future version. Please use EllipticCurvePublicKey.public_bytes to obtain both compressed and uncompressed point encoding.
  m.add_string(self.Q_C.public_numbers().encode_point())
/home/wpinheir/.virtualenvs/remote_execution/lib/python3.6/site-packages/paramiko/kex_ecdh_nist.py:96: CryptographyDeprecationWarning: Support for unsafe construction of public numbers from encoded data will be removed in a future version. Please use EllipticCurvePublicKey.from_encoded_point
  self.curve, Q_S_bytes
/home/wpinheir/.virtualenvs/remote_execution/lib/python3.6/site-packages/paramiko/kex_ecdh_nist.py:111: CryptographyDeprecationWarning: encode_point has been deprecated on EllipticCurvePublicNumbers and will be removed in a future version. Please use EllipticCurvePublicKey.public_bytes to obtain both compressed and uncompressed point encoding.
  hm.add_string(self.Q_C.public_numbers().encode_point())
... processor	: 0
... vendor_id	: GenuineIntel
... cpu family	: 6
... model		: 6
... model name	: QEMU Virtual CPU version 2.5+
... stepping	: 3
... microcode	: 0x1
... cpu MHz		: 2712.000
... cache size	: 16384 KB
... physical id	: 0
... siblings	: 1
... core id		: 0
... cpu cores	: 1
... apicid		: 0
... initial apicid	: 0
... fpu		: yes
... fpu_exception	: yes
... cpuid level	: 13
... wp		: yes
... flags		: fpu de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pse36 clflush mmx fxsr sse sse2 syscall nx lm rep_good nopl xtopology pni cx16 x2apic hypervisor lahf_lm
... bogomips	: 5424.00
... clflush size	: 64
... cache_alignment	: 64
... address sizes	: 40 bits physical, 48 bits virtual
... power management:
```

To use it, my advice is:
- Create a virtual environment to your application
```
$ python3 -m venv ~/.virtualenvs/remote_execution
```
- Load the virtual env
```
$ source ~/.virtualenvs/remote_execution/bin/activate
```
- Install the paramiko module
```
$ pip install paramiko
``` 
- Download the example
```
$ wget https://raw.githubusercontent.com/waldirio/remote_execution/master/demo_simple.py
```
- Set the permission
```
$ chmod +x demo_simple.py
```
- Run it
```
(remote_execution) [wpinheir@ironman remote_execution]$ ./demo_simple.py 
Hostname: 
```

