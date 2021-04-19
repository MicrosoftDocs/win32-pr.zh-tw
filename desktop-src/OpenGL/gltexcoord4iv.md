---
title: 'glTexCoord4iv 函式 (Gl) '
description: '設定目前的材質座標。 |glTexCoord4iv 函式 (Gl) '
ms.assetid: 4ce3070c-70c1-4a2b-a6e7-084a4baa3dc5
keywords:
- glTexCoord4iv 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4iv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2ec50556e871a66db79bb3d7d956e103f586a9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "107000354"
---
# <a name="gltexcoord4iv-function"></a>glTexCoord4iv 函式

設定目前的材質座標。

## <a name="syntax"></a>語法


```C++
void WINAPI glTexCoord4iv(
   const GLint *v
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*V* 
</dt> <dd>

四個元素之陣列的指標，接著會指定 s、t、r 和 q 材質座標。

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

 

 





