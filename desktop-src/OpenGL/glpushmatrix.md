---
title: 'glPushMatrix 函式 (Gl) '
description: 'GlPushMatrix 和 glPopMatrix 函式會推送並取出目前的矩陣堆疊。 |glPushMatrix 函式 (Gl) '
ms.assetid: 97d8e644-50bb-4130-b6b7-d87df4468e73
keywords:
- glPushMatrix 函式 OpenGL
topic_type:
- apiref
api_name:
- glPushMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0d6af41bb02c82a28b667a2b5ad62d942c036c7f744a68fa9bb79188e26ae8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795133"
---
# <a name="glpushmatrix-function"></a>glPushMatrix 函式

**GlPushMatrix** 和 [**glPopMatrix**](glpopmatrix.md)函式會推送並取出目前的矩陣堆疊。

## <a name="syntax"></a>語法


```C++
void WINAPI glPushMatrix(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

推送完整的矩陣堆疊或 pop 只包含單一矩陣的矩陣堆疊是錯誤的。 在任一種情況下，都會設定錯誤旗標，且不會對 OpenGL 狀態進行其他變更。

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 堆疊 \_ 溢位**</dt> </dl>    | 當目前的矩陣堆疊已滿時，就會呼叫函數。<br/>                                                           |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

每個矩陣模式都有一個矩陣堆疊。 在 GL \_ 模型模式中，堆疊深度至少為32。 在其他兩種模式中，則 \_ 是 gl 投射和 gl \_ 材質，深度至少是2。 在任何模式下，目前的矩陣都是該模式之堆疊頂端的矩陣。

**GlPushMatrix** 函式會將目前的矩陣堆疊向下推一，以複製目前的矩陣。 也就是說，在 **glPushMatrix** 呼叫之後，堆疊頂端的矩陣與下面的矩陣相同。 **GlPopMatrix** 函式會取出目前的矩陣堆疊，並將目前的矩陣取代為堆疊上的下一個矩陣。 一開始，每個堆疊都會包含一個矩陣，也就是一個識別矩陣。

下列函式會取出 **glPushMatrix** 和 **glPopMatrix** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet

具有引數 GL \_ 模型 \_ 矩陣的 glGet

具有引數 GL \_ 投射 \_ 矩陣的 glGet

具有引數 GL \_ 材質 \_ 矩陣的 glGet

具有引數 GL \_ 模型 \_ STACK \_ 深度的 glGet

具有引數 GL \_ 投射 \_ 堆疊 \_ 深度的 glGet

具有引數 GL \_ 紋理 \_ 堆疊 \_ 深度的 glGet

具有引數 GL \_ 最大 \_ 模型 \_ 堆疊 \_ 深度的 glGet

具有引數 GL \_ 最大 \_ 投射 \_ 堆疊 \_ 深度的 glGet

具有引數 GL \_ 最大 \_ 材質 \_ 堆疊 \_ 深度的 glGet

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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





