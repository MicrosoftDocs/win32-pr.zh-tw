---
title: 'glColor4b 函式 (Gl) '
description: '設定目前的色彩。 |glColor4b 函式 (Gl) '
ms.assetid: 50d829f2-f336-40be-8598-a255c86f0722
keywords:
- glColor4b 函式 OpenGL
topic_type:
- apiref
api_name:
- glColor4b
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7cddf33fa16b0ffa6607610b9194a8518cbb31bc06e05cd335710605fa258c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061856"
---
# <a name="glcolor4b-function"></a>glColor4b 函式

設定目前的色彩。

## <a name="syntax"></a>語法


```C++
void WINAPI glColor4b(
   GLbyte red,
   GLbyte green,
   GLbyte blue,
   GLbyte alpha
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*紅* 
</dt> <dd>

目前色彩的新紅色值。

</dd> <dt>

*綠色* 
</dt> <dd>

目前色彩的新綠色值。

</dd> <dt>

*藍色* 
</dt> <dd>

目前色彩的新藍色值。

</dd> <dt>

*阿 爾 法* 
</dt> <dd>

目前色彩的新 Alpha 值。

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

 

 





