---
title: 'IVMGuestOS ServicePackMinor 屬性 (VPCCOMInterfaces .h) '
description: 虛擬機器中執行之客體作業系統的 service pack 次要版本。
ms.assetid: f1413b5a-6a74-42a6-9671-b00b7c8912fa
keywords:
- ServicePackMinor 屬性 Virtual PC
- ServicePackMinor 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，ServicePackMinor 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.ServicePackMinor
- IVMGuestOS.get_ServicePackMinor
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e35562c3648281cfee96aacbfc4fc6a9ede23139da92444a5fac41e9a02e9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938783"
---
# <a name="ivmguestosservicepackminor-property"></a>IVMGuestOS：： ServicePackMinor 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

虛擬機器中執行之客體作業系統的 service pack 次要版本。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_ServicePackMinor(
  [out, retval] BSTR *servicePackMinor
);
```



## <a name="property-value"></a>屬性值

已安裝最新 Service Pack 的次要版本號碼。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                       | 意義                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                          | 作業成功。<br/>                        |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                            | 參數為 **Null**。<br/>                           |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl>               | VM 未執行。<br/>                               |
| <dl> <dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt> </dl> | 此 VM 中未安裝整合元件。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                    | 已發生未預期的錯誤。<br/>                    |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

