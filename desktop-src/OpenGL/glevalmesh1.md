---
title: 'glEvalMesh1 函式 (Gl) '
description: 計算點或線條的一維方格。
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- glEvalMesh1 函式 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508787"
---
# <a name="glevalmesh1-function"></a>glEvalMesh1 函式

計算點或線條的一維方格。

## <a name="syntax"></a>語法


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

值，指定是否要計算點或線條的一維網格。 接受下列符號常數： GL \_ 點和 gl \_ 行。

</dd> <dt>

*i1* 
</dt> <dd>

方格網域變數 i 的第一個整數值。

</dd> <dt>

*i2* 
</dt> <dd>

方格網域變數 i 的最後一個整數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | 表示 *模式* 不是可接受的值。 <br/>                                                                            |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。 <br/> |



## <a name="remarks"></a>備註

將 [**glMapGrid**](glmapgrid-functions.md) 和 [**glEvalMesh**](glevalmesh-functions.md) 一起使用，可有效率地產生和評估一系列平均間距的地圖定義域值。 **GlEvalMesh** 函式會逐步執行一維或二維方格的整數定義域，其範圍是 [**glMap1**](glmap1.md)和 [**glMap2**](glmap2.md)所指定之評估對應的定義域。 Mode 參數會決定產生的頂點是否以點、線條或填滿的多邊形連接。

在一維的案例中， **glEvalMesh1** 會產生網格，就像執行下列程式碼片段一樣：

[**glBegin**](glbegin.md) (*類型*) ;

針對 (i = i1;i <= i2;i + = 1) 

{

[**glEvalCoord1**](glevalcoord1d.md) (i？ u + u1) 

}

[**glEnd**](glend.md) ( ) ;

其中

？ u = (u2 u1) /n

和 n、u1 和 u2 是最新 [**glMapGrid1**](glmapgrid1d.md) 函式的引數。  \_ 如果模式為 gl 點，則類型參數為 gl 點 \_ ， \_ 如果模式為 GL 行，則為 gl 行 \_ 。 其中一個絕對數值需求是，如果 i = n，則計算自 i？ u + u1 的值就完全是 u2。

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

[**glBegin**](glbegin.md)
</dt> </dl>

 

 





