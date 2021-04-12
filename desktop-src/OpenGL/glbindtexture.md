---
title: 'glBindTexture 函式 (Gl) '
description: GlBindTexture 函數可讓您建立系結至材質目標的命名材質。
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- glBindTexture 函式 OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384829"
---
# <a name="glbindtexture-function"></a>glBindTexture 函式

**GlBindTexture** 函數可讓您建立系結至材質目標的命名材質。

## <a name="syntax"></a>語法


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

材質所系結的目標。 必須具有值 GL \_ 紋理 \_ 1D 或 GL \_ 紋理 \_ 2d。

</dd> <dt>

*紋理* 
</dt> <dd>

材質的名稱;材質名稱目前無法使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | 參數 *目標* 不是可接受的值。<br/>                                                                                                                                                       |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 參數 *材質* 沒有與 *目標* 相同的維度，或呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlBindTexture** 函數可讓您建立命名紋理。 將 *目標* 設定為 GL  \_ 紋理 \_ 1d 或 gl \_ 材質 \_ 2d，並將材質設定為您所建立之新材質的名稱時，會將材質名稱系結至適當的材質目標，來呼叫 glBindTexture。 當材質系結至目標時，該目標的先前系結將不再有效。

材質名稱是一種不帶正負號的整數，其值為零，表示每個材質目標的預設材質。 材質名稱和對應的材質內容位於目前 OpenGL 轉譯內容的共用顯示清單空間區域中;只有當兩個轉譯內容也共用顯示清單時，才會共用材質名稱。 您可以使用 [**glGenTextures**](glgentextures.md)來產生一組新的材質名稱。

第一次系結材質時，它會假設其材質目標的維度。系結至 GL \_ 紋理1d 的材質 \_ 會變成一維，且系結至 gl \_ 材質2d 的材質 \_ 會變成二維。 您在紋理目標上執行的作業也會影響系結至目標的材質。 當您查詢材質目標時，傳回值會是所系結之材質的狀態。 紋理目標會成為目前系結之紋理的別名。

當您使用 **glBindTexture** 系結材質時，系結會保持作用中，直到不同的材質系結至相同的目標，或使用 [**glDeleteTextures**](gldeletetextures.md) 函式刪除系結的材質為止。 建立命名材質之後，您可以將它系結至具有相同維度的材質目標（視需要一樣）。

使用 **glBindTexture** 將現有的指名材質系結至其中一個材質目標，通常會比使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)重載紋理影像更快。 若要進一步控制紋理效能，請使用 [**glPrioritizeTextures**](glprioritizetextures.md)。

您可以在顯示清單中加入 **glBindTexture** 的呼叫。

> [!Note]  
> **GlBindTexture** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

下列函式會取出與 **glBindTexture** 相關的資訊：

-   [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 紋理 \_ 1D 系結的 glGet \_

具有引數 GL \_ 材質 \_ 2D 系結的 glGet \_

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

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





