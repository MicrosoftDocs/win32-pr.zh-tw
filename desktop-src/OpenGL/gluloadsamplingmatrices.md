---
title: 'gluLoadSamplingMatrices 函式 (X.glu 隊) '
description: GluLoadSamplingMatrices 函式會載入非統一的有理 B 曲線 (NURBS) 取樣和剔除矩陣。
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- gluLoadSamplingMatrices 函式 OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41b2f6b25e0cecf0d13d87760a941d5ea68baa1fdd85495c8a316e862c77aec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777528"
---
# <a name="gluloadsamplingmatrices-function"></a>gluLoadSamplingMatrices 函式

**GluLoadSamplingMatrices** 函式會載入非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 取樣和剔除矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nobj* 
</dt> <dd>

使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。

</dd> <dt>

*modelMatrix* 
</dt> <dd>

模型矩陣 (為 [**glGetFloatv**](glgetfloatv.md) 呼叫) 。

</dd> <dt>

*projMatrix* 
</dt> <dd>

投射矩陣 (從 **glGetFloatv** 呼叫) 。

</dd> <dt>

*視窗* 
</dt> <dd>

從 [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 呼叫)  (的區。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluLoadSamplingMatrices** 函式會使用 *modelMatrix*、 *projMatrix* 和 *視口* 來重新計算儲存在 *nobj* 中的取樣和剔除矩陣。 取樣矩陣會決定必須鑲嵌的 NURBS 曲線或表面，以滿足 X.GLU 隊 \_ 取樣容錯屬性) 所決定的取樣 (容錯 \_ 。 您可以使用 [剔除] 矩陣來決定是否應該在轉譯 (，然後在) 開啟 [X.GLU 隊剔除] 屬性時，挑選 \_ 。

只有當 [X.GLU 隊 AUTO LOAD MATRIX] 屬性關閉時，才需要 **gluLoadSamplingMatrices** 函式 \_ \_ \_ (請參閱 [**gluNurbsProperty**](glunurbsproperty.md)) 。 雖然讓 X.GLU 隊 \_ AUTO \_ LOAD MATRIX 屬性保持開啟很方便 \_ ，但這麼做會需要往返于 OpenGL 伺服器，才能取得模型矩陣、投影矩陣和視口的目前值。 ) 

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

[**glGetFloatv**](glgetfloatv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





