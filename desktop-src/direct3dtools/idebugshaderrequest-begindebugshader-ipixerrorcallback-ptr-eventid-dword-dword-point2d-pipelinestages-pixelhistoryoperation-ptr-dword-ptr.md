---
description: 針對指定的管線階段、圖元/頂點（如果適用、事件和框架）啟動著色器偵測會話的要求。
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest：： BeginDebugShader 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b6512dc8aa67b3f4d128be3cd2dcd2b622ba2035
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109256"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest：： BeginDebugShader 方法

針對指定的管線階段、圖元/頂點（如果適用、事件和框架）啟動著色器偵測會話的要求。

## <a name="syntax"></a>語法


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a>參數

*errorCallback*   
偵錯工具期間可能發生的錯誤回呼位址。

*eventID*   
指定的事件。

*frameNumber*   
指定的框架。

*頂點*   
指定的頂點。 只適用于對頂點著色器進行調試時。

*圖元*   
指定的圖元。 只適用于對圖元著色器進行調試時。

*階段*   
指定的管線階段。

*pPixelHistory*   
用來尋找關聯圖元以進行 debug 的圖元歷程記錄結果位址。 只適用于對圖元著色器進行調試時。

*pDevice*   
要傳遞至偵測引擎以便與此 (的偵測引擎進行通訊的位址) 的 readprocessmemory debug engine。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IDebugShaderRequest**](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
