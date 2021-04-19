---
title: 'glPopAttrib 函式 (Gl) '
description: 彈出屬性堆疊。
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- glPopAttrib 函式 OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968171"
---
# <a name="glpopattrib-function"></a>glPopAttrib 函式

彈出屬性堆疊。

## <a name="syntax"></a>語法


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 堆疊 \_ 下溢**</dt> </dl>   | 當屬性堆疊是空的時，就會呼叫此函式。<br/>                                                               |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

[**GlPushAttrib**](glpushattrib.md)函式會採用一個引數，此遮罩會指出要在屬性堆疊上儲存的狀態變數群組。 符號常數用來設定遮罩中的位。 Mask 參數通常是由 **或** 將數個常陣列成。 特殊遮罩 GL \_ 所有的 \_ ATTRIB \_ 位都可以用來儲存所有可堆疊的狀態。

**GlPopAttrib** 函式會還原使用 last [**glPushAttrib**](glpushattrib.md)命令所儲存之狀態變數的值。 未儲存的會保持不變。

將屬性推送至完整堆疊，或從空白堆疊取出屬性是錯誤的。 在任一種情況下，都會設定錯誤旗標，且不會對 OpenGL 狀態進行其他變更。

一開始，屬性堆疊是空的。

並非所有 OpenGL 狀態的值都可以儲存在屬性堆疊上。 例如，您無法儲存圖元 pack 和解除封裝狀態、轉譯模式狀態，以及選取和意見反應狀態。

屬性堆疊的深度取決於執行，但必須至少為16。

下列函式會取出 [**glPushAttrib**](glpushattrib.md) 和 **glPopAttrib** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ ATTRIB \_ STACK \_ 深度的 glGet

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ ATTRIB 參數 \_ 堆疊 \_ 深度的 glGet

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

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





