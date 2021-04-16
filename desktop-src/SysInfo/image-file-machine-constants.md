---
description: 描述可能的電腦架構。
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: " (Winnt. h) 的影像檔電腦常數"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511984"
---
# <a name="image-file-machine-constants"></a><span data-ttu-id="755a8-103">影像檔案電腦常數</span><span class="sxs-lookup"><span data-stu-id="755a8-103">Image File Machine Constants</span></span>

<span data-ttu-id="755a8-104">描述可能的電腦架構。</span><span class="sxs-lookup"><span data-stu-id="755a8-104">Describes possible machine architectures.</span></span> <span data-ttu-id="755a8-105">用於 [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a)、 [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) 和 [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2)。</span><span class="sxs-lookup"><span data-stu-id="755a8-105">Used in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) and [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span></span>

<dl> <dt>

<span data-ttu-id="755a8-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**圖像 \_ 檔 \_ 電腦 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="755a8-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**IMAGE\_FILE\_MACHINE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-107">0</span><span class="sxs-lookup"><span data-stu-id="755a8-107">0</span></span>
</dt> <dt>



<span data-ttu-id="755a8-108">Unknown</span><span class="sxs-lookup"><span data-stu-id="755a8-108">Unknown</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**圖像 \_ 檔 \_ 電腦 \_ 目標 \_ 主機**</span><span class="sxs-lookup"><span data-stu-id="755a8-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**IMAGE\_FILE\_MACHINE\_TARGET\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="755a8-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="755a8-111">與主機互動，而不是 WOW64 來賓</span><span class="sxs-lookup"><span data-stu-id="755a8-111">Interacts with the host and not a WOW64 guest</span></span>

> [!Note]  
> <span data-ttu-id="755a8-112">從 Windows 10、1607版和 Windows Server 2016 開始，可以使用這個常數。</span><span class="sxs-lookup"><span data-stu-id="755a8-112">This constant is available starting with Windows 10, version 1607 and Windows Server 2016.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**圖像 \_ 檔 \_ 機器 \_ I386**</span><span class="sxs-lookup"><span data-stu-id="755a8-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**IMAGE\_FILE\_MACHINE\_I386**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-114">0x014c</span><span class="sxs-lookup"><span data-stu-id="755a8-114">0x014c</span></span>
</dt> <dt>



<span data-ttu-id="755a8-115">Intel 386</span><span class="sxs-lookup"><span data-stu-id="755a8-115">Intel 386</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**圖像 \_ 檔 \_ 機器 \_ R3000**</span><span class="sxs-lookup"><span data-stu-id="755a8-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**IMAGE\_FILE\_MACHINE\_R3000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-117">0x0162</span><span class="sxs-lookup"><span data-stu-id="755a8-117">0x0162</span></span>
</dt> <dt>



<span data-ttu-id="755a8-118">MIPS 位元組由小到大、0x160 位元組由大到小</span><span class="sxs-lookup"><span data-stu-id="755a8-118">MIPS little-endian, 0x160 big-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**圖像 \_ 檔 \_ 機器 \_ R4000**</span><span class="sxs-lookup"><span data-stu-id="755a8-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**IMAGE\_FILE\_MACHINE\_R4000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-120">0x0166</span><span class="sxs-lookup"><span data-stu-id="755a8-120">0x0166</span></span>
</dt> <dt>



<span data-ttu-id="755a8-121">MIPS 小位元組由小到大</span><span class="sxs-lookup"><span data-stu-id="755a8-121">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**圖像 \_ 檔 \_ 機器 \_ R10000**</span><span class="sxs-lookup"><span data-stu-id="755a8-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**IMAGE\_FILE\_MACHINE\_R10000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-123">0x0168</span><span class="sxs-lookup"><span data-stu-id="755a8-123">0x0168</span></span>
</dt> <dt>



<span data-ttu-id="755a8-124">MIPS 小位元組由小到大</span><span class="sxs-lookup"><span data-stu-id="755a8-124">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**圖像 \_ 檔 \_ 機器 \_ WCEMIPSV2**</span><span class="sxs-lookup"><span data-stu-id="755a8-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**IMAGE\_FILE\_MACHINE\_WCEMIPSV2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-126">0x0169</span><span class="sxs-lookup"><span data-stu-id="755a8-126">0x0169</span></span>
</dt> <dt>



<span data-ttu-id="755a8-127">MIPS 位元組由小到小 WCE v2</span><span class="sxs-lookup"><span data-stu-id="755a8-127">MIPS little-endian WCE v2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**圖像 \_ 檔 \_ 電腦 \_ ALPHA**</span><span class="sxs-lookup"><span data-stu-id="755a8-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**IMAGE\_FILE\_MACHINE\_ALPHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-129">0x0184</span><span class="sxs-lookup"><span data-stu-id="755a8-129">0x0184</span></span>
</dt> <dt>



<span data-ttu-id="755a8-130">Alpha \_ AXP</span><span class="sxs-lookup"><span data-stu-id="755a8-130">Alpha\_AXP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**圖像 \_ 檔 \_ 機器 \_ SH3**</span><span class="sxs-lookup"><span data-stu-id="755a8-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**IMAGE\_FILE\_MACHINE\_SH3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-132">0x01a2</span><span class="sxs-lookup"><span data-stu-id="755a8-132">0x01a2</span></span>
</dt> <dt>



<span data-ttu-id="755a8-133">SH3 位元組由小到大</span><span class="sxs-lookup"><span data-stu-id="755a8-133">SH3 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**圖像 \_ 檔 \_ 機器 \_ SH3DSP**</span><span class="sxs-lookup"><span data-stu-id="755a8-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**IMAGE\_FILE\_MACHINE\_SH3DSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-135">0x01a3</span><span class="sxs-lookup"><span data-stu-id="755a8-135">0x01a3</span></span>
</dt> <dt>



<span data-ttu-id="755a8-136">SH3DSP</span><span class="sxs-lookup"><span data-stu-id="755a8-136">SH3DSP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**圖像 \_ 檔 \_ 機器 \_ SH3E**</span><span class="sxs-lookup"><span data-stu-id="755a8-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**IMAGE\_FILE\_MACHINE\_SH3E**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-138">0x01a4</span><span class="sxs-lookup"><span data-stu-id="755a8-138">0x01a4</span></span>
</dt> <dt>



<span data-ttu-id="755a8-139">SH3E 位元組由小到大</span><span class="sxs-lookup"><span data-stu-id="755a8-139">SH3E little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**圖像 \_ 檔 \_ 機器 \_ SH4**</span><span class="sxs-lookup"><span data-stu-id="755a8-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**IMAGE\_FILE\_MACHINE\_SH4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-141">0x01a6</span><span class="sxs-lookup"><span data-stu-id="755a8-141">0x01a6</span></span>
</dt> <dt>



<span data-ttu-id="755a8-142">SH4 位元組由小到大</span><span class="sxs-lookup"><span data-stu-id="755a8-142">SH4 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**圖像 \_ 檔 \_ 機器 \_ SH5**</span><span class="sxs-lookup"><span data-stu-id="755a8-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**IMAGE\_FILE\_MACHINE\_SH5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-144">0x01a8</span><span class="sxs-lookup"><span data-stu-id="755a8-144">0x01a8</span></span>
</dt> <dt>



<span data-ttu-id="755a8-145">SH5</span><span class="sxs-lookup"><span data-stu-id="755a8-145">SH5</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**圖像 \_ 檔 \_ 機器 \_ ARM**</span><span class="sxs-lookup"><span data-stu-id="755a8-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**IMAGE\_FILE\_MACHINE\_ARM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-147">0x01c0</span><span class="sxs-lookup"><span data-stu-id="755a8-147">0x01c0</span></span>
</dt> <dt>



<span data-ttu-id="755a8-148">ARM Little-Endian</span><span class="sxs-lookup"><span data-stu-id="755a8-148">ARM Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**圖像 \_ 檔 \_ 機器 \_ 經驗**</span><span class="sxs-lookup"><span data-stu-id="755a8-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**IMAGE\_FILE\_MACHINE\_THUMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-150">0x01c2</span><span class="sxs-lookup"><span data-stu-id="755a8-150">0x01c2</span></span>
</dt> <dt>



<span data-ttu-id="755a8-151">ARM Thumb/Thumb-2 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="755a8-151">ARM Thumb/Thumb-2 Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**圖像 \_ 檔 \_ 機器 \_ ARMNT**</span><span class="sxs-lookup"><span data-stu-id="755a8-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**IMAGE\_FILE\_MACHINE\_ARMNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-153">0x01c4</span><span class="sxs-lookup"><span data-stu-id="755a8-153">0x01c4</span></span>
</dt> <dt>



<span data-ttu-id="755a8-154">ARM Thumb-2 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="755a8-154">ARM Thumb-2 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="755a8-155">從 Windows 7 和 Windows Server 2008 R2 開始，可以使用這個常數。</span><span class="sxs-lookup"><span data-stu-id="755a8-155">This constant is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**圖像 \_ 檔 \_ 機器 \_ AM33**</span><span class="sxs-lookup"><span data-stu-id="755a8-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**IMAGE\_FILE\_MACHINE\_AM33**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-157">0x01d3</span><span class="sxs-lookup"><span data-stu-id="755a8-157">0x01d3</span></span>
</dt> <dt>



<span data-ttu-id="755a8-158">TAM33BD</span><span class="sxs-lookup"><span data-stu-id="755a8-158">TAM33BD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**圖像 \_ 檔 \_ 機器 \_ POWERPC**</span><span class="sxs-lookup"><span data-stu-id="755a8-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**IMAGE\_FILE\_MACHINE\_POWERPC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-160">0x01F0</span><span class="sxs-lookup"><span data-stu-id="755a8-160">0x01F0</span></span>
</dt> <dt>



<span data-ttu-id="755a8-161">IBM PowerPC Little-Endian</span><span class="sxs-lookup"><span data-stu-id="755a8-161">IBM PowerPC Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**圖像 \_ 檔 \_ 機器 \_ POWERPCFP**</span><span class="sxs-lookup"><span data-stu-id="755a8-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**IMAGE\_FILE\_MACHINE\_POWERPCFP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-163">0x01f1</span><span class="sxs-lookup"><span data-stu-id="755a8-163">0x01f1</span></span>
</dt> <dt>



<span data-ttu-id="755a8-164">POWERPCFP</span><span class="sxs-lookup"><span data-stu-id="755a8-164">POWERPCFP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**圖像 \_ 檔案 \_ 電腦 \_ IA64**</span><span class="sxs-lookup"><span data-stu-id="755a8-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**IMAGE\_FILE\_MACHINE\_IA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-166">0x0200</span><span class="sxs-lookup"><span data-stu-id="755a8-166">0x0200</span></span>
</dt> <dt>



<span data-ttu-id="755a8-167">Intel 64</span><span class="sxs-lookup"><span data-stu-id="755a8-167">Intel 64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**圖像 \_ 檔 \_ 機器 \_ MIPS16**</span><span class="sxs-lookup"><span data-stu-id="755a8-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**IMAGE\_FILE\_MACHINE\_MIPS16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-169">0x0266</span><span class="sxs-lookup"><span data-stu-id="755a8-169">0x0266</span></span>
</dt> <dt>



<span data-ttu-id="755a8-170">MIPS</span><span class="sxs-lookup"><span data-stu-id="755a8-170">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**圖像 \_ 檔 \_ 機器 \_ ALPHA64**</span><span class="sxs-lookup"><span data-stu-id="755a8-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**IMAGE\_FILE\_MACHINE\_ALPHA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-172">0x0284</span><span class="sxs-lookup"><span data-stu-id="755a8-172">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="755a8-173">ALPHA64</span><span class="sxs-lookup"><span data-stu-id="755a8-173">ALPHA64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**圖像 \_ 檔 \_ 機器 \_ MIPSFPU**</span><span class="sxs-lookup"><span data-stu-id="755a8-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-175">0x0366</span><span class="sxs-lookup"><span data-stu-id="755a8-175">0x0366</span></span>
</dt> <dt>



<span data-ttu-id="755a8-176">MIPS</span><span class="sxs-lookup"><span data-stu-id="755a8-176">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**圖像 \_ 檔 \_ 機器 \_ MIPSFPU16**</span><span class="sxs-lookup"><span data-stu-id="755a8-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-178">0x0466</span><span class="sxs-lookup"><span data-stu-id="755a8-178">0x0466</span></span>
</dt> <dt>



<span data-ttu-id="755a8-179">MIPS</span><span class="sxs-lookup"><span data-stu-id="755a8-179">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**圖像 \_ 檔 \_ 機器 \_ AXP64**</span><span class="sxs-lookup"><span data-stu-id="755a8-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**IMAGE\_FILE\_MACHINE\_AXP64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-181">0x0284</span><span class="sxs-lookup"><span data-stu-id="755a8-181">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="755a8-182">AXP64</span><span class="sxs-lookup"><span data-stu-id="755a8-182">AXP64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**圖像 \_ 檔 \_ 機器 \_ TRICORE**</span><span class="sxs-lookup"><span data-stu-id="755a8-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**IMAGE\_FILE\_MACHINE\_TRICORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-184">0x0520</span><span class="sxs-lookup"><span data-stu-id="755a8-184">0x0520</span></span>
</dt> <dt>



<span data-ttu-id="755a8-185">恒</span><span class="sxs-lookup"><span data-stu-id="755a8-185">Infineon</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**圖像 \_ 檔 \_ 機器 \_ CEF**</span><span class="sxs-lookup"><span data-stu-id="755a8-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**IMAGE\_FILE\_MACHINE\_CEF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-187">0x0CEF</span><span class="sxs-lookup"><span data-stu-id="755a8-187">0x0CEF</span></span>
</dt> <dt>



<span data-ttu-id="755a8-188">Cef</span><span class="sxs-lookup"><span data-stu-id="755a8-188">CEF</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**圖像 \_ 檔 \_ 機器 \_ EBC**</span><span class="sxs-lookup"><span data-stu-id="755a8-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**IMAGE\_FILE\_MACHINE\_EBC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-190">0x0EBC</span><span class="sxs-lookup"><span data-stu-id="755a8-190">0x0EBC</span></span>
</dt> <dt>



<span data-ttu-id="755a8-191">EFI 位元組碼</span><span class="sxs-lookup"><span data-stu-id="755a8-191">EFI Byte Code</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**圖像 \_ 檔 \_ 電腦 \_ AMD64**</span><span class="sxs-lookup"><span data-stu-id="755a8-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**IMAGE\_FILE\_MACHINE\_AMD64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-193">0x8664</span><span class="sxs-lookup"><span data-stu-id="755a8-193">0x8664</span></span>
</dt> <dt>



<span data-ttu-id="755a8-194">AMD64 (K8) </span><span class="sxs-lookup"><span data-stu-id="755a8-194">AMD64 (K8)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**圖像 \_ 檔 \_ 機器 \_ M32R**</span><span class="sxs-lookup"><span data-stu-id="755a8-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**IMAGE\_FILE\_MACHINE\_M32R**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-196">0x9041</span><span class="sxs-lookup"><span data-stu-id="755a8-196">0x9041</span></span>
</dt> <dt>



<span data-ttu-id="755a8-197">M32R 位元組由小到大</span><span class="sxs-lookup"><span data-stu-id="755a8-197">M32R little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**圖像 \_ 檔 \_ 機器 \_ ARM64**</span><span class="sxs-lookup"><span data-stu-id="755a8-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**IMAGE\_FILE\_MACHINE\_ARM64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-199">0xAA64</span><span class="sxs-lookup"><span data-stu-id="755a8-199">0xAA64</span></span>
</dt> <dt>



<span data-ttu-id="755a8-200">ARM64 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="755a8-200">ARM64 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="755a8-201">從 Windows 8.1 和 Windows Server 2012 R2 開始，可以使用這個常數。</span><span class="sxs-lookup"><span data-stu-id="755a8-201">This constant is available starting with Windows 8.1 and Windows Server 2012 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="755a8-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**圖像 \_ 檔 \_ 機器 \_ 產生 CEE**</span><span class="sxs-lookup"><span data-stu-id="755a8-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**IMAGE\_FILE\_MACHINE\_CEE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="755a8-203">0xC0EE</span><span class="sxs-lookup"><span data-stu-id="755a8-203">0xC0EE</span></span>
</dt> <dt>



<span data-ttu-id="755a8-204">CEE</span><span class="sxs-lookup"><span data-stu-id="755a8-204">CEE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="755a8-205">規格需求</span><span class="sxs-lookup"><span data-stu-id="755a8-205">Requirements</span></span>



| <span data-ttu-id="755a8-206">需求</span><span class="sxs-lookup"><span data-stu-id="755a8-206">Requirement</span></span> | <span data-ttu-id="755a8-207">值</span><span class="sxs-lookup"><span data-stu-id="755a8-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="755a8-208">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="755a8-208">Minimum supported client</span></span><br/> | <span data-ttu-id="755a8-209">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="755a8-209">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="755a8-210">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="755a8-210">Minimum supported server</span></span><br/> | <span data-ttu-id="755a8-211">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="755a8-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="755a8-212">標頭</span><span class="sxs-lookup"><span data-stu-id="755a8-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="755a8-213"><dt>Winnt。h</dt></span><span class="sxs-lookup"><span data-stu-id="755a8-213"><dt>Winnt.h</dt></span></span> </dl> |



 

 




