---
description: ISampleGrabberCB 介面提供 ISampleGrabber：： SetCallback 方法的回呼方法。 如果您的應用程式呼叫該方法，則必須執行這個介面。 如需詳細資訊，請參閱 ISampleGrabber。
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: 'ISampleGrabberCB 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994223"
---
# <a name="isamplegrabbercb-interface"></a>ISampleGrabberCB 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`ISampleGrabberCB`介面提供 [**ISampleGrabber：： SetCallback**](isamplegrabber-setcallback.md)方法的回呼方法。 如果您的應用程式呼叫該方法，則必須執行這個介面。 如需詳細資訊，請參閱 [**ISampleGrabber**](isamplegrabber.md)。

## <a name="members"></a>成員

**ISampleGrabberCB** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ISampleGrabberCB** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISampleGrabberCB** 介面具有這些方法。



| 方法                                        | 描述                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**BufferCB**](isamplegrabbercb-buffercb.md) | 回呼方法，這個方法會接收範例緩衝區的指標。<br/> |
| [**SampleCB**](isamplegrabbercb-samplecb.md) | 回呼方法，這個方法會接收媒體範例的指標。<br/>  |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
