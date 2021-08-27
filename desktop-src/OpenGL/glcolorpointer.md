---
title: 'glColorPointer 函式 (Gl) '
description: GlColorPointer 函式會定義色彩的陣列。
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- glColorPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e08f046cc1bd41293a076f36389506320e85025e415b264bed1ed0de14f9a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081708"
---
# <a name="glcolorpointer-function"></a>glColorPointer 函式

**GlColorPointer** 函式會定義色彩的陣列。

## <a name="syntax"></a>語法


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*size* 
</dt> <dd>

每一色彩的元件數目。 值必須是3或4。

</dd> <dt>

*type* 
</dt> <dd>

色彩陣列中每個色彩元件的資料類型。 您可以使用下列常數指定可接受的資料類型： GL \_ 位元組、gl \_ 無符號 \_ 位元組、GL \_ short、gl 不 \_ 帶正負號 \_ 簡短、gl \_ int、GL 不 \_ 帶正負號 \_ INT、gl \_ FLOAT 或 GL \_ DOUBLE。

</dd> <dt>

*大步* 
</dt> <dd>

連續色彩之間的位元組位移。 當 *stride* 為零時，色彩會緊密地封裝在陣列中。

</dd> <dt>

*指標* 
</dt> <dd>

色彩陣列中第一個 color 元素第一個元件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                              | 意義                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl> | *大小* 不是3或4。<br/>            |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>  | *類型* 不是可接受的值。<br/> |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl> | *stride* 或 *計數* 為負數。<br/> |



## <a name="remarks"></a>備註

**GlColorPointer** 函式會指定轉譯時要使用之色彩元件陣列的位置和資料格式。 *Stride* 參數會決定從某種色彩到下一個色彩的位元組位移，以便將單一陣列或儲存區中的頂點屬性封裝成不同的陣列。 在某些情況下，在單一陣列中儲存頂點屬性，會比使用個別陣列更有效率。

藉由 \_ \_ 使用 [**glEnableClientState**](glenableclientstate.md)指定 GL 色彩陣列常數來啟用色彩陣列。 呼叫 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md) 會使用因此啟用的色彩陣列。 預設會停用色彩陣列。 **GlColorPointer** 呼叫不能藉由在顯示清單中輸入。

當您使用 **glColorPointer** 指定色彩陣列時，所有函式的色彩陣列參數值都會儲存在用戶端狀態，而且您可以快取靜態陣列元素。 因為色彩陣列參數處於用戶端狀態， [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 不會儲存或還原參數的值。

雖然在 [**glBegin**](glbegin.md) 和 [**glend**](glend.md) 配對內指定色彩陣列並不會產生錯誤，但結果卻是未定義的。

下列函式會取出與 **glColorPointer** 函數相關的資訊：

[](glisenabled.md)具有引數 GL \_ 色彩 \_ 陣列的 glIsEnabled

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 色彩 \_ 陣列 \_ 大小的 glGet

具有引數 GL \_ 色彩 \_ 陣列 \_ 類型的 glGet

具有引數 GL \_ 色彩 \_ 陣列 \_ STRIDE 的 glGet

具有引數 GL \_ 色彩 \_ 陣列 \_ 計數的 glGet

[](glgetpointerv.md)具有引數 GL \_ 色彩 \_ 陣列 \_ 指標的 glGetPointerv

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

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





