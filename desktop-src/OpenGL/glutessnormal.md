---
title: 'gluTessNormal 函式 (X.glu 隊) '
description: GluTessNormal 函數會指定多邊形的一般。
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- gluTessNormal 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934983"
---
# <a name="glutessnormal-function"></a>gluTessNormal 函式

**GluTessNormal** 函數會指定多邊形的一般。

## <a name="syntax"></a>語法


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*苔 絲* 
</dt> <dd>

使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。

</dd> <dt>

*x* 
</dt> <dd>

一般的 x 座標元件。

</dd> <dt>

*y* 
</dt> <dd>

一般的 y 座標元件。

</dd> <dt>

*Z* 
</dt> <dd>

一般的 z 座標元件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluTessNormal** 函式描述您所定義多邊形的一般。 所有輸入資料都會投射在鑲嵌式之前垂直的平面，而且所有輸出三角形都是以逆時針方向進行導向。  (若要取得順時針方向，請將提供的一般) 的正負號反轉。 例如，如果您知道所有多邊形都位於 x-y 平面中，請在轉譯任何多邊形之前，先呼叫 **gluTessNormal** (tess，0.0，0.0，1.0) 。

如果提供的一般 (0.0、0.0、0.0)  (預設值) ，則會以下列方式決定正常：

1.  標準的方向（最多可到其正負號）是藉由將平面調整到頂點的方式找到，而不考慮頂點的連接方式。 輸入資料應該大約位於平面中;否則，垂直投影的三個座標軸之一可以大幅變更幾何。
2.  選擇 [一般] 的正負號，如此一來，所有輸入等高線的已簽署區域總和都是非負的 (其中的逆時針輪廓具有正區域) 。

提供的一般保存，直到 **gluTessNormal** 的另一個呼叫變更為止。

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

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> </dl>

 

 





