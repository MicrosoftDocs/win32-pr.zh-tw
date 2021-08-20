---
title: 'IVMVirtualNetwork HostAdapter 屬性 (VPCCOMInterfaces .h) '
description: 虛擬網路連線的介面卡名稱。
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- HostAdapter 屬性 Virtual PC
- HostAdapter 屬性 Virtual PC，IVMVirtualNetwork 介面
- IVMVirtualNetwork 介面 Virtual PC，HostAdapter 屬性
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72db5d8349572b2bd3549c2ee54d20e994bdfe8aed6ba0fbe31875e04f6942f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122678"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a>IVMVirtualNetwork：： HostAdapter 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取虛擬網路所連接的介面卡名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a>屬性值

虛擬網路所連接之主機介面卡的名稱。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                            | 意義                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                               | 作業成功。<br/>                                                                                                                              |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                 | 參數為 **Null**。<br/>                                                                                                                                 |
| <dl> <dt>VM \_\_ \_ \_ 找不到電子 ADAPTER</dt> <dt>0xA0040700</dt> </dl> | 此虛擬網路連線的主機乙太網路介面卡已無法再使用。 主機乙太網路介面卡可能已移除或停用。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>         | 已發生未預期的錯誤。<br/>                                                                                                                          |



## <a name="remarks"></a>備註

虛擬網路介面卡可讓虛擬網路與外部網路通訊。 在主機電腦上安裝的每個乙太網路介面卡通常都有一個介面卡。 例如，假設主機電腦有一個標示為 "10/100 ENET" 的介面卡。 若要將虛擬 NIC 連線到連接至 "10/100 ENET" 的網路，請將虛擬網路的 Network **HostAdapter** 屬性設定為 "10/100 ENET"，並將虛擬 nic 連線到此虛擬網路。

如果 **HostAdapter** 屬性設定為空字串 ( "" ) ，虛擬 NIC 介面卡會連線到「內部網路」或「共用網路 (NAT) 」網路。 連接至「內部網路」網路的虛擬 Nic 將無法存取系統主機上的外部網路。 不過，連接到此虛擬網路的虛擬 Nic 仍可彼此通訊。

您可以透過 [**IVMHostInfo：： NetworkAdapters**](ivmhostinfo-networkadapters.md) 屬性來存取完整的介面卡清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork 定義為431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

