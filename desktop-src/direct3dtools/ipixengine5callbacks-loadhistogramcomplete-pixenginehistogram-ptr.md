---
description: 當長條圖載入已完成時，用來通知主機的回呼函式。
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadHistogramComplete\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks：： LoadHistogramComplete 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A72DB49E-06C8-4061-9872-C4380D90EEB2
api_name:
- IPixEngine5Callbacks.LoadHistogramComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4ca80f705b9d3761cb08410224ad9942af040103
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624504"
---
# <a name="span-idvspixengineipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptrspanipixengine5callbacksloadhistogramcomplete-method"></a><span id="vspixengine.ipixengine5callbacks_loadhistogramcomplete_pixenginehistogram_ptr"></span>IPixEngine5Callbacks：： LoadHistogramComplete 方法

當長條圖載入已完成時，用來通知主機的回呼函式。

## <a name="syntax"></a>語法


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>參數

*長條圖*   
已載入長條圖的長條圖資料位址。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
