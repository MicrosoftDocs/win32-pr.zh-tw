---
description: IWiaUIExtension 介面提供的方法可取代預設系統使用者介面、提供自訂裝置點陣圖標誌，以及提供自訂裝置圖示。
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: 'IWiaUIExtension 介面 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: f2b83a1cd2638489ef0cf1a635ab32619597c395f0ca9b41d2ffaed80f59c228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034929"
---
# <a name="iwiauiextension-interface"></a>IWiaUIExtension 介面

**IWiaUIExtension** 介面提供的方法可取代預設系統使用者介面、提供自訂裝置點陣圖標誌，以及提供自訂裝置圖示。

## <a name="members"></a>成員

**IWiaUIExtension** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaUIExtension** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaUIExtension** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**DeviceDialog**](-wia-iwiauiextension-devicedialog.md)               | 提供可取代預設系統使用者介面的自訂使用者介面。<br/> |
| [**GetDeviceBitmapLogo**](-wia-iwiauiextension-getdevicebitmaplogo.md) | 取得裝置的自訂點陣圖標誌。<br/>                                         |
| [**GetDeviceIcon**](-wia-iwiauiextension-getdeviceicon.md)             | 取得自訂裝置圖示。<br/>                                                        |



 

## <a name="remarks"></a>備註



| IUnknown 方法                                        | 描述                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | 傳回受支援介面的指標。 |
| [IUnknown：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | 遞增參考次數。               |
| [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | 遞減參考次數。               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wiadevd。h</dt> </dl> |



 

 
