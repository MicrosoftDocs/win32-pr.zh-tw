---
title: 'IVMHardDisk Type 屬性 (VPCCOMInterfaces .h) '
description: 虛擬硬碟的類型。
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- 類型虛擬電腦
- Type property Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，Type 屬性
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39c2ba462496f6791d129918b93401c971b755ef40c40ef9a1177059dc7bcce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998928"
---
# <a name="ivmharddisktype-property"></a>IVMHardDisk：： Type 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

捕獲虛擬硬碟的類型。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a>屬性值

目前硬碟映射的類型。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                               | 意義                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                  |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                                    | 參數為 **Null**。<br/>                                                     |
| <dl> <dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt> </dl> | 找不到目前的硬碟影像檔案。<br/>                           |
| <dl> <dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt> </dl>                         | 目前硬碟映射的類型無效。<br/>                            |
| <dl> <dt>VM \_E \_ HD \_ 映射 \_ 開啟 \_ 失敗</dt> <dt>0xA004067C</dt> </dl>                  | 嘗試開啟目前的硬碟影像檔案時發生錯誤。<br/>   |
| <dl> <dt>VM \_電子 \_ HD \_ 影像 \_ 存取</dt> <dt>0xA0040681</dt> </dl>                      | 嘗試存取目前的硬碟影像檔案時發生錯誤。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                              |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

