---
title: 'glDrawArrays 函式 (Gl) '
description: GlDrawArrays 函數會指定多個要轉譯的基本專案。
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- glDrawArrays 函式 OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349ba3407d84d66afd431d14c3fc97b151661f4f783a05734a55d9ba1dc313ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616990"
---
# <a name="gldrawarrays-function"></a>glDrawArrays 函式

**GlDrawArrays** 函數會指定多個要轉譯的基本專案。

## <a name="syntax"></a>語法


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

要轉譯的基本類型。 下列常數指定可接受的基本類型： GL \_ 點、gl \_ 行 \_ 帶、gl \_ 線 \_ 迴圈、gl \_ 線、gl \_ 三角形區域 \_ 、gl \_ 三角形 \_ 風扇、gl \_ 三角形、gl \_ 四個區域 \_ 、gl \_ 四邊形和 gl \_ 多邊形。

</dd> <dt>

*first* 
</dt> <dd>

啟用的陣列中的起始索引。

</dd> <dt>

*計數* 
</dt> <dd>

要呈現的索引數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *計數* 為負數。<br/>                                                                                                      |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *模式* 不是可接受的值。<br/>                                                                                          |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

使用 **glDrawArrays**，您可以指定多個幾何基本型別來呈現。 除了呼叫個別的 OpenGL 函式來傳遞每個個別頂點、一般或色彩之外，您還可以指定不同的頂點、法線和色彩陣列，以定義一系列的基本專案， (所有相同種類) 與 **glDrawArrays** 的單一呼叫。

當您呼叫 **glDrawArrays** 時，會使用每個已啟用陣列的連續元素 *計數* ，從 *第一個* 元素開始，用來建立一系列幾何基本專案。 *Mode* 參數指定要建立的基本類型，以及如何使用陣列元素來建立基本專案。

**GlDrawArrays** 傳回之後，由 **glDrawArrays** 修改的頂點屬性值為未定義。 例如，如果 \_ \_ 已啟用 GL 色彩陣列，則在 **glDrawArrays** 傳回之後，目前色彩的值會是未定義的。 **GlDrawArrays** 未修改的屬性仍會定義。 如果 \_ \_ 未啟用 GL 頂點陣列，則不會產生任何幾何基本專案，但是會修改對應至已啟用陣列的屬性。

您可以在顯示清單中包含 **glDrawArrays** 。 當您在顯示清單中包含 **glDrawArrays** 時，會在顯示清單中產生並輸入必要的陣列資料（由陣列指標和啟用所決定）。 陣列指標和啟用的值會在建立顯示清單期間決定。

您可以隨時讀取靜態陣列資料。 如果已修改任何靜態陣列元素，且未再次指定陣列，則任何後續呼叫 **glDrawArrays** 的結果都是未定義的。

雖然當您在 [**glBegin**](glbegin.md) 和 [**glend**](glend.md) 配對中多次指定陣列時，不會產生任何錯誤，但結果是未定義的。

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
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

 

 





