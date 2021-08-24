---
title: 'IVMHardDisk SizeInGuest 屬性 (VPCCOMInterfaces .h) '
description: 抓取客體作業系統中虛擬硬碟的大小。
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- SizeInGuest 屬性 Virtual PC
- SizeInGuest 屬性 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，SizeInGuest 屬性
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efbdcf9f5aa60a8dfdce9c71de745e0567995b90df13ffd39b5969689de099c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653288"
---
# <a name="ivmharddisksizeinguest-property"></a>IVMHardDisk：： SizeInGuest 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取客體作業系統中虛擬硬碟的大小。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>屬性值

硬碟影像的大小（以位元組為單位）。 此值為 VT  DECIMAL 類型的變數 \_ 。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                               | 意義                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                  |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                                    | 參數為 **Null**。<br/>                                                     |
| <dl> <dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt> </dl> | 找不到目前的虛擬硬碟檔案。<br/>                         |
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

 

