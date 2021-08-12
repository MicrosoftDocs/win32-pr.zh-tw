---
title: 'glEvalMesh2 函式 (Gl) '
description: 計算點或線條的二維方格。
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- glEvalMesh2 函式 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5f1a16b1ceda2c13f24a779032b0e920d364db46167a9dc02ca2b27277262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616104"
---
# <a name="glevalmesh2-function"></a>glEvalMesh2 函式

計算點或線條的二維方格。

## <a name="syntax"></a>語法


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

值，指定是否要計算點、線條或多邊形的二維網格。 接受下列符號常數： GL \_ 點、gl \_ 線路和 gl \_ 填滿。

</dd> <dt>

*i1* 
</dt> <dd>

方格網域變數 i 的第一個整數值。

</dd> <dt>

*i2* 
</dt> <dd>

方格網域變數 i 的最後一個整數值。

</dd> <dt>

*j1* 
</dt> <dd>

方格網域變數 j 的第一個整數值。

</dd> <dt>

*j2* 
</dt> <dd>

方格網域變數 j 的最後一個整數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | 表示 *模式* 不是可接受的值。 <br/>                                                                            |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。 <br/> |



## <a name="remarks"></a>備註

使用 [**glMapGrid**](glmapgrid-functions.md) 和 [**glEvalMesh**](glevalmesh-functions.md) ，以便有效率地產生和評估一系列平均間距的地圖定義域值。 **GlEvalMesh** 函式會逐步執行一維或二維方格的整數定義域，其範圍是 [**glMap1**](glmap1.md)和 [**glMap2**](glmap2.md)所指定之評估對應的定義域。 Mode 參數會決定產生的頂點是否以點、線條或填滿的多邊形連接。

在二維案例中， **glEvalMesh2**，let

? u = (u2 u1) /n

? v = (v2 v1) /m，

其中 n、u1、u2、m、v1 和 v2 是最新 [**glMapGrid2**](glmapgrid-functions.md) 函式的引數。 然後，如果 *mode* 是 GL \_ FILL， **glEvalMesh2** 相當於：

若為 (j = j1;j < j2;j + = 1) 

{

[**glBegin**](glbegin.md) (GL \_ 四個 \_ 帶) ;

針對 (i = i1;i <= i2;i + = 1) 

{

[**glEvalCoord2**](glevalcoord2d.md) (i？u + u1 ( ) ，j？ v + v1) ;

[**glEvalCoord2**](glevalcoord2d.md) (i？u + u1 ( ) ， (j + 1) ？ v + v1) ;

}

[**glEnd**](glend.md) ( ) ;}

如果 *mode* 是 GL \_ 行，則呼叫 **glEvalMesh2** 相當於：

若為 (j = j1;j <= j2;j + = 1) 

{

[**glBegin**](glbegin.md) (GL \_ 行 \_ 帶) ;

針對 (i = i1;i <= i2;i + = 1) 

{

[**glEvalCoord2**](glevalcoord2d.md) (i？u + u1、j？v + v1) ;

}

[**glEnd**](glend.md) ( ) ;

}

針對 (i = i1;i <= i2;i + = 1) 

{

[**glBegin**](glbegin.md) (GL \_ 行 \_ 帶) ;

若為 (j = j1;j <= j1;j + = 1) 

{

[**glEvalCoord2**](glevalcoord2d.md) (i？u + u1、j？v + v1) ;

}

glEnd ( ) ;

}

最後，如果 *模式* 是 GL \_ 點，則呼叫 **glEvalMesh2** 相當於：

[**glBegin**](glbegin.md) (GL \_ 點) ;

若為 (j = j1;j <= j2;j + = 1) 

{

針對 (i = i1;i <= i2;i + = 1) 

{

[**glEvalCoord2**](glevalcoord2d.md) (i？u + u1、j？v + v1) ;

}

}

[**glEnd**](glend.md) ( ) ;

在這三種情況下，唯一的絕對數值需求是，如果 i = n，則是從 i 計算的值？u + u1 正好是 u2，如果 j = m，則是從 j 計算的值？v + v1 正好為 v2。 下列函式會取出與 **glEvalMesh** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ MAP1 \_ 方格 \_ 網域的 glGet

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ list.map2 \_ 方格 \_ 網域的 glGet

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ MAP1 \_ 方格 \_ 區段的 glGet

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ list.map2 \_ 方格 \_ 區段的 glGet

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl>         |
| 程式庫<br/>                  | <dl> <dt>Opengl32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

 





