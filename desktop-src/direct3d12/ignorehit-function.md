---
description: 從任何命中的著色器呼叫，以拒絕點擊並結束著色器。
ms.assetid: ''
title: IgnoreHit 函式
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000051"
---
# <a name="ignorehit-function"></a>IgnoreHit 函式

從 [任何命中的著色器](any-hit-shader.md) 呼叫，以拒絕點擊並結束著色器。 點擊搜尋會繼續進行，而不會認可目前點擊的距離和屬性。  [交集著色器](intersection-shader.md)中的 [**ReportHit**](reporthit-function.md)呼叫（如果有的話）會傳回 false。  任何對光線承載所做的任何修改都會保留在任何點擊著色器中的這個位置。

## <a name="syntax"></a>語法

```
void IgnoreHit();

```


## <a name="return-value"></a>傳回值

**void**

## <a name="remarks"></a>備註

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**任何命中著色器**](any-hit-shader.md)




## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




