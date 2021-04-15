---
title: 'glFrustum 函式 (Gl) '
description: GlFrustum 函式會將目前的矩陣乘以透視圖矩陣。
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- glFrustum 函式 OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce67879ca20819713e61a9392bf77be2f15211d5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104554978"
---
# <a name="glfrustum-function"></a>glFrustum 函式

**GlFrustum** 函式會將目前的矩陣乘以透視圖矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI glFrustum(
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

右垂直裁剪平面的座標。

</dd> <dt>

*底部* 
</dt> <dd>

下水準裁剪平面的座標。

</dd> <dt>

*top* 
</dt> <dd>

下水準裁剪平面的座標。

</dd> <dt>

*zNear* 
</dt> <dd>

接近深度裁剪平面的距離。 必須是正數。

</dd> <dt>

*zFar* 
</dt> <dd>

距離最深度裁剪平面的距離。 必須是正數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | 未 postitive *zNear* 或 *zFar* 。<br/>                                                                                       |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlFrustum** 函式描述會產生透視圖投影的透視圖矩陣。  (*left*、top **、 *zNear*) 和 (*right*、 *top*、 *zNear*) 參數指定接近裁剪平面的點，這些點會分別對應至視窗左下角和右上角，並假設眼睛位於 (0、0、0) 。 *ZFar* 參數會指定最遠裁剪平面的位置。 *ZNear* 和 *zFar* 都必須是正數。 對應的矩陣如下圖所示。

![顯示產生觀點投射之透視圖矩陣的圖表。](images/frust01.png)![顯示描述透視圖矩陣之 glFrustum 函數的方程式。](images/frust02.png)

**GlFrustum** 函式會將目前的矩陣乘以此矩陣，並將結果取代為目前的矩陣。 也就是說，如果 M 是目前的矩陣，而 F 是截錐的觀點矩陣，則 **glFrustum** 會以 m F 取代 m。

使用 [**glPushMatrix**](glpushmatrix.md) 和 [**glPopMatrix**](glpopmatrix.md) 來儲存和還原目前的矩陣堆疊。

深度緩衝區精確度會受到針對 *zNear* 和 *zFar* 指定的值所影響。 *ZFar* 與 *zNear* 的比率愈大，深度緩衝區就越不會區分彼此接近的表面。 如果

![顯示距離接近的比率的方程式。](images/frust03.png)

大約 *記錄* 2 (*r*) 深度緩衝區精確度的位會遺失。 因為 *r* 的 *zNear* 方法為零，所以不應該將 *zNear* 設定為零。

下列函式會取出 **glFrustum** 的相關資訊：

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

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





