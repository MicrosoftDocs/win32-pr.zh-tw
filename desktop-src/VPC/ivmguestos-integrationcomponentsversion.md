---
title: 'IVMGuestOS IntegrationComponentsVersion 屬性 (VPCCOMInterfaces .h) '
description: 抓取在客體作業系統中安裝之整合元件的版本。
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- IntegrationComponentsVersion 屬性 Virtual PC
- IntegrationComponentsVersion 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，IntegrationComponentsVersion 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854cb86817f461085c72a437fa962649e50ab11b65a847d0756dc8e9c7b18177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999048"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a>IVMGuestOS：： IntegrationComponentsVersion 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取在客體作業系統中安裝之整合元件的版本。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a>屬性值

版本。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                              | 意義                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                 | 作業成功。<br/>                                                     |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                   | 參數為 **Null**。<br/>                                                        |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>           | 找不到虛擬機器 (VM) 。<br/>                                      |
| <dl> <dt>VM \_E \_ 新增 \_ 專案 \_ 無法</dt> <dt>0xA0040504</dt> </dl> | 此 VM 未安裝整合元件，或 VM 從未啟動。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>           | 已發生未預期的錯誤。<br/>                                                 |



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

 

