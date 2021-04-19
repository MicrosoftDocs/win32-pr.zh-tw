---
description: 從物件空間轉換成世界空間的矩陣。
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: 613b4c403f235819845114e7019e07051a25ec80
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966632"
---
# <a name="objecttoworld4x3"></a>ObjectToWorld4x3

從物件空間轉換成世界空間的矩陣。 物件空間是指目前最下層加速結構的空間。

## <a name="syntax"></a>語法

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a>備註

矩陣是 **ObjectToWorld3x4** 矩陣的調換。

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**任何命中著色器**](any-hit-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**交集著色器**](intersection-shader.md)





## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




