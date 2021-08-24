---
title: 'IVMDisplay 介面 (VPCCOMInterfaces .h) '
description: 控制虛擬機器的顯示設定。 您可以使用 IVMVirtualMachine 顯示內容來抓取虛擬機器的 IVMDisplay 介面。
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- IVMDisplay 介面 Virtual PC
- IVMDisplay 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6239747477cdddf0ecbcf3acac90e33e61c0f5f4c9dd327b80eb6a33cb113c32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654138"
---
# <a name="ivmdisplay-interface"></a>IVMDisplay 介面

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

控制虛擬機器的顯示設定。 您可以使用 [**IVMVirtualMachine：:D isplay**](ivmvirtualmachine-display.md)屬性來抓取虛擬機器的 **IVMDisplay** 介面。

## <a name="members"></a>成員

**IVMDisplay** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMDisplay** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMDisplay** 介面具有這些方法。



| 方法                                                       | 描述                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) | 抓取圖元的陣列，表示虛擬機器畫面的縮圖影像。<br/> |
| [**SetDimensions**](ivmdisplay-setdimensions.md)            | 設定虛擬機器顯示的高度和寬度（以圖元為單位）。<br/>                       |



 

### <a name="properties"></a>屬性

**IVMDisplay** 介面具有這些屬性。



| 屬性                                             | 存取類型          | 描述                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**Graphicswindow.canresize**](ivmdisplay-canresize.md)<br/> | 唯讀<br/> | 指出來賓是否允許解析變更。<br/>                             |
| [**高度**](ivmdisplay-height.md)<br/>       | 唯讀<br/> | 虛擬機器的顯示高度（以圖元為單位）。<br/>                            |
| [**縮圖**](ivmdisplay-thumbnail.md)<br/> | 唯讀<br/> | 圖元的陣列，表示虛擬機器畫面的縮圖影像。<br/> |
| [**VideoMode**](ivmdisplay-videomode.md)<br/> | 唯讀<br/> | 目前的影片模式 (文字、VGA、SVGA 等) 。<br/>                               |
| [**寬度**](ivmdisplay-width.md)<br/>         | 唯讀<br/> | 虛擬機器的顯示寬度（以圖元為單位）。<br/>                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



 

