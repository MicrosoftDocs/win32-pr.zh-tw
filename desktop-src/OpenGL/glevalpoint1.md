---
title: 'glEvalPoint1 函式 (Gl) '
description: 'GlEvalPoint1 和 glEvalPoint2 函數會產生和評估網格中的單一點。 |glEvalPoint1 函式 (Gl) '
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- glEvalPoint1 函式 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853888"
---
# <a name="glevalpoint1-function"></a>glEvalPoint1 函式

[**GlEvalPoint1**](glevalpoint.md)和 **glEvalPoint2** 函數會產生和評估網格中的單一點。

## <a name="syntax"></a>語法


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*i* 
</dt> <dd>

方格網域變數 *i* 的整數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

[**GlMapGrid**](glmapgrid-functions.md)和 [**glEvalMesh**](glevalmesh-functions.md)函式會以串聯方式使用，以有效率地產生和評估一連串的平均地圖定義域值。 您可以使用 **glEvalPoint** 來評估 **glEvalMesh** 所進行的相同 gridspace 中的單一方格點。 呼叫 [**glEvalPoint1**](glevalpoint.md) 相當於呼叫

**glEvalCoord1** (*i* ？*u*  +*u* 1 ) ;

其中

?*u* = (*u* 2 *u* 1 ) /*n*

和 *n*、 *u* 1 和 *u* 2 是最近 **glMapGrid1** 函數的引數。 其中一個絕對數值需求是，如果 *我* 是  =  *n*，則會從 (*i* 計算值？*u* + u1 ) 剛好是 *u* 2。

在二維案例中， **glEvalPoint2**，let

?*u* = (*u* 2 *u* 1 ) /*n*

?*v* = (*v* 2 *v* 1 ) /*m*

其中 *n*、 *u* 1、 *u* 2、 *m*、 *v* 1 和 *v* 2 是最新 **glMapGrid2** 函式的引數。 然後， **glEvalPoint2** 函式相當於呼叫

**glEvalCoord2** (*i* ？*u*  + *u* 1、 *j* ？*v*  + *v* 1 ) ;

唯一的絕對數值需求是，如果 *我* 是 = *n*，則會從 (*i* 計算值？*u*  +  *u* 1 ) 完全是 u2，如果是 *j*  =  *m*，則是從 (*j* 計算的值？*v v*  +  ** 1 ) 正好是 *v* 2。

下列函式會取得 [**glEvalPoint1**](glevalpoint.md) 和 **glEvalPoint2** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ MAP1 \_ 方格 \_ 網域的 glGet

具有引數 GL \_ list.map2 \_ 方格 \_ 網域的 glGet

具有引數 GL \_ MAP1 \_ 方格 \_ 區段的 glGet

具有引數 GL \_ list.map2 \_ 方格 \_ 區段的 glGet

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl>         |
| 程式庫<br/>                  | <dl> <dt>Opengl32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> </dl>

 

 





