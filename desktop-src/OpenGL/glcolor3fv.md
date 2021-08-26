---
title: 'glColor3fv 函式 (Gl) '
description: '從已存在的色彩值陣列中設定目前的色彩。 |glColor3fv 函式 (Gl) '
ms.assetid: 4ffaaa7e-4fa3-45b8-acf0-850e1e9d9a60
keywords:
- glColor3fv 函式 OpenGL
topic_type:
- apiref
api_name:
- glColor3fv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533256054c847d01b0e4799f58736b49fbad2aff399452bdcb2d956c8ee610fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081908"
---
# <a name="glcolor3fv-function"></a>glColor3fv 函式

從已存在的色彩值陣列中設定目前的色彩。

## <a name="syntax"></a>語法


```C++
void WINAPI glColor3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*v* 
</dt> <dd>

陣列的指標，其中包含紅色、綠色和藍色值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

GL 會儲存目前的單一值色彩索引和目前的四值 RGBA 色彩。 **glcolor** 會設定新的四值 RGBA 色彩。 **glcolor** 有兩個主要變異： **glcolor3** 和 **glcolor4**。 **glcolor3** 變體會明確指定新的紅色、綠色和藍色值，並將目前的 Alpha 值設定為1.0， (以隱含的方式) 完全濃度。 **glcolor4** variant 會明確指定全部四個色彩元件。

**glcolor3b**、 **glcolor4b**、 **glcolor3s**、 **glcolor4s**、 **glcolor3i** 和 **glcolor4i** 會採用三個或四個帶正負號的位元組、短或長整數作為引數。 當 v 附加至名稱時，color 命令可取得此類值陣列的指標。

目前的色彩值會以浮點格式儲存，並具有未指定的尾數和指數大小。 指定時，不帶正負號的整數色彩元件會以線性方式對應至浮點值，因此最大的可表示值會對應至 1.0 (滿濃度) ，而0對應至 0.0 (零濃度) 。 經過指定時，帶正負號的整數色彩元件會以線性方式對應至浮點值，因此最大的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。  (請注意，此對應不會精確地將0轉換為0.0。 ) 浮點值會直接對應。

浮點數或帶正負號的整數值都不會在 \[ \] 目前的色彩更新之前壓制至範圍0、1。 不過，在將色彩元件插入或寫入至色彩緩衝區之前，會將色彩元件壓制至這個範圍。

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

[**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindexd.md)
</dt> </dl>

 

 





