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
ms.openlocfilehash: 2111c25a83a9b826f4cab7dba8f689e01a9868ac416b8fb3026f1b1fb49a90ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208141"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wiadevd。h</dt> </dl> |



 

 
