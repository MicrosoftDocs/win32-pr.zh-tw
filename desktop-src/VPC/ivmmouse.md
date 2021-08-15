---
title: 'IVMMouse 介面 (VPCCOMInterfaces .h) '
description: 控制 VM 內的滑鼠裝置。
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- IVMMouse 介面 Virtual PC
- IVMMouse 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912365065b639f3c970390746c8e23ae1fc33648ecdf14278365290c503da26d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998848"
---
# <a name="ivmmouse-interface"></a>IVMMouse 介面

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

控制虛擬機器 (VM) 內的滑鼠裝置。 您可以使用 [**IVMVirtualMachine：：滑鼠**](ivmvirtualmachine-mouse.md)屬性來抓取虛擬機器的 **IVMMouse** 。 滑鼠裝置的座標可以用絕對座標或 delta 座標表示。 您可以使用 [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) 屬性來區別兩個座標標記法。 請注意，只有在客體作業系統已安裝整合元件時，才支援抓取目前的資料指標位置和絕對座標的使用。

## <a name="members"></a>成員

**IVMMouse** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMMouse** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMMouse** 介面具有這些方法。



| 方法                                  | 描述                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [**按一下**](ivmmouse-click.md)         | 模擬滑鼠按鍵的點擊。<br/>                                         |
| [**GetButton**](ivmmouse-getbutton.md) | 抓取所指定滑鼠按鍵的目前狀態 (向上或向下) 。<br/> |
| [**SetButton**](ivmmouse-setbutton.md) | 將目前狀態 () 指定的滑鼠按鍵。<br/>      |



 

### <a name="properties"></a>屬性

**IVMMouse** 介面具有這些屬性。



| 屬性                                                                         | 存取類型           | Description                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [**HorizontalPosition**](ivmmouse-horizontalposition.md)<br/>             | 讀取/寫入<br/> | 滑鼠的絕對 x 座標。<br/>                                         |
| [**ScrollWheelPosition**](ivmmouse-scrollwheelposition.md)<br/>           | 唯寫<br/> | 滑鼠 (相對於) 的 z 座標。<br/>                                  |
| [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md)<br/> | 讀取/寫入<br/> | 指出滑鼠座標是否代表絕對或相對座標。<br/> |
| [**VerticalPosition**](ivmmouse-verticalposition.md)<br/>                 | 讀取/寫入<br/> | 滑鼠的絕對 y 座標。<br/>                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse 定義為 ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



 

