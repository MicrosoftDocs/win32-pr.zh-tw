---
title: 'IVMVirtualNetwork 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬網路。
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- IVMVirtualNetwork 介面 Virtual PC
- IVMVirtualNetwork 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106972693"
---
# <a name="ivmvirtualnetwork-interface"></a>IVMVirtualNetwork 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬網路。 **IVMVirtualNetwork** 物件是從 [**IVMVirtualPC**](ivmvirtualpc.md) 方法 [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md)傳回。 您也可以從 [**IVMVirtualPC：： VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)屬性傳回的 [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)物件中取出 **IVMVirtualNetwork** 物件。

虛擬網路是由虛擬交換器所組成，它會執行所有的內部路由，以及數個「插入」至虛擬交換器的連接。 這些連線可以是真實的外部主機連線、「內部網路」或共用網路 (NAT) 。

## <a name="members"></a>成員

**IVMVirtualNetwork** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMVirtualNetwork** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMVirtualNetwork** 介面具有這些方法。



| 方法                                | 描述                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [**\_ID**](ivmvirtualnetwork--id.md) | 抓取虛擬網路的內部識別碼。<br/> |



 

### <a name="properties"></a>屬性

**IVMVirtualNetwork** 介面具有這些屬性。



| 屬性                                                                | 存取類型          | Description                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**HostAdapter**](ivmvirtualnetwork-hostadapter.md)<br/>         | 唯讀<br/> | 虛擬網路連線的介面卡名稱。<br/>  |
| [**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))<br/>             | 唯讀<br/> | 判斷虛擬網路實例是否為無線。<br/> |
| [**Name**](ivmvirtualnetwork-name.md)<br/>                       | 唯讀<br/> | 虛擬網路實例的唯一名稱。<br/>                    |
| [**NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)<br/> | 唯讀<br/> | 連接至虛擬網路之 Nic 的可列舉集合。<br/>   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork 定義為431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



 

