---
description: 用來指出如何拒絕圖元的列舉。
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PIXELKILLREASON 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58ead08f81c8dee1644e431ae100c5100551e9907ab9a9d5bf00f6aae3532abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119322"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>PIXELKILLREASON 列舉

用來指出如何拒絕圖元的列舉。

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>常數

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ 無**  
值，指出未拒絕圖元。

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**  
值，表示因為未執行著色器而拒絕圖元。

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**  
值，表示因為剪式測試失敗而拒絕圖元。

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**  
值，表示因為 Alpha 測試失敗而拒絕圖元。

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**  
值，表示因為樣板測試失敗而拒絕圖元。

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**  
值，表示因為深度測試失敗，所以已拒絕圖元。

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**  
值，表示無法計算圖元歷史記錄。

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR \_ 錯誤**  
值，表示因為發生一般錯誤，所以已拒絕圖元。

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR \_ NOINTERSECTION**  
值，表示因為繪製呼叫不會相交圖元，所以已拒絕圖元。

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ PIXELS OCCLUDED**  
值，表示因為繪圖已 pixels occluded，所以已拒絕圖元。

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**  
值，表示因為深度和樣板測試失敗，所以已拒絕圖元。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



