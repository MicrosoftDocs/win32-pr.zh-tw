---
title: 'gluBeginTrim 函式 (X.glu 隊) '
description: 'GluBeginTrim 和 gluEndTrim 函式會分隔非統一的有理數 B 曲線 (NURBS) 修剪迴圈定義。 |gluBeginTrim 函式 (X.glu 隊) '
ms.assetid: 636402d0-8f6d-4ad8-84c6-66364025d788
keywords:
- gluBeginTrim 函式 OpenGL
topic_type:
- apiref
api_name:
- gluBeginTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf103a2476aa856b55319e0eca42b8708da169fcedb34e48362062689727ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937881"
---
# <a name="glubegintrim-function"></a>gluBeginTrim 函式

**GluBeginTrim** 和 [**gluEndTrim**](gluendtrim.md)函式會分隔非統一的有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 修剪迴圈定義。

## <a name="syntax"></a>語法


```C++
void WINAPI gluBeginTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nobj* 
</dt> <dd>

使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

使用 **gluBeginTrim** 來標示修剪迴圈的開頭，並使用 **gluEndTrim** 來標記修剪迴圈的結尾。 修剪迴圈是一組面向的曲線線段， (形成封閉曲線) ，以定義 NURBS 表面的界限。 您可以在 [**gluBeginSurface**](glubeginsurface.md) 和 [**gluEndSurface**](gluendsurface.md)的呼叫之間，將這些修剪迴圈包含在 NURBS 介面的定義中。

NURBS 介面的定義可以包含許多修剪迴圈。 例如，如果您撰寫的 NURBS 介面定義類似于帶有打孔的矩形，則定義會包含兩個修剪迴圈。 一個迴圈會定義矩形的外部邊緣;另一個則會定義「穿孔」孔。 這些修剪迴圈的定義會以 **gluBeginTrim**  /  **gluEndTrim** 配對括住。

單一封閉修剪迴圈的定義可以由多個曲線區段所組成，每個線段都是形成線性曲線的一連串直線線段， (查看 [**gluPwlCurve**](glupwlcurve.md)) ，例如單一 NURBS 曲線 ([**查看) ，**](glunurbscurve.md) 或是以任何順序結合兩者。 唯一可出現在 **gluBeginTrim** 和 **gluEndTrim**) 呼叫 (之間的程式庫呼叫，就是 **gluPwlCurve** 和 **gluNurbsCurve**。

NURBS 表面的顯示區域是當曲線參數增加時，在修剪曲線左邊的定義域中的區域。 因此，NURBS 表面的保留區域是在逆時針修剪迴圈內，而非順向修剪迴圈外部。 針對稍早所述的矩形，矩形外部邊緣的修剪迴圈會以逆時針的方向執行，而向外執行的修剪迴圈則以順時針方向執行。

如果您使用多個曲線來定義單一修剪迴圈，則曲線線段必須形成封閉迴圈 (也就是說，每個曲線的端點都必須是下一個曲線的起點，而最後曲線的端點必須是第一個曲線) 的起點。 如果曲線的端點足以緊密地關閉，但不完全一致，則會強制它們相符。 如果端點未足夠關閉，則會產生錯誤結果 (查看 [*gluNurbsCallback*](glunurbs.md)) 。

如果修剪迴圈定義包含多個曲線，則曲線的方向必須是一致的 (也就是說，內部必須位於所有曲線的左邊) 。 只要曲線方向的替代正確，您就可以使用嵌套修剪迴圈。 修剪曲線無法自我相交，也不能彼此相交 (或錯誤結果) 。

如果未針對 NURBS 表面提供修剪資訊，則會繪製整個表面。

## <a name="examples"></a>範例

這個程式碼片段會定義一個修剪迴圈，其中包含一個分段線性曲線和兩個 NURBS 曲線：

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>X.glu 隊。h</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Glu32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





