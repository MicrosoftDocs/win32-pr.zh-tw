---
title: 'IVMHardDisk HostFreeDiskSpace 屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬硬碟主機上的剩餘可用磁碟空間量。
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- HostFreeDiskSpace 屬性 Virtual PC
- HostFreeDiskSpace 屬性 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，HostFreeDiskSpace 屬性
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105810"
---
# <a name="ivmharddiskhostfreediskspace-property"></a>IVMHardDisk：： HostFreeDiskSpace 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取虛擬硬碟主機上的剩餘可用磁碟空間量。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a>屬性值

主機電腦上目前硬碟影像檔案的剩餘可用磁碟空間量。 此值為 VT  DECIMAL 類型的變數 \_ 。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                            | 意義                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                               | 作業成功。<br/>                                |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                                 | 參數為 **Null**。<br/>                                   |
| <dl> <dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤) </dt> <dt>0x800700a1</dt> </dl> | 目前虛擬硬碟檔案的路徑無效。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                         | 已發生未預期的錯誤。<br/>                            |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

