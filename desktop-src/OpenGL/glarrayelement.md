---
title: 'glArrayElement 函式 (Gl) '
description: GlArrayElement 函式會指定用來呈現頂點的陣列元素。
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- glArrayElement 函式 OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967340"
---
# <a name="glarrayelement-function"></a>glArrayElement 函式

**GlArrayElement** 函式會指定用來呈現頂點的陣列元素。

## <a name="syntax"></a>語法


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*index* 
</dt> <dd>

啟用的陣列中的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

使用 [**glBegin**](glbegin.md)和 [**glEnd**](glend.md)配對內的 **glArrayElement** 函式來指定點、線條和多邊形基本專案的頂點和屬性資料。 **GlArrayElement** 函式會使用位於已啟用頂點陣列 *索引* 的頂點和屬性資料，來指定單一頂點的資料。

您可以使用 **glArrayElement** 來建立基本資料，方法是編制頂點資料的索引，而不是在第一次到最後一個訂單的資料陣列之間進行串流處理。 因為 **glArrayElement** 只會指定單一頂點，所以您可以明確指定個別基本專案的屬性。 例如，您可以針對每個個別的三角形設定單一一般。

當您在顯示清單中包含 **glArrayElement** 的呼叫時，顯示清單中也會輸入必要的陣列資料（由陣列指標和啟用值所決定）。 陣列指標和啟用值是在顯示清單建立時決定，而不是在執行顯示清單時決定。

您可以隨時使用 **glArrayElement** 來讀取和快取靜態陣列資料。 當您修改靜態陣列的元素而未再次指定陣列時，任何後續呼叫 **glArrayElement** 的結果都是未定義的。

當您呼叫 **glArrayElement** 時，若未先呼叫 **glEnableClientState** (GL \_ 頂點 \_ 陣列) ，就不會進行任何繪製，但是會修改對應到已啟用陣列的屬性。 雖然當您在 **glBegin** 和 **glEnd** 配對內指定陣列時，不會產生任何錯誤，但結果是未定義的。

> [!Note]  
> **GlArrayElement** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





