---
title: 'glPrioritizeTextures 函式 (Gl) '
description: GlPrioritizeTextures 函數會設定紋理的居住優先權。
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- glPrioritizeTextures 函式 OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685694"
---
# <a name="glprioritizetextures-function"></a>glPrioritizeTextures 函式

**GlPrioritizeTextures** 函數會設定紋理的居住優先權。

## <a name="syntax"></a>語法


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*n* 
</dt> <dd>

要設定優先順序的材質數目。

</dd> <dt>

*紋理* 
</dt> <dd>

陣列的第一個元素的指標，其中包含要設定優先順序的材質名稱。

</dd> <dt>

*優先 級* 
</dt> <dd>

陣列的第一個元素的指標，其中包含材質優先權。 Priority 參數的元素中 *指定的優先順序* 適用于 *材質* 參數的對應元素所命名的材質。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *n* 為負數值。<br/>                                                                                                  |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlPrioritizeTextures** 函式會將 *優先權* 參數中指定的 *n* 紋理優先順序指派給 *紋理* 參數中所命名的 *n* 紋理。 在數量有限的材質記憶體的電腦上，OpenGL 會建立位於材質記憶體中之材質的「工作集」。 這些紋理可以更有效率地系結至紋理目標，比不是常駐的材質更有效率。

藉由指定每個材質的優先順序， **glPrioritizeTextures** 函式可讓您判斷哪些材質應該是常駐的。

*優先順序* 中的材質優先順序元素會先壓制到 \[ 0.0、1.0 範圍， \] 然後再指派。 零表示最低優先順序;因此，優先順序為零的材質最不可能是常駐的。 值1.0 表示最高優先順序;因此，具有優先順序1.0 的材質最有可能是常駐的。 不過，在系結之前，不保證紋理是常駐的。

**GlPrioritizeTextures** 函式會忽略設定材質0順序的嘗試，或未對應至現有材質的任何材質名稱。 *材質* 參數所命名的任何函式都必須系結至材質目標。

如果材質目前已系結，您也可以使用 [**glTexParameter**](gltexparameter-functions.md) 函式來設定其優先順序。 這是設定預設材質優先權的唯一方式。

您可以在顯示清單中包含 **glPrioritizeTextures** 。

下列函式會抓取與 **glPrioritizeTextures** 相關之目前系結材質的優先順序：

-   [](glgettexparameter.md)具有參數名稱 GL \_ 材質 \_ 優先權的 glGetTexParameter

> [!Note]  
> **GlPrioritizeTextures** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

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

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





