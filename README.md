# V2ray-OpenWRT
Compiled V2Ray Binaries for OpenWRT(ipk file)
ΪOpenWRT�����V2Ray�������ļ���ipk��ʽ��
Source Merged from an "Outdated" Lede firmware
Դ�����һ�ݡ���ʱ����Lede�̼����ϲ�
https://github.com/coolsnowwolf/lede/pull/331
#--------------Installations----------------
1.Install V2ray,V2ray Pro and the Depencies
1.��װV2ray,V2ray Pro������
Note the package dnsmasq-full would make a conflict with the current dnsmasq,so run the following commands:
ע��������dnsmasq-full�����ִ���Ŀdnsmasq��ͻ�������������������
opkg remove dnsmasq
opkg install YourFileNameOfDnsmasq-full(���dnsmasq-full�ļ�����)
2.Because OpenWRT's ip command isn't in its correct place so a link is required:
2.��ΪOpenWRT��ip���������ȷ��λ���ϣ�����������Ҫһ�����ӣ�
which ip
ln -s YourIPPathFromWhich(which����ʾ�ĵ�ַ) /usr/bin/ip
3.Generate V2Ray profile manually by using:
3.ͨ�����������ֶ�����V2ray�����ļ���
cd /etc/v2ray
lua gen_config.lua
cp TheGeneratedProfile(��һ�����ɵ������ļ�) ./
4.Enable the LuCi V2ray-Pro server
4.����ͼ�λ�V2Ray-Pro������
service v2raypro start
5.Further settings in LuCi interface
��LuCi��������������
