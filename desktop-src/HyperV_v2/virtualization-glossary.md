---
description: Windows 虛擬化 SDK 檔中使用的詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Hyper-v 詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194554"
---
# <a name="hyper-v-glossary"></a><span data-ttu-id="3522c-103">Hyper-v 詞彙</span><span class="sxs-lookup"><span data-stu-id="3522c-103">Hyper-V glossary</span></span>

<span data-ttu-id="3522c-104">本主題提供 Windows 虛擬化 SDK 檔中使用的詞彙術語。</span><span class="sxs-lookup"><span data-stu-id="3522c-104">This topic provides a glossary of terms used in the Windows Virtualization SDK documentation.</span></span>

<dl> <dt>

<span data-ttu-id="3522c-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**綁定**</span><span class="sxs-lookup"><span data-stu-id="3522c-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-106">軟體服務和層級連結在一起的進程。</span><span class="sxs-lookup"><span data-stu-id="3522c-106">A process by which software services and layers are linked together.</span></span> <span data-ttu-id="3522c-107">安裝網路服務時，會建立服務的系結關聯性和相依性。</span><span class="sxs-lookup"><span data-stu-id="3522c-107">When a network service is installed, the binding relationships and dependencies for the services are established.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**檢查站**</span><span class="sxs-lookup"><span data-stu-id="3522c-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**checkpoint**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-109">虛擬機器的快照，可讓系統管理員將虛擬機器復原到建立檢查點時的狀態。</span><span class="sxs-lookup"><span data-stu-id="3522c-109">A snapshot of a virtual machine that enables an administrator to roll the virtual machine back to its state at the moment the checkpoint was created.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**緊湊**</span><span class="sxs-lookup"><span data-stu-id="3522c-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**compact**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-111">藉由從 .vhd 檔案中移除未使用的空間，減少動態擴充的虛擬硬碟大小。</span><span class="sxs-lookup"><span data-stu-id="3522c-111">To reduce the size of a dynamically expanding virtual hard disk by removing unused space from the .vhd file.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**差異虛擬硬碟**</span><span class="sxs-lookup"><span data-stu-id="3522c-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**differencing virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-113">將變更儲存至相關聯之父虛擬硬碟的虛擬硬碟，目的是要讓父系保持不變。</span><span class="sxs-lookup"><span data-stu-id="3522c-113">A virtual hard disk that stores the changes to an associated parent virtual hard disk for the purpose of keeping the parent intact.</span></span> <span data-ttu-id="3522c-114">差異磁片是與父磁片之 .vhd 檔案相關聯的個別 .vhd 檔案。</span><span class="sxs-lookup"><span data-stu-id="3522c-114">The differencing disk is a separate .vhd file that is associated with the .vhd file of the parent disk.</span></span> <span data-ttu-id="3522c-115">變更會繼續累積到差異磁片，直到它合併到父磁片為止。</span><span class="sxs-lookup"><span data-stu-id="3522c-115">Changes continue to accumulate in the differencing disk until it is merged to the parent disk.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**動態擴充虛擬硬碟**</span><span class="sxs-lookup"><span data-stu-id="3522c-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**dynamically expanding virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-117">每次修改時都會成長大小的虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="3522c-117">A virtual hard disk that grows in size each time it is modified.</span></span> <span data-ttu-id="3522c-118">這種類型的虛擬硬碟會以 3 KB .vhd 檔案的形式啟動，而且可成長為檔案建立時所指定的大小上限。</span><span class="sxs-lookup"><span data-stu-id="3522c-118">This type of virtual hard disk starts as a 3 KB .vhd file and can grow as large as the maximum size specified when the file was created.</span></span> <span data-ttu-id="3522c-119">減少檔案大小的唯一方法是將已刪除的資料移至零，然後壓縮虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="3522c-119">The only way to reduce the file size is to zero out the deleted data and then compact the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**固定大小的虛擬硬碟**</span><span class="sxs-lookup"><span data-stu-id="3522c-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**fixed-size virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-121">具有固定大小的虛擬硬碟，並在建立磁片時配置所有空間。</span><span class="sxs-lookup"><span data-stu-id="3522c-121">A virtual hard disk with a fixed size that is determined and for which all space is allocated when the disk is created.</span></span> <span data-ttu-id="3522c-122">新增或刪除資料時，磁片的大小不會變更。</span><span class="sxs-lookup"><span data-stu-id="3522c-122">The size of the disk does not change when data is added or deleted.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**第1代虛擬機器**</span><span class="sxs-lookup"><span data-stu-id="3522c-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Generation 1 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-124">虛擬機器 (VM) ，其中包含 Windows 8.1 和 Windows Server 2012 R2 之前的 Hyper-v 版本中存在相同的虛擬硬體</span><span class="sxs-lookup"><span data-stu-id="3522c-124">A virtual machine (VM) that contains the same virtual hardware present in versions of Hyper-V prior to Windows 8.1 and Windows Server 2012 R2</span></span>

