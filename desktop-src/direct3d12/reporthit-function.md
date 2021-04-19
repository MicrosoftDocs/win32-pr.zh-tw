---
description: 由交集著色器呼叫以報告光線交集。
ms.assetid: ''
title: ReportHit 函式
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973593"
---
# <a name="reporthit-function"></a>ReportHit 函式

由 [交集著色器](intersection-shader.md) 呼叫以報告光線交集。

## <a name="syntax"></a>Syntax
此內建函式定義相當於下列函式範本：

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>參數

`THit`

浮點值，指定交集的參數距離。

`HitKind`

識別所發生點擊類型的不帶正負號的整數。  這是在0-127 範圍內的使用者指定值。  您可以使用 **HitKind** 內建的 [任何命中](any-hit-shader.md)或 [最接近的點擊](closest-hit-shader.md)著色器來讀取該值。

`Attributes`

指定交集屬性的使用者定義 [**交集屬性結構**](intersection-attributes.md) 結構。  

## <a name="return-value"></a>傳回值

**bool** 如果已接受點擊則為 True。  如果 *賦值* 超出目前的光線間隔，或任何點擊著色器呼叫 [**IgnoreHit**](ignorehit-function.md)，則會拒絕點擊。  目前的光線間隔是由 **RayTMin** 和 **RayTCurrent** 定義。

## <a name="remarks"></a>備註

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**交集著色器**](intersection-shader.md)





## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




