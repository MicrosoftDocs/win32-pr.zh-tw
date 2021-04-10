---
description: IWiaUIExtension2 介面提供的方法會將預設的系統提供的使用者介面取代為自訂的使用者介面，並提供自訂裝置圖示。
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: 'IWiaUIExtension2 介面 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943465"
---
# <a name="iwiauiextension2-interface"></a>IWiaUIExtension2 介面

IWiaUIExtension2 介面提供的方法會將預設的系統提供的使用者介面取代為自訂的使用者介面，並提供自訂裝置圖示。 裝置廠商可以執行此介面，為其裝置提供自訂使用者介面。

## <a name="members"></a>成員

**IWiaUIExtension2** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaUIExtension2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaUIExtension2** 介面具有這些方法。



| 方法                                                       | 描述                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**DeviceDialog**](-wia-iwiauiextension2-devicedialog.md)   | 提供可取代預設系統使用者介面的自訂使用者介面。<br/> |
| [**GetDeviceIcon**](-wia-iwiauiextension2-getdeviceicon.md) | 取得自訂裝置圖示。<br/>                                                        |



 

## <a name="remarks"></a>備註



| IUnknown 方法                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | 傳回受支援介面的指標。 |
| [IUnknown：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | 遞增參考次數。               |
| [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | 遞減參考次數。               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wiadevd。h</dt> </dl> |



 

 
