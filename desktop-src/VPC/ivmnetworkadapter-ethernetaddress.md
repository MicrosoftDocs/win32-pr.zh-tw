---
title: 'IVMNetworkAdapter EthernetAddress 屬性 (VPCCOMInterfaces .h) '
description: 網路介面的乙太網路 (MAC) 位址。
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- EthernetAddress 屬性 Virtual PC
- EthernetAddress 屬性 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，EthernetAddress 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685472"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a>IVMNetworkAdapter：： EthernetAddress 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取並設定網路介面的 Ethernet (MAC) 位址。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a>屬性值

虛擬 NIC 的 MAC 位址。 它的格式應該是「*xx* xx xx xx xx xx」 -  -  -  -  - **，其中每個 *X* 都是十六進位數位。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                         | 意義                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ 確定</dt> </dl>                                                                                                   | 作業成功。<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                              | 參數為 **Null**。<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>E \_INVALIDARG</dt> <dt>0x80000003</dt> </dl>                           | 參數的格式不正確。<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>VM \_E \_ 無法 \_ 設定 \_ 動態 \_ MAC \_ 位址</dt> <dt>0xA004070A</dt> </dl> | 網路介面的乙太網路位址可以動態產生，也可以由使用者設定為靜態位址。 當地址設定為動態產生時，無法呼叫這個方法。 [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)屬性是用來變更乙太網路位址的產生行為。<br/> |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>                      | 找不到虛擬機器。 如果在建立 [**IVMNetworkAdapter**](ivmnetworkadapter.md) 物件之後移除電腦，就可能發生這種情況。<br/>                                                                                                                                                                                                                        |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                      | 已發生未預期的錯誤。<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

