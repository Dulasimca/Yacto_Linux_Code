# Instruction for Build
### Run the Following commands for creating Build environment and building
<ol><li><pre>mkdir riscv-incoresemi; cd riscv-incoresemi</pre></li>
 <li><pre>repo init -u https://gitlab.com/outer_space/meta-incoresemi -m tools/manifests/incoresemi.xml</pre></li>
 <li><pre>repo sync</pre></li>
 <li><pre>MACHINE=chromite-h bitbake opensbi</pre></li></ol>
