---
title: 'IVMGuestOS HeartbeatPercentage 屬性 (VPCCOMInterfaces .h) '
description: 過去一分鐘收到的預期心跳量百分比。
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- HeartbeatPercentage 屬性 Virtual PC
- HeartbeatPercentage 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，HeartbeatPercentage 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509256"
---
# <a name="ivmguestosheartbeatpercentage-property"></a>IVMGuestOS：： HeartbeatPercentage 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取過去一分鐘所收到的預期心跳量百分比。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a>屬性值

過去一分鐘收到的預期心跳量百分比。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                              | 意義                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                 | 作業成功。<br/>                                                                                                            |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                   | 參數為 **Null**。<br/>                                                                                                               |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>           | 未知的設定。<br/>                                                                                                            |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl>      | 虛擬機器 (VM) 必須針對此操作執行。<br/>                                                                             |
| <dl> <dt>VM \_E \_ 新增 \_ 專案 \_ 無法</dt> <dt>0xA0040504</dt> </dl> | VM 未完全啟動、未安裝整合元件功能，或安裝的版本不支援這項功能。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>           | 已發生未預期的錯誤。<br/>                                                                                                        |



## <a name="remarks"></a>備註

當客體作業系統正在執行時，整合元件會將週期性心跳傳送至 Windows Virtual PC。 如果虛擬作業系統的負載很高，Windows Virtual PC 可能會收到比預期更少的心跳。 如果心跳百分比降至零，表示客體作業系統可能沒有回應或損毀。 虛擬機器必須執行 (也就是，完全開機且未關閉) 而且必須在叫用這個屬性時安裝整合元件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

