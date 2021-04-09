---
title: 'IVMNetworkAdapterCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬網路介面卡的集合。 若要取得 IVMNetworkAdapterCollection 物件，請使用 IVMVirtualMachine NetworkAdapters、IVMVirtualNetwork NetworkAdapters 和 IVMVirtualPC UnconnectedNetworkAdapters 屬性。
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- IVMNetworkAdapterCollection 介面 Virtual PC
- IVMNetworkAdapterCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025194"
---
# <a name="ivmnetworkadaptercollection-interface"></a>IVMNetworkAdapterCollection 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬網路介面卡的集合。 若要取得 IVMNetworkAdapterCollection 物件，請使用 [**IVMVirtualMachine：： NetworkAdapters**](ivmvirtualmachine-networkadapters.md)、 [**IVMVirtualNetwork：： NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)和 [**IVMVirtualPC：： UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) 屬性。

## <a name="members"></a>成員

**IVMNetworkAdapterCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMNetworkAdapterCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMNetworkAdapterCollection** 介面具有這些屬性。



| 屬性                                                             | 存取類型          | Description                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmnetworkadaptercollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                                                                  |
| [**計數**](ivmnetworkadaptercollection-count.md)<br/>        | 唯讀<br/> | 這個集合中的網路介面數目。<br/>                                               |
| [**項目**](ivmnetworkadaptercollection-item.md)<br/>          | 唯讀<br/> | 對應至指定之索引的 [**IVMNetworkAdapter**](ivmnetworkadapter.md) 物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                           |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                  |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection 定義為 ebaeafe9-ebcd-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> <dt>

[**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

