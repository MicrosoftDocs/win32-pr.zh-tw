---
title: 'IVMHostInfo FloppyDrives 屬性 (VPCCOMInterfaces .h) '
description: 抓取與主機軟碟磁碟機相關聯的磁碟機號。
ms.assetid: 9a8ab4b5-6ee8-463f-809b-b88cd28d9373
keywords:
- FloppyDrives 屬性 Virtual PC
- FloppyDrives 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，FloppyDrives 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.FloppyDrives
- IVMHostInfo.get_FloppyDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bb15927a528ce6ab8910caad47a7b63f885847ae21f28eb62be843bed84523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345692"
---
# <a name="ivmhostinfofloppydrives-property"></a>IVMHostInfo：： FloppyDrives 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取與主機軟碟磁碟機相關聯的磁碟機號。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_FloppyDrives(
  [out, retval] VARIANT *floppyDrives
);
```



## <a name="property-value"></a>屬性值

磁碟機號的陣列。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>     |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>        |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

