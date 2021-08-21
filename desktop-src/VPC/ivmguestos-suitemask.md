---
title: 'IVMGuestOS SuiteMask 屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器中執行的客體作業系統 SuiteMask。
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- SuiteMask 屬性 Virtual PC
- SuiteMask 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，SuiteMask 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22075c68ef30fda7360f25e76c84dbffbf7e306335a0ef20bda45559cb6dac09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472290"
---
# <a name="ivmguestossuitemask-property"></a>IVMGuestOS：： SuiteMask 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取虛擬機器中執行的客體作業系統 SuiteMask。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a>屬性值

套件遮罩。 以下是支援的字串值。



| 值                                                                                   | 意義                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000004</dt> </dl> | 已安裝 Microsoft BackOffice 元件。<br/>                                                                                                              |
| <dl> <dt>"0x00000400"</dt> </dl> | Windows伺服器2003，Web Edition 已安裝。<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | Windows已安裝 Server 2003、Compute Cluster Edition。<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | Windows已安裝 Server 2008 R2 datacenter、Windows server 2008 datacenter、Windows Server 2003、Datacenter Edition 或 Windows 2000 Datacenter Server。<br/> |
| <dl> <dt>0x00000002</dt> </dl> | Windows已安裝 server 2008 R2 Enterprise、Windows server 2008 Enterprise、Windows Server 2003、Enterprise Edition 或 Windows 2000 Advanced Server。<br/>   |
| <dl> <dt>0x00000040</dt> </dl> | Windows已安裝 XP Embedded。<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | Windowsvista home 進階版、Windows vista home Basic 或 Windows XP home Edition 皆已安裝。<br/>                                                              |
| <dl> <dt>0x00000100</dt> </dl> | 支援遠端桌面，但只支援一個互動式會話。<br/>                                                                                 |
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server 已安裝在系統上，但可能已升級至另一個版本的 Windows。<br/>                                 |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server 會以強制的嚴格用戶端授權安裝。<br/>                                                                  |
| <dl> <dt>0x00002000</dt> </dl> | 已安裝 Windows 儲存體 server 2003 R2 或 Windows 儲存體 server 2003。<br/>                                                                                 |
| <dl> <dt>0x00000010</dt> </dl> | 已安裝遠端桌面服務。 一律會設定這個值。<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | Windows已安裝 Home Server。<br/>                                                                                                                           |



 

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

 

