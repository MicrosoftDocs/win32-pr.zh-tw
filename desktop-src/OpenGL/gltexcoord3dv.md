---
title: 'glTexCoord3dv 函式 (Gl) '
description: '設定目前的材質座標。 |glTexCoord3dv 函式 (Gl) '
ms.assetid: 410f49d6-7950-4940-a377-d62ca2bd5db7
keywords:
- glTexCoord3dv 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02bc579a0ae8c9dc0c386ee7ce6757c7d6bbe11539561b0716cde8949b0cc23a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036348"
---
# <a name="gltexcoord3dv-function"></a>glTexCoord3dv 函式

設定目前的材質座標。

## <a name="syntax"></a>語法


```C++
void WINAPI glTexCoord3dv(
   const GLdouble *v
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*v* 
</dt> <dd>

指標，指向三個元素的陣列，接著指定 s、t 和 r 材質座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

[**GlTexCoord**](gltexcoord-functions.md)函式會將目前的材質座標設定為與多邊形頂點相關聯之資料的一部分。 **GlTexCoord** 函數會指定一、二、三或四個維度中的材質座標。 GlTexCoord1 函式會將目前的材質座標設定為 (s、0、0、1) ;對 glTexCoord2 的呼叫會將它們設定為 (s、t、0、1) 。 同樣地，glTexCoord3 會將材質座標指定為 (s、t、r、1) ，而 glTexCoord4 會將所有四個元件明確定義為 (s、t、r、q) 。 您可以隨時更新目前的材質座標。 尤其是，您可以呼叫 [**glBegin**](glbegin.md) 的呼叫與 [**glEnd**](glend.md)的對應呼叫之間的 glTexCoord。 下列函式會抓取 **glTexCoord** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 材質 \_ COORDS 的 glGet

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





