---
title: 'glIndexMask 函式 (Gl) '
description: GlIndexMask 函式會控制如何在色彩索引緩衝區中寫入個別位。
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- glIndexMask 函式 OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d426cb1f4bb2e794bef53853d0336db1d64b263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966911"
---
# <a name="glindexmask-function"></a>glIndexMask 函式

**GlIndexMask** 函式會控制如何在色彩索引緩衝區中寫入個別位。

## <a name="syntax"></a>語法


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*面具* 
</dt> <dd>

用來啟用和停用在色彩索引緩衝區中寫入個別位的位元遮罩。 一開始，遮罩就是所有的遮罩。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlIndexMask** 函式會控制如何在色彩索引緩衝區中寫入個別位。 最小的 *n* 位 *遮罩*，其中 *1* 是色彩索引緩衝區中的位數，指定遮罩。 當遮罩中出現一個時，會將色彩索引緩衝區 (或) 緩衝區中的對應位設為可寫入。 如果出現零，則位為寫入保護。

這個遮罩只會在色彩索引模式中使用，它只會影響目前為寫入所選取的緩衝區 (請參閱 [**glDrawBuffer**](gldrawbuffer.md)) 。 一開始，所有位都會啟用寫入。

下列函式會抓取 **glIndexMask** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 索引 \_ WRITEMASK 的 glGet

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

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