</dd> <dt>

<span data-ttu-id="3522c-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**第2代虛擬機器**</span><span class="sxs-lookup"><span data-stu-id="3522c-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Generation 2 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-126">虛擬機器 (VM) ，其中包含簡化的虛擬硬體模型，並使用 UEFI 固件而非 BIOS。</span><span class="sxs-lookup"><span data-stu-id="3522c-126">A virtual machine (VM) that contains a simplified virtual hardware model and uses UEFI firmware instead of BIOS.</span></span> <span data-ttu-id="3522c-127">在此 VM 中，大部分的模擬裝置都會被移除，進而降低管理複雜度和安全性攻擊面。</span><span class="sxs-lookup"><span data-stu-id="3522c-127">In this VM, most of the emulated devices are removed, which reduces management complexity and security attack surface.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**客體作業系統**</span><span class="sxs-lookup"><span data-stu-id="3522c-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**guest operating system**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-129">在虛擬機器上執行的作業系統。</span><span class="sxs-lookup"><span data-stu-id="3522c-129">The operating system running on a virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**integration services**</span><span class="sxs-lookup"><span data-stu-id="3522c-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**integration services**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-131">服務與軟體驅動程式的集合，可將效能最大化，並在虛擬機器中提供更好的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="3522c-131">A collection of services and software drivers that maximize performance and provide a better user experience within a virtual machine.</span></span> <span data-ttu-id="3522c-132">Integration services 僅適用于支援的客體作業系統。</span><span class="sxs-lookup"><span data-stu-id="3522c-132">Integration services are only available for supported guest operating systems.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**索引鍵/值組**</span><span class="sxs-lookup"><span data-stu-id="3522c-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**key-value pair**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-134">包含唯一識別碼的資料項目目集，稱為索引鍵，而值則是索引鍵的實際資料。</span><span class="sxs-lookup"><span data-stu-id="3522c-134">A set of data items that contains a unique identifier, called a key, and a value that is the actual data for the key.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**實體電腦**</span><span class="sxs-lookup"><span data-stu-id="3522c-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**physical computer**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-136">以硬體為基礎的電腦，而不是以軟體為基礎的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="3522c-136">A hardware-based computer, as opposed to a software-based virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**儲存狀態**</span><span class="sxs-lookup"><span data-stu-id="3522c-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**saved state**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-138">一種儲存虛擬機器的方式，讓它可以快速恢復，類似于休眠的膝上型電腦。</span><span class="sxs-lookup"><span data-stu-id="3522c-138">A manner of storing a virtual machine so that it can be quickly resumed, similar to a hibernated laptop.</span></span> <span data-ttu-id="3522c-139">當您將執行中的虛擬機器置於儲存狀態時，Virtual Server 和 Hyper-v 會停止該虛擬機器，並將存在於記憶體中的資料寫入暫存檔案，並停止耗用系統資源。</span><span class="sxs-lookup"><span data-stu-id="3522c-139">When you place a running virtual machine in a saved state, Virtual Server and Hyper-V stop the virtual machine, write the data that exists in memory to temporary files, and stop the consumption of system resources.</span></span> <span data-ttu-id="3522c-140">從儲存的狀態還原虛擬機器，會傳回其狀態儲存時的相同條件。</span><span class="sxs-lookup"><span data-stu-id="3522c-140">Restoring a virtual machine from a saved state returns it to the same condition it was in when its state was saved.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**虛擬磁片**</span><span class="sxs-lookup"><span data-stu-id="3522c-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**virtual floppy disk**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-142">實體磁碟的檔案形式版本。</span><span class="sxs-lookup"><span data-stu-id="3522c-142">A file-based version of a physical floppy disk.</span></span> <span data-ttu-id="3522c-143">虛擬磁片會儲存為副檔名為 .vfd 的檔案。</span><span class="sxs-lookup"><span data-stu-id="3522c-143">A virtual floppy disk is stored as a file with a .vfd file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**虛擬硬碟**</span><span class="sxs-lookup"><span data-stu-id="3522c-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-145">虛擬機器的儲存媒體。</span><span class="sxs-lookup"><span data-stu-id="3522c-145">The storage medium for a virtual machine.</span></span> <span data-ttu-id="3522c-146">它可以位於主機作業系統可存取的任何存放裝置拓撲上，包括外部裝置、儲存區域網路，以及網路連接的存放裝置。</span><span class="sxs-lookup"><span data-stu-id="3522c-146">It can reside on any storage topology that the host operating system can access, including external devices, storage area networks, and network-attached storage.</span></span> <span data-ttu-id="3522c-147">副檔名為 .vhd。</span><span class="sxs-lookup"><span data-stu-id="3522c-147">The file name extension is .vhd.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**虛擬機器**</span><span class="sxs-lookup"><span data-stu-id="3522c-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-149">電腦內的電腦，會在軟體中執行。</span><span class="sxs-lookup"><span data-stu-id="3522c-149">A computer within a computer, implemented in software.</span></span> <span data-ttu-id="3522c-150">虛擬機器會模擬獨立、隔離的環境中完整的硬體系統 (從處理器到網路卡)，讓原本不相容的作業系統能夠同步運作。</span><span class="sxs-lookup"><span data-stu-id="3522c-150">A virtual machine emulates a complete hardware system, from processor to network card, in a self-contained, isolated software environment, enabling the simultaneous operation of otherwise incompatible operating systems.</span></span> <span data-ttu-id="3522c-151">每個子作業系統都是在它自己的隔離軟體虛擬機器中執行。</span><span class="sxs-lookup"><span data-stu-id="3522c-151">Each child operating system runs in its own isolated software virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**虛擬機器設定**</span><span class="sxs-lookup"><span data-stu-id="3522c-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**virtual machine configuration**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-153">指派給虛擬機器的資源設定。</span><span class="sxs-lookup"><span data-stu-id="3522c-153">The configuration of the resources assigned to a virtual machine.</span></span> <span data-ttu-id="3522c-154">範例包括磁片和網路介面卡等裝置，以及記憶體和處理器。</span><span class="sxs-lookup"><span data-stu-id="3522c-154">Examples include devices such as disks and network adapters, as well as memory and processors.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**虛擬機器管理服務**</span><span class="sxs-lookup"><span data-stu-id="3522c-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Virtual Machine Management Service**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-156">提供虛擬機器管理存取權的 Hyper-v 服務。</span><span class="sxs-lookup"><span data-stu-id="3522c-156">The Hyper-V service that provides management access to virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**虛擬機器快照集**</span><span class="sxs-lookup"><span data-stu-id="3522c-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**virtual machine snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-158">在特定時間點，以檔案為基礎的狀態、磁片資料和虛擬機器設定快照集。</span><span class="sxs-lookup"><span data-stu-id="3522c-158">A file-based snapshot of the state, disk data, and configuration of a virtual machine at a specific point in time.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**虛擬網路**</span><span class="sxs-lookup"><span data-stu-id="3522c-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**virtual network**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-160">實體網路交換器的虛擬版本。</span><span class="sxs-lookup"><span data-stu-id="3522c-160">A virtual version of a physical network switch.</span></span> <span data-ttu-id="3522c-161">您可以將虛擬網路設定成可以存取一或多部虛擬機器的本機或外部網路資源。</span><span class="sxs-lookup"><span data-stu-id="3522c-161">A virtual network can be configured to provide access to local or external network resources for one or more virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**虛擬網路管理員**</span><span class="sxs-lookup"><span data-stu-id="3522c-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Virtual Network Manager**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-163">用來建立和管理虛擬網路的 Hyper-v 服務。</span><span class="sxs-lookup"><span data-stu-id="3522c-163">A Hyper-V service used to create and manage virtual networks.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**虛擬交換器**</span><span class="sxs-lookup"><span data-stu-id="3522c-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**virtual switch**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-165">請參閱虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="3522c-165">See virtual network.</span></span>

</dd> <dt>

<span data-ttu-id="3522c-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**VHDX 調整大小**</span><span class="sxs-lookup"><span data-stu-id="3522c-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**VHDX resize**</span></span>
</dt> <dd>

<span data-ttu-id="3522c-167">壓縮或展開虛擬硬碟的操作。</span><span class="sxs-lookup"><span data-stu-id="3522c-167">The operation that shrinks or expands a virtual hard disk.</span></span>

</dd> </dl>

 

 



