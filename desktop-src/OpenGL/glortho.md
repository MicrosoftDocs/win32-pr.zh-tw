---
title: 'glOrtho 函式 (Gl) '
description: GlOrtho 函式會將目前的矩陣乘以正向矩陣。
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- glOrtho 函式 OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104553311"
---
# <a name="glortho-function"></a>glOrtho 函式

**GlOrtho** 函式會將目前的矩陣乘以正向矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI glOrtho(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*離開* 
</dt> <dd>

左方垂直裁剪平面的座標。

</dd> <dt>

*對* 
</dt> <dd>

Theright 垂直裁剪平面的座標。

</dd> <dt>

*底部* 
</dt> <dd>

底部水準裁剪平面的座標。

</dd> <dt>

*top* 
</dt> <dd>

上方水準裁剪計畫的座標。

</dd> <dt>

*zNear* 
</dt> <dd>

靠近深度裁剪平面的距離。 如果平面位於檢視器後方，此距離就會是負數。

</dd> <dt>

*zFar* 
</dt> <dd>

距離深度裁剪平面的距離。 如果平面位於檢視器後方，此距離就會是負數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlOrtho** 函數描述產生平行投影的透視圖矩陣。  (*左方*、 *底部*、 *接近*) 和 (*right*、 *top*、 *near*) 參數指定接近裁剪平面的點，這些點會分別對應至視窗左下角和右上角，並假設眼睛位於 (0、0、0) 。 最 *遠* 的參數會指定最遠裁剪平面的位置。 *ZNear* 和 *zFar* 都可以是正數或負數。 對應的矩陣如下圖所示。

![此圖顯示 glOrtho 函式所描述的透視圖矩陣。](images/ortho1.png)

其中

![描述透視圖矩陣的方。](images/ortho2.png)

目前的矩陣會乘以此矩陣，且結果會取代目前的矩陣。 也就是說，如果 M 是目前的矩陣，而 O 是 ortho 矩陣，則 M 會取代為 M O。

使用 [**glPushMatrix**](glpushmatrix.md) 和 **glPopMatrix** 來儲存和還原目前的矩陣堆疊。 使用 [**glMatrixMode**](glmatrixmode.md) 來設定目前的矩陣。

下列函式會取出與 **glOrtho** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet

具有引數 GL \_ 模型 \_ 矩陣的 glGet

具有引數 GL \_ 投射 \_ 矩陣的 glGet

具有引數 GL \_ 材質 \_ 矩陣的 glGet

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
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





