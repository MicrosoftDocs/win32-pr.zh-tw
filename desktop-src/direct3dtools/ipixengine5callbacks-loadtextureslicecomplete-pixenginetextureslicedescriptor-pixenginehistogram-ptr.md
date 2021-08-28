---
description: 當材質配量載入已完成時，用來通知主機的回呼函式。
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureSliceComplete\_PixEngineTextureSliceDescriptor\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks：： LoadTextureSliceComplete 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CEEAB77F-0856-4DEC-991A-7CEB921C84BB
api_name:
- IPixEngine5Callbacks.LoadTextureSliceComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93ad2b73c1d139aeacd23bb62df63b8393e6e695
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627104"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptrspanipixengine5callbacksloadtextureslicecomplete-method"></a><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks：： LoadTextureSliceComplete 方法

當材質配量載入已完成時，用來通知主機的回呼函式。

## <a name="syntax"></a>語法


```C++
HRESULT LoadTextureSliceComplete(
   PixEngineTextureSliceDescriptor sliceDesc,
   PixEngineHistogram*             histogram
);
```

## <a name="parameters"></a>參數

*sliceDesc*   
已載入之配量的描述項。

*長條圖*   
已載入之配量的長條圖資料位址。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
