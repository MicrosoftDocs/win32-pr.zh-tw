---
title: 'glColorMask 函式 (Gl) '
description: GlColorMask 函式會啟用和停用框架緩衝區色彩元件的寫入功能。
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- glColorMask 函式 OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e8b3e9e00eaa294f77813f8e994358cbb473fc4e5c02fce8e5115dc517cae20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081718"
---
# <a name="glcolormask-function"></a>glColorMask 函式

**GlColorMask** 函式會啟用和停用框架緩衝區色彩元件的寫入功能。

## <a name="syntax"></a>語法


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*紅* 
</dt> <dd>

指定紅色是否可寫入至畫面格緩衝區。 預設值為 GL \_ TRUE，表示可以寫入色彩元件。

</dd> <dt>

*綠色* 
</dt> <dd>

指定綠色是否可以或無法寫入至畫面格緩衝區。 預設值為 GL \_ TRUE，表示可以寫入色彩元件。

</dd> <dt>

*藍色* 
</dt> <dd>

指定 blue 是否可以或無法寫入至畫面格緩衝區。 預設值為 GL \_ TRUE，表示可以寫入色彩元件。

</dd> <dt>

*阿 爾 法* 
</dt> <dd>

指定是否可以或不能將 Alpha 寫入至畫面格緩衝區。 預設值為 GL \_ TRUE，表示可以寫入色彩元件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlColorMask** 函式會指定畫面格緩衝區中的個別色彩元件是否可以或無法寫入。 如果 *red* 為 GL \_ FALSE，則不會對任何色彩緩衝區中任何圖元的紅色元件進行任何變更，不論嘗試進行的繪圖操作為何。

無法控制個別元件元件的變更。 相反地，會針對整個色彩元件啟用或停用變更。

下列函式會取出與 **glColorMask** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 色彩 \_ WRITEMASK 的 glGet

具有引數 GL \_ RGBA \_ 模式的 glGet

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





