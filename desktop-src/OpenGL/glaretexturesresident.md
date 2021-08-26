---
title: 'glAreTexturesResident 函式 (Gl) '
description: GlAreTexturesResident 函式會判斷指定的材質物件是否常駐在材質記憶體中。
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- glAreTexturesResident 函式 OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c503cac59bbec912c535120161d27991118dab818a185c1f39d8f48cb2a5939
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082238"
---
# <a name="glaretexturesresident-function"></a>glAreTexturesResident 函式

**GlAreTexturesResident** 函式會判斷指定的材質物件是否常駐在材質記憶體中。

## <a name="syntax"></a>語法


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*n* 
</dt> <dd>

要查詢的材質數目。

</dd> <dt>

*紋理* 
</dt> <dd>

陣列的位址，其中包含要查詢之材質的名稱。

</dd> <dt>

*住宅* 
</dt> <dd>

傳回紋理居住狀態的陣列位址。 以 *紋理* 元素命名之材質的居住狀態會在 *residences* 的對應元素中傳回。

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *n* 為負值、 *材質* 中的元素為零，或 *紋理* 中的元素未包含材質識別碼。<br/> |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/>     |



## <a name="remarks"></a>備註

在數量有限的材質記憶體的電腦上，OpenGL 會建立一組可在材質記憶體中使用的材質。 這些紋理可以更有效率地系結至紋理目標，比不是常駐的材質更有效率。

**GlAreTexturesResident** 函式會 *查詢紋理的* 元素所命名之 *n* 紋理的材質居住狀態。 如果所有命名紋理都是常駐的， **glAreTexturesResident** 會傳回 GL \_ TRUE，而 *residences* 的內容不會受到干擾。 如果任何已命名的紋理都不存在，則 **glAreTexturesResident** 會 \_ 傳回 GL FALSE，並在 *residences* 的 *n* 個元素中傳回詳細的狀態。

如果 *residences* 的元素是 GL \_ TRUE，則由 *紋理的* 對應元素所命名的材質會在材質記憶體中。

若要查詢單一系結材質的居住狀態，請呼叫 [**glGetTexParameter**](glgettexparameter.md) ，並將 *目標* 參數設定為目標材質（目標材質），並將 *PNAME* 參數設定為 [GL \_ 紋理常駐] \_ 。 您必須使用這個方法來查詢預設材質的常駐狀態。

您無法在顯示清單中包含 **glAreTexturesResident** 。

**GlAreTexturesResident** 函式會在叫用時，傳回紋理的常駐狀態。 這並不保證紋理會在任何其他時間保持存留。

如果材質位於虛擬記憶體中 (沒有紋理記憶體) ，則會被視為持續存在。

> [!Note]  
> **GlAreTexturesResident** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





