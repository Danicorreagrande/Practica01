zone "example.com" {
    type master;
    file "/etc/bind/db.example.com";
};


;
; BIND data file for example.com 
;
$TTL	604800
@	IN	SOA	example.com. root.example.com. (
			      2		; Serial
			 604800		; Refresh
			  86400		; Retry
			2419200		; Expire
			 604800 )	; Negative Cache TTL
;
@		IN	NS		ns.example.com.
@		IN	A		127.0.0.1
@		IN	AAAA	::1
ns 		IN	AAAA	172.18.0.3
songoku	IN 	A		10.1.0.254
juan	IN 	TXT "profesor_de_iaw"


forwarders {
		8.8.8.8;
		8.8.4.4;
	 };