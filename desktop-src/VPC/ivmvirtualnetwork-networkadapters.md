---
title: 'IVMVirtualNetwork NetworkAdapters 屬性 (VPCCOMInterfaces .h) '
description: 抓取連接至虛擬網路之 Nic 的可列舉集合。
ms.assetid: d5b95831-4642-441e-93e8-34e125087a43
keywords:
- NetworkAdapters 屬性 Virtual PC
- NetworkAdapters 屬性 Virtual PC，IVMVirtualNetwork 介面
- IVMVirtualNetwork 介面 Virtual PC，NetworkAdapters 屬性
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.NetworkAdapters
- IVMVirtualNetwork.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cbcf6a4c1f4aeb5f7c16d1e3a25a0081e664f0b3d71708fd85c6b457acb1b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122628"
---
# <a name="ivmvirtualnetworknetworkadapters-property"></a>IVMVirtualNetwork：： NetworkAdapters 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取連接至虛擬網路之 Nic 的可列舉集合。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkInterfaceCollection
);
```



## <a name="property-value"></a>屬性值

新的 [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) ，其中包含連接到此虛擬網路的虛擬 nic。

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
| IID<br/>                      | IID \_ IVMVirtualNetwork 定義為431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

