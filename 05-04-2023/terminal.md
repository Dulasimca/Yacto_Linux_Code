<pre>(yocto) (base) <font color="#26A269"><b>padmanaban@administrator-ThinkBook-15-G3-ACL</b></font>:<font color="#12488B"><b>/media/padmanaban/e5fd8dba-c6a6-4243-8cee-aed03004ac1d/ri2/build</b></font>$ MACHINE=chromite-h bitbake opensbi
Loading cache: 100% |###############################################################################################################################################################################| Time: 0:00:00
Loaded 4017 entries from dependency cache.
<font color="#C01C28"><b>ERROR</b></font>: <font color="#C01C28">ExpansionError during parsing /media/padmanaban/e5fd8dba-c6a6-4243-8cee-aed03004ac1d/ri2/incore-Layer/recipes-kernel/incore.bb</font>                                                              | ETA:  --:--:--
Traceback (most recent call last):
  File &quot;Var &lt;do_fetch[file-checksums]&gt;&quot;, line 1, in &lt;module&gt;
  File &quot;/media/padmanaban/e5fd8dba-c6a6-4243-8cee-aed03004ac1d/ri2/openembedded-core/bitbake/lib/bb/fetch2/__init__.py&quot;, line 1228, in get_checksum_file_list(d=&lt;bb.data_smart.DataSmart object at 0x7f763d24fd30&gt;):
         &quot;&quot;&quot;
    &gt;    fetch = Fetch([], d, cache = False, localonly = True)
         filelist = []
  File &quot;/media/padmanaban/e5fd8dba-c6a6-4243-8cee-aed03004ac1d/ri2/openembedded-core/bitbake/lib/bb/fetch2/__init__.py&quot;, line 1684, in Fetch.__init__(urls=[&apos;file://&apos;], d=&lt;bb.data_smart.DataSmart object at 0x7f763d24fd30&gt;, cache=False, localonly=True, connection_cache=None):
                     try:
    &gt;                    self.ud[url] = FetchData(url, d, localonly)
                     except NonLocalMethod:
  File &quot;/media/padmanaban/e5fd8dba-c6a6-4243-8cee-aed03004ac1d/ri2/openembedded-core/bitbake/lib/bb/fetch2/__init__.py&quot;, line 1271, in FetchData.__init__(url=&apos;file://&apos;, d=&lt;bb.data_smart.DataSmart object at 0x7f763d24fd30&gt;, localonly=True):
             self.basepath = None
    &gt;        (self.type, self.host, self.path, self.user, self.pswd, self.parm) = decodeurl(d.expand(url))
             self.date = self.getSRCDate(d)
  File &quot;/media/padmanaban/e5fd8dba-c6a6-4243-8cee-aed03004ac1d/ri2/openembedded-core/bitbake/lib/bb/fetch2/__init__.py&quot;, line 357, in decodeurl(url=&apos;file://&apos;):
         if not m:
    &gt;        raise MalformedUrl(url)
     
bb.data_smart.ExpansionError: Failure expanding variable do_fetch[file-checksums], expression was ${@bb.fetch.get_checksum_file_list(d)}  ${@get_lic_checksum_file_list(d)} which triggered exception MalformedUrl: The URL: &apos;file://&apos; is invalid and cannot be interpreted
The variable dependency chain for the failure is: do_fetch[file-checksums]

<font color="#C01C28"><b>ERROR</b></font>: <font color="#C01C28">Parsing halted due to errors, see error messages above</font>

Summary: There were 2 ERROR messages, returning a non-zero exit code.
(yocto) (base) <font color="#26A269"><b>padmanaban@administrator-ThinkBook-15-G3-ACL</b></font>:<font color="#12488B"><b>/media/padmanaban/e5fd8dba-c6a6-4243-8cee-aed03004ac1d/ri2/build</b></font>$ MACHINE=chromite-h bitbake opensbi
Loading cache: 100% |###############################################################################################################################################################################| Time: 0:00:00
Loaded 4017 entries from dependency cache.
Parsing recipes: 100% |#############################################################################################################################################################################| Time: 0:00:03
Parsing of 2576 .bb files complete (2570 cached, 6 parsed). 4029 targets, 450 skipped, 0 masked, 0 errors.
<b>NOTE</b>: Resolving any missing task queue dependencies

Build Configuration:
BB_VERSION           = &quot;2.2.0&quot;
BUILD_SYS            = &quot;x86_64-linux&quot;
NATIVELSBSTRING      = &quot;universal&quot;
TARGET_SYS           = &quot;riscv64-oe-linux&quot;
MACHINE              = &quot;chromite-h&quot;
DISTRO               = &quot;nodistro&quot;
DISTRO_VERSION       = &quot;nodistro.0&quot;
TUNE_FEATURES        = &quot;riscv64&quot;
meta                 = &quot;HEAD:a0ef4386d37f84e8f169cbe3cfa9307010b89bbd&quot;
meta-oe              
meta-python          
meta-multimedia      
meta-networking      = &quot;HEAD:3f9340a9241d497753b330d90d6a3d8332c1ba7f&quot;
meta-riscv           = &quot;HEAD:d5628ffd5adadb879dee96b3beb076ca2abfcf6d&quot;
meta-incoresemi      = &quot;HEAD:9f91055ad87e6d7d385f1aaaecbab9c31f5b4cf3&quot;
incore-Layer         = &quot;&lt;unknown&gt;:&lt;unknown&gt;&quot;

Initialising tasks: 100% |##########################################################################################################################################################################| Time: 0:00:02
Sstate summary: Wanted 687 Local 0 Mirrors 0 Missed 687 Current 98 (0% match, 12% complete)
<b>NOTE</b>: Executing Tasks
<font color="#A2734C"><b>WARNING</b></font>: <font color="#A2734C">shared-mime-info-native-2.2-r0 do_fetch: Failed to fetch URL git://gitlab.freedesktop.org/xdg/shared-mime-info.git;protocol=https;branch=master, attempting MIRRORS if available</font>
<font color="#A2734C"><b>WARNING</b></font>: <font color="#A2734C">linux-mainline-5.11+gitAUTOINC+399fcd7052-r0 do_package_qa: QA Issue: File /usr/src/debug/linux-mainline/5.11+gitAUTOINC+399fcd7052-r0/lib/oid_registry_data.c in package linux-mainline-src contains reference to TMPDIR</font>
<font color="#A2734C">File /usr/src/debug/linux-mainline/5.11+gitAUTOINC+399fcd7052-r0/drivers/tty/vt/consolemap_deftbl.c in package linux-mainline-src contains reference to TMPDIR [buildpaths]</font>
<font color="#A2734C"><b>WARNING</b></font>: <font color="#A2734C">opensbi-1.1-r0 do_package_qa: QA Issue: File /share/opensbi/lp64/generic/firmware/.debug/fw_dynamic.elf in package opensbi-dbg contains reference to TMPDIR</font>
<font color="#A2734C">File /share/opensbi/lp64/generic/firmware/.debug/fw_jump.elf in package opensbi-dbg contains reference to TMPDIR</font>
<font color="#A2734C">File /share/opensbi/lp64/generic/firmware/.debug/fw_payload.elf in package opensbi-dbg contains reference to TMPDIR [buildpaths]</font>
<font color="#A2734C"><b>WARNING</b></font>: <font color="#A2734C">opensbi-1.1-r0 do_package_qa: QA Issue: File /share/opensbi/lp64/generic/firmware/fw_dynamic.elf in package opensbi contains reference to TMPDIR</font>
<font color="#A2734C">File /share/opensbi/lp64/generic/firmware/fw_jump.elf in package opensbi contains reference to TMPDIR</font>
<font color="#A2734C">File /share/opensbi/lp64/generic/firmware/fw_payload.elf in package opensbi contains reference to TMPDIR [buildpaths]</font>
<b>NOTE</b>: Tasks Summary: Attempted 2018 tasks of which 480 didn&apos;t need to be rerun and all succeeded.
<b>NOTE</b>: Writing buildhistory
<b>NOTE</b>: Writing buildhistory took: 2 seconds
<b>NOTE</b>: Build completion summary:
<b>NOTE</b>:   do_populate_sysroot: 0.0% sstate reuse(0 setscene, 121 scratch)
<b>NOTE</b>:   do_deploy_source_date_epoch: 0.0% sstate reuse(0 setscene, 106 scratch)
<b>NOTE</b>:   do_package_qa: 0.0% sstate reuse(0 setscene, 70 scratch)
<b>NOTE</b>:   do_package: 0.0% sstate reuse(0 setscene, 70 scratch)
<b>NOTE</b>:   do_packagedata: 0.0% sstate reuse(0 setscene, 70 scratch)
<b>NOTE</b>:   do_package_write_ipk: 0.0% sstate reuse(0 setscene, 70 scratch)
<b>NOTE</b>:   do_populate_lic: 0.0% sstate reuse(0 setscene, 173 scratch)

Summary: There were 4 WARNING messages.
(yocto) (base) <font color="#26A269"><b>padmanaban@administrator-ThinkBook-15-G3-ACL</b></font>:<font color="#12488B"><b>/media/padmanaban/e5fd8dba-c6a6-4243-8cee-aed03004ac1d/ri2/build</b></font>(yocto) (base) <font color="#26A269"><b>padmanaban@administrator-ThinkBook-15-G3-ACL</b></font>:<font color="#12488B"><b>/media/padmanaban/e5fd8dba-</b></font>(yocto) (base) <font color="#26A269"><b>padmanaban@administrator-ThinkBook-15-G3-ACL</b></font>:<font color="#12488B"><b>/media/padmanaban/e5fd8dba-c6a6-4243-8cee-aed03004ac1d/ri2/build</b></font>$ 

</pre>
