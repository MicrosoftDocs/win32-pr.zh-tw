---
description: 傳回作為 HitKind 參數傳遞至 ReportHit 的值。
ms.assetid: ''
title: HitKind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972341"
---
# <a name="hitkind"></a>HitKind

傳回作為 **HitKind** 參數傳遞至 [**ReportHit**](reporthit-function.md)的值。

## <a name="syntax"></a>語法

```
uint HitKind();

```



## <a name="remarks"></a>備註

如果交集是由固定函式三角形交集所報告，則 **HitKind** 會是 (254) 的 **點擊類型 \_ \_ 三角形 \_ 正面 \_ 臉部** ，或 (255) 的 **點擊 \_ 類型 \_ 三角形 \_ \_** 。

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**任何命中著色器**](any-hit-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**交集著色器**](intersection-shader.md)





## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




