---
title: 'glLoadMatrixf 函式 (Gl) '
description: 'GlLoadMatrixf 函數會以任意矩陣取代目前的矩陣。 |glLoadMatrixf 函式 (Gl) '
ms.assetid: 6e1337b0-d1e7-4002-a561-d959d7f70942
keywords:
- glLoadMatrixf 函式 OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3d822d784d6e24b15296a29da1c77b37b55af4211d2d9b5ce40a3c6a43c7fdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492840"
---
# <a name="glloadmatrixf-function"></a>glLoadMatrixf 函式

[**GlLoadMatrixd**](glloadmatrixd.md)和 **glLoadMatrixf** 函數會將目前的矩陣取代為任意矩陣。

## <a name="syntax"></a>語法


```C++
void WINAPI glLoadMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*m* 
</dt> <dd>

以資料行主要順序儲存為16個連續值之4x4 矩陣的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlLoadMatrix** 函式會將目前的矩陣取代為在 *m* 中指定的矩陣。 目前的矩陣是投射矩陣、模型矩陣或紋理矩陣，由目前的矩陣模式決定 (查看 [**glMatrixMode**](glmatrixmode.md)) 。

*M* 參數指向以資料行主要順序儲存之單精確度或雙精確度浮點值的4x4 矩陣。 也就是說，矩陣的儲存方式如下圖所示。

![顯示 m 參數所指向之4x4 矩陣的圖表。](images/load02.png)

下列函式會取出與 **glLoadMatrix** 相關的資訊：

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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





