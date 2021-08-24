---
description: ISampleGrabber 介面是由範例捕獲篩選器所公開。 它可讓應用程式在整個篩選圖形中移動時，取得個別的媒體範例。
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: 'ISampleGrabber 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 485301d58da6ca48bf43414fd9907048943ab8868c514132e2887fef29e5d2b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817642"
---
# <a name="isamplegrabber-interface"></a>ISampleGrabber 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

**ISampleGrabber** 介面是由 [**範例捕獲**](sample-grabber-filter.md)篩選器所公開。 它可讓應用程式在整個篩選圖形中移動時，取得個別的媒體範例。

## <a name="members"></a>成員

**ISampleGrabber** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ISampleGrabber** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISampleGrabber** 介面具有這些方法。



| 方法                                                                | 描述                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) | 抓取範例抓取之輸入 pin 的連接媒體類型。<br/>                                        |
| [**GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)           | 抓取篩選器最近收到的範例複本。<br/>                                                 |
| [**GetCurrentSample**](isamplegrabber-getcurrentsample.md)           | 未實作。<br/>                                                                                                       |
| [**SetBufferSamples**](isamplegrabber-setbuffersamples.md)           | 指定是否在通過篩選時，將範例資料複製到緩衝區。<br/>                                     |
| [**SetCallback**](isamplegrabber-setcallback.md)                     | 指定要對傳入範例呼叫的回呼方法。<br/>                                                               |
| [**SetMediaType**](isamplegrabber-setmediatype.md)                   | 在範例抓取程式的輸入釘選上指定連接的媒體類型。<br/>                                    |
| [**SetOneShot**](isamplegrabber-setoneshot.md)                       | 指定 [**範例**](sample-grabber-filter.md) 抓取篩選器是否會在篩選器收到範例後停止。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用範例捕獲](using-the-sample-grabber.md)
</dt> </dl>

 

 
