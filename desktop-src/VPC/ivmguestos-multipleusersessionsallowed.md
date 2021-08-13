---
title: IVMGuestOS MultipleUserSessionsAllowed 屬性
description: 判斷客體作業系統中是否允許多個並行使用者會話。
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- MultipleUserSessionsAllowed 屬性 Virtual PC
- MultipleUserSessionsAllowed 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，MultipleUserSessionsAllowed 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68075c13cfc65b79d992b849b310bd3c88b09f7901567baf249bff15496ede05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594071"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a>IVMGuestOS：： MultipleUserSessionsAllowed 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

判斷客體作業系統中是否允許多個並行使用者會話。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a>屬性值

**變異 \_** 如果客體作業系統允許多個並行使用者會話，則為 TRUE，**否則 \_ 為 VARIANT** 。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                       | 意義                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                          | 作業成功。<br/>                                                                                       |
| <dl> <dt>S \_FALSE</dt> <dt>1</dt> </dl>                                       | 先前稱為終端機服務) 的遠端桌面服務 (尚未在客體作業系統中初始化。<br/> |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                            | *SessionStatus* 參數為 **Null**。<br/>                                                                          |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl>               | 虛擬機器未執行。<br/>                                                                                 |
| <dl> <dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt> </dl> | 此虛擬機器中未安裝整合元件。<br/>                                                   |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                    | 已發生未預期的錯誤。<br/>                                                                                   |



## <a name="remarks"></a>備註

除非 [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) 屬性為 **VARIANT \_ TRUE**，否則這個屬性的值無效。

針對 Windows 用戶端作業系統，如果支援快速使用者切換，則 **MultipleUserSessionsAllowed** 為 **VARIANT \_** 。 針對 Windows Server 作業系統，如果已安裝並啟用遠端桌面服務 (之前稱為「終端機) 服務」，則 **MultipleUserSessionsAllowed** 是 **VARIANT \_** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                 |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                      |
| Idl<br/>                      | <dl> <dt>IVMGuestOS .idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

