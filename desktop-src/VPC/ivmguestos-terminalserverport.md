---
title: IVMGuestOS TerminalServerPort 屬性
description: 客體作業系統中遠端桌面服務所使用的埠。
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- TerminalServerPort 屬性 Virtual PC
- TerminalServerPort 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，TerminalServerPort 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b9eea5c545613f05dbd828a9436175fab6bfc5a05ba2fe5f59588f78da913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512158"
---
# <a name="ivmguestosterminalserverport-property"></a>IVMGuestOS：： TerminalServerPort 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

遠端桌面服務的埠 (之前稱為「終端機服務」，可在客體作業系統中) 。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a>屬性值

傳回客體作業系統中遠端桌面服務所使用的埠。



| 值                                                                              | 意義                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>3389</dt> </dl>    | 預設值<br/>                      |
| <dl> <dt>1 65535</dt> </dl> | 有效範圍<br/>                        |
| <dl> <dt>0</dt> </dl>       | 無法使用有效的埠值。<br/> |



 

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                       | 意義                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                          | 作業成功。<br/>                                                 |
| <dl> <dt>S \_FALSE</dt> <dt>1</dt> </dl>                                       | 遠端桌面服務尚未在客體作業系統中初始化。<br/> |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                            | *TsPort* 參數為 **Null**。<br/>                                           |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl>               | 虛擬機器未執行。<br/>                                           |
| <dl> <dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt> </dl> | 此虛擬機器中未安裝整合元件。<br/>             |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                    | 已發生未預期的錯誤。<br/>                                             |



## <a name="remarks"></a>備註

除非 [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) 屬性為 **VARIANT \_ TRUE**，否則這個屬性的值無效。

如果 [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) 屬性由於埠上的連接錯誤而成為 **VARIANT \_ FALSE** ，則 **TerminalServerPort** 屬性所傳回的值會包含錯誤值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                 |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                      |
| IDL<br/>                      | <dl> <dt>IVMGuestOS .idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

