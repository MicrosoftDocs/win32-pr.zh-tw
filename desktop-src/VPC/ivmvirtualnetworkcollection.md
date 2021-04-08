---
title: 'IVMVirtualNetworkCollection 介面 (VPCCOMInterfaces .h) '
description: 定義 IVMVirtualNetwork 物件的集合。 若要取得 IVMVirtualNetworkCollection 物件，請使用 IVMVirtualPC VirtualNetworks 屬性。
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- IVMVirtualNetworkCollection 介面 Virtual PC
- IVMVirtualNetworkCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686303"
---
# <a name="ivmvirtualnetworkcollection-interface"></a>IVMVirtualNetworkCollection 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義 [**IVMVirtualNetwork**](ivmvirtualnetwork.md) 物件的集合。 若要取得 **IVMVirtualNetworkCollection** 物件，請使用 [**IVMVirtualPC：： VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) 屬性。

## <a name="members"></a>成員

**IVMVirtualNetworkCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMVirtualNetworkCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMVirtualNetworkCollection** 介面具有這些屬性。



| 屬性                                                             | 存取類型          | Description                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualnetworkcollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                                                                  |
| [**計數**](ivmvirtualnetworkcollection-count.md)<br/>        | 唯讀<br/> | 此集合中的虛擬網路數目。<br/>                                                 |
| [**項目**](ivmvirtualnetworkcollection-item.md)<br/>          | 唯讀<br/> | 對應至指定之索引的 [**IVMVirtualNetwork**](ivmvirtualnetwork.md) 物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                           |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                  |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection 定義為8ed680be-4242-4b2a-a21c-1982d8b0f675<br/> |



 

