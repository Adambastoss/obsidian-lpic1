
##### KVM (Kernel-based Virtual Machine)

Módulo do kernel Linux que o transforma em um hipervisor.

O KVM se utiliza da **virtualização assistida por hardware** (Intel VT-x ou AMD-V) para atingir um desempenho muito alto.

**`libvirt`**: Esta é uma API e um conjunto de ferramentas de gerenciamento. Ele fornece uma CLI (`virsh`) e ferramentas gráficas para gerenciar máquinas virtuais.

###### INICIAR UMA VM: ``virsh start <nome_da_vm>
###### LISTAR VMs: ``virsh list
###### PARAR VM: ``virsh shutdown <nome_da_vm>

**`QEMU`**: O **QEMU** é um ==emulador== de hardware. Ele é usado em conjunto com o KVM.
O **KVM** fornece a aceleração do ==processador==, enquanto o **QEMU** ==emula== o restante do hardware (placa de vídeo, disco rígido, placa de rede, etc.).