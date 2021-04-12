---
title: 'gluNextContour 函式 (X.glu 隊) '
description: GluNextContour 函式會將另一個輪廓的開頭標示為開頭。
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- gluNextContour 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384250"
---
# <a name="glunextcontour-function"></a>gluNextContour 函式

\[**GluNextContour** 函式已過時，而且只為了回溯相容性而提供。 **GluNextContour** 函式會對應到 [**gluTessEndContour**](glutessendcontour.md) ，後面接著 [**gluTessBeginContour**](glutessbegincontour.md)。\]

**GluNextContour** 函式會將另一個輪廓的開頭標示為開頭。

## <a name="syntax"></a>語法


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*苔 絲* 
</dt> <dd>

使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。

</dd> <dt>

*type* 
</dt> <dd>

要定義的輪廓類型。 下列是有效的值。



| 值                                                                                                                                                                | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <dt>**X.GLU 隊 \_ 外部**</dt> </dl>           | 外輪廓定義多邊形的外部界限。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <dt>**X.GLU 隊 \_ 內部**</dt> </dl>           | 內部輪廓會定義多邊形 (的內部界限，例如洞) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <dt>**X.GLU 隊 \_ 不明**</dt> </dl>              | 程式庫會分析未知的輪廓，以判斷其是否為內部或外部。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <dt>**X.GLU 隊 \_ CCW，X.GLU 隊 \_ CW**</dt> </dl> | 第一個定義的 X.GLU 隊 \_ CCW 或 X.glu 隊 \_ CW 分布圖會視為外部。 如果所有其他的輪廓都是以相同方向進行導向， (順時針或逆時針) 作為第一個輪廓，如果不是，則會被視為外部。<br/> 如果某個輪廓的類型為 X.GLU 隊 \_ CCW 或 X.glu 隊 \_ CW，則所有的輪廓都必須是相同類型 (如果不是，則所有 x.glu 隊 \_ CCW 和 x.glu 隊 \_ 的 CW 分佈將會變更為 x.glu 隊 \_ 未知) 。 請注意，X.GLU 隊 \_ CCW 和 x.glu 隊的 CW 分佈類型之間沒有真正的差異 \_ 。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

您可以使用 **gluNextContour** 函數來描述具有多個分佈的多邊形。 當您透過一連串的 [**gluTessVertex**](glutessvertex.md) 呼叫來描述第一個輪廓之後， **gluNextContour** 呼叫會指出先前的輪廓已完成，而且下一個輪廓即將開始。 執行另一系列的 **gluTessVertex** 呼叫來描述新的輪廓。 重複此程式，直到描述所有的輪廓為止。

*Type* 參數會定義其後的輪廓類型。

若要定義第一個輪廓的型別，您可以在描述第一個輪廓之前呼叫 **gluNextContour** 。 如果您未在第一個輪廓之前呼叫 **gluNextContour** ，則會將第一個輪廓標示為 x.glu 隊 \_ 外部。

## <a name="examples"></a>範例

您可以在其中描述具有三角形孔的四邊形，如下所示：

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4);  
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7);  
gluEndPolygon(tess);
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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





