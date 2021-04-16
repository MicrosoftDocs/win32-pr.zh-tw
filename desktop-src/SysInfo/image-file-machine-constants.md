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
# <a name="image-file-machine-constants"></a>影像檔案電腦常數

描述可能的電腦架構。 用於 [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a)、 [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) 和 [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2)。

<dl> <dt>

<span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**圖像 \_ 檔 \_ 電腦 \_ 不明**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Unknown


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**圖像 \_ 檔 \_ 電腦 \_ 目標 \_ 主機**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



與主機互動，而不是 WOW64 來賓

> [!Note]  
> 從 Windows 10、1607版和 Windows Server 2016 開始，可以使用這個常數。

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**圖像 \_ 檔 \_ 機器 \_ I386**
</dt> <dd> <dl> <dt>

0x014c
</dt> <dt>



Intel 386


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**圖像 \_ 檔 \_ 機器 \_ R3000**
</dt> <dd> <dl> <dt>

0x0162
</dt> <dt>



MIPS 位元組由小到大、0x160 位元組由大到小


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**圖像 \_ 檔 \_ 機器 \_ R4000**
</dt> <dd> <dl> <dt>

0x0166
</dt> <dt>



MIPS 小位元組由小到大


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**圖像 \_ 檔 \_ 機器 \_ R10000**
</dt> <dd> <dl> <dt>

0x0168
</dt> <dt>



MIPS 小位元組由小到大


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**圖像 \_ 檔 \_ 機器 \_ WCEMIPSV2**
</dt> <dd> <dl> <dt>

0x0169
</dt> <dt>



MIPS 位元組由小到小 WCE v2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**圖像 \_ 檔 \_ 電腦 \_ ALPHA**
</dt> <dd> <dl> <dt>

0x0184
</dt> <dt>



Alpha \_ AXP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**圖像 \_ 檔 \_ 機器 \_ SH3**
</dt> <dd> <dl> <dt>

0x01a2
</dt> <dt>



SH3 位元組由小到大


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**圖像 \_ 檔 \_ 機器 \_ SH3DSP**
</dt> <dd> <dl> <dt>

0x01a3
</dt> <dt>



SH3DSP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**圖像 \_ 檔 \_ 機器 \_ SH3E**
</dt> <dd> <dl> <dt>

0x01a4
</dt> <dt>



SH3E 位元組由小到大


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**圖像 \_ 檔 \_ 機器 \_ SH4**
</dt> <dd> <dl> <dt>

0x01a6
</dt> <dt>



SH4 位元組由小到大


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**圖像 \_ 檔 \_ 機器 \_ SH5**
</dt> <dd> <dl> <dt>

0x01a8
</dt> <dt>



SH5


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**圖像 \_ 檔 \_ 機器 \_ ARM**
</dt> <dd> <dl> <dt>

0x01c0
</dt> <dt>



ARM Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**圖像 \_ 檔 \_ 機器 \_ 經驗**
</dt> <dd> <dl> <dt>

0x01c2
</dt> <dt>



ARM Thumb/Thumb-2 Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**圖像 \_ 檔 \_ 機器 \_ ARMNT**
</dt> <dd> <dl> <dt>

0x01c4
</dt> <dt>



ARM Thumb-2 Little-Endian

> [!Note]  
> 從 Windows 7 和 Windows Server 2008 R2 開始，可以使用這個常數。

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**圖像 \_ 檔 \_ 機器 \_ AM33**
</dt> <dd> <dl> <dt>

0x01d3
</dt> <dt>



TAM33BD


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**圖像 \_ 檔 \_ 機器 \_ POWERPC**
</dt> <dd> <dl> <dt>

0x01F0
</dt> <dt>



IBM PowerPC Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**圖像 \_ 檔 \_ 機器 \_ POWERPCFP**
</dt> <dd> <dl> <dt>

0x01f1
</dt> <dt>



POWERPCFP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**圖像 \_ 檔案 \_ 電腦 \_ IA64**
</dt> <dd> <dl> <dt>

0x0200
</dt> <dt>



Intel 64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**圖像 \_ 檔 \_ 機器 \_ MIPS16**
</dt> <dd> <dl> <dt>

0x0266
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**圖像 \_ 檔 \_ 機器 \_ ALPHA64**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



ALPHA64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**圖像 \_ 檔 \_ 機器 \_ MIPSFPU**
</dt> <dd> <dl> <dt>

0x0366
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**圖像 \_ 檔 \_ 機器 \_ MIPSFPU16**
</dt> <dd> <dl> <dt>

0x0466
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**圖像 \_ 檔 \_ 機器 \_ AXP64**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



AXP64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**圖像 \_ 檔 \_ 機器 \_ TRICORE**
</dt> <dd> <dl> <dt>

0x0520
</dt> <dt>



恒


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**圖像 \_ 檔 \_ 機器 \_ CEF**
</dt> <dd> <dl> <dt>

0x0CEF
</dt> <dt>



Cef


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**圖像 \_ 檔 \_ 機器 \_ EBC**
</dt> <dd> <dl> <dt>

0x0EBC
</dt> <dt>



EFI 位元組碼


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**圖像 \_ 檔 \_ 電腦 \_ AMD64**
</dt> <dd> <dl> <dt>

0x8664
</dt> <dt>



AMD64 (K8) 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**圖像 \_ 檔 \_ 機器 \_ M32R**
</dt> <dd> <dl> <dt>

0x9041
</dt> <dt>



M32R 位元組由小到大


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**圖像 \_ 檔 \_ 機器 \_ ARM64**
</dt> <dd> <dl> <dt>

0xAA64
</dt> <dt>



ARM64 Little-Endian

> [!Note]  
> 從 Windows 8.1 和 Windows Server 2012 R2 開始，可以使用這個常數。

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**圖像 \_ 檔 \_ 機器 \_ 產生 CEE**
</dt> <dd> <dl> <dt>

0xC0EE
</dt> <dt>



CEE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Winnt。h</dt> </dl> |



 

 




