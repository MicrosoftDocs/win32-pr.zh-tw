---
title: 'IVMHardDisk 介面 (VPCCOMInterfaces .h) '
description: 提供硬碟影像的存取。 您可以透過 IVMHardDiskConnection 硬碟屬性或 IVMVirtualPC GetHardDisk 方法來存取它。
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- IVMHardDisk 介面 Virtual PC
- IVMHardDisk 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464189"
---
# <a name="ivmharddisk-interface"></a>IVMHardDisk 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

提供硬碟影像的存取。 您可以透過 [**IVMHardDiskConnection：：硬碟**](ivmharddiskconnection-harddisk.md) 屬性或 [**IVMVirtualPC：： GetHardDisk**](ivmvirtualpc-getharddisk.md) 方法來存取它。

## <a name="members"></a>成員

**IVMHardDisk** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMHardDisk** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMHardDisk** 介面具有這些方法。



| 方法                                 | 描述                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**精簡**](ivmharddisk-compact.md) | 壓縮動態擴充的虛擬硬碟映射。<br/>                                                                                        |
| [**轉換**](ivmharddisk-convert.md) | 將任何虛擬硬碟轉換成動態擴充的虛擬硬碟或固定大小的虛擬硬碟。<br/>                            |
| [**合併**](ivmharddisk-merge.md)     | 合併差異虛擬硬碟與其父磁片映射。<br/>                                                                              |
| [**MergeTo**](ivmharddisk-mergeto.md) | 將差異虛擬硬碟與其所有父系合併 (（包括根父系虛擬硬碟) ）至新的硬碟檔案。<br/> |



 

### <a name="properties"></a>屬性

**IVMHardDisk** 介面具有這些屬性。



| 屬性                                                              | 存取類型           | Description                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**檔案**](ivmharddisk-file.md)<br/>                           | 唯讀<br/>  | 虛擬硬碟檔案的完整路徑名稱。<br/>                                   |
| [**HostFreeDiskSpace**](ivmharddisk-hostfreediskspace.md)<br/> | 唯讀<br/>  | 虛擬硬碟的主機上可用的剩餘磁碟空間量。<br/> |
| [**父代**](ivmharddisk-parent.md)<br/>                       | 讀取/寫入<br/> | 差異虛擬硬碟的父系。<br/>                                   |
| [**SizeInGuest**](ivmharddisk-sizeinguest.md)<br/>             | 唯讀<br/>  | 客體作業系統中的虛擬硬碟大小。<br/>                    |
| [**SizeOnHost**](ivmharddisk-sizeonhost.md)<br/>               | 唯讀<br/>  | 主機電腦上虛擬硬碟檔案的大小。<br/>                        |
| [**類型**](ivmharddisk-type.md)<br/>                           | 唯讀<br/>  | 虛擬硬碟的類型。<br/>                                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



 

