---
description: ObjectToWorld4x3-從物件空間轉換成世界空間的矩陣。
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
ms.openlocfilehash: bc91c6e98aceb13af3f589f873a4b96c2b1843c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098296"
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

 

 




