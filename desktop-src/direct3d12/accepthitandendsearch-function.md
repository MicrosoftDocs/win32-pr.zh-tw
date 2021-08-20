---
description: 用於任何命中的著色器，以認可目前的點擊次數，然後停止搜尋光線的更多叫用。
ms.assetid: ''
title: AcceptHitAndEndSearch 函式
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 35073145a9b9a4788c6aed3bbae0633f0a9f5b85
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813038"
---
# <a name="accepthitandendsearch-function"></a>AcceptHitAndEndSearch 函式

用於 [任何命中的著色器](any-hit-shader.md) ，以認可目前的點擊次數，然後停止搜尋光線的更多叫用。 如果有交集著色器正在執行，則會停止執行。  執行會傳遞至 [最接近的點擊著色器](closest-hit-shader.md)（若已啟用），並在目前為止記錄最接近的點擊。

## <a name="syntax"></a>語法

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>傳回值

**void**

## <a name="remarks"></a>備註

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**可呼叫著色器**](callable-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**遺漏著色器**](miss-shader.md)
* [**光線產生著色器**](ray-generation-shader.md)



## <a name="see-also"></a>另請參閱

* [Direct3D 12 raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
