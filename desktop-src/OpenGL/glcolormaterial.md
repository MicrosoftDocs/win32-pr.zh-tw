---
title: 'glColorMaterial 函式 (Gl) '
description: GlColorMaterial 函式會導致材質色彩追蹤目前的色彩。
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- glColorMaterial 函式 OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55cc846cfbc400d2372186f9af4a09db08e5ad769d1e8fec5f5f6f757e1ff447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360469"
---
# <a name="glcolormaterial-function"></a>glColorMaterial 函式

**GlColorMaterial** 函式會導致材質色彩追蹤目前的色彩。

## <a name="syntax"></a>語法


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*臉* 
</dt> <dd>

指定 front、back 或 front 和 back 材質參數是否都應該追蹤目前的色彩。 接受的值是 GL \_ 前端、gl \_ 回來，以及 gl \_ 前端 \_ 和 \_ 後端。 預設值是 GL \_ FRONT \_ 和 \_ BACK。

</dd> <dt>

*mode* 
</dt> <dd>

指定要追蹤目前色彩的數個材質參數。 接受的值為 GL 發出 \_ 、gl \_ 環境、gl \_ 擴散、gl \_ 反射，以及 gl \_ 環境 \_ 和 \_ 擴散。 預設值為 GL \_ 環境 \_ 和 \_ 擴散。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *臉部* 或 *模式* 不是可接受的值。<br/>                                                                                |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlColorMaterial** 函數會指定追蹤目前色彩的材質參數。 當您 \_ \_ 針對 *臉部* 所指定的每個材質或材質啟用 GL 色彩材質時，由 *模式* 指定的材質參數或參數會隨時追蹤目前的色彩。 使用 GlEnable 和 GlDisable 函式來啟用和停 \_ 用 gl 色彩 \_ 材質，以 GL [](glenable.md) [](gldisable.md) \_ 色彩 \_ 材質作為其引數來呼叫。 預設 \_ \_ 會停用 GL 色彩材質。

使用 **glColorMaterial**，您可以只使用 [**glColor**](glcolor-functions.md) 函數來變更每個頂點的材質參數子集，而不需要呼叫 [**glMaterial**](glmaterial-functions.md)。 如果您只是針對每個頂點指定這類參數子集，最好使用 **glColorMaterial** 而不是 **glMaterial**。

下列函式會取出與 **glColorMaterial** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ COLOR \_ 材質 \_ 參數的 glGet

**glGet** 與引數 GL \_ 色彩 \_ 材質 \_ 臉部

[](glisenabled.md)具有引數 GL \_ 色彩 \_ 材質的 glIsEnabled

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





