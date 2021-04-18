---
title: 'glVertexPointer 函式 (Gl) '
description: GlVertexPointer 函式會定義頂點資料的陣列。
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- glVertexPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466316"
---
# <a name="glvertexpointer-function"></a>glVertexPointer 函式

**GlVertexPointer** 函式會定義頂點資料的陣列。

## <a name="syntax"></a>語法


```C++
void WINAPI glVertexPointer(
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

每個頂點的座標數目。 *大小* 的值必須是2、3或4。

</dd> <dt>

*type* 
</dt> <dd>

陣列中每個座標的資料類型，使用下列符號常數： GL \_ SHORT、gl \_ INT、gl \_ FLOAT 和 gl \_ DOUBLE。

</dd> <dt>

*大步* 
</dt> <dd>

連續頂點之間的位元組位移。 當 *stride* 為零時，就會將頂點緊密地封裝在陣列中。

</dd> <dt>

*指標* 
</dt> <dd>

陣列中第一個頂點的第一個座標指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                              | 意義                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl> | *大小* 不是2、3或4。 <br/>        |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>  | *類型* 不是可接受的值。<br/>  |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl> | *stride* 或 *計數* 為負數。 <br/> |



## <a name="remarks"></a>備註

**GlVertexPointer** 函式會指定要在轉譯時使用之頂點座標陣列的位置和資料。 *Size* 參數指定每個頂點的座標數目。 *Type* 參數指定每個頂點座標的資料類型。 *Stride* 參數會決定從某個頂點到下一個頂點的位元組位移，以便將單一陣列或儲存區中的頂點和屬性封裝成不同的陣列。 在某些情況下，在單一陣列中儲存頂點和屬性，會比使用不同的陣列更有效率 (請參閱 [**glInterleavedArrays**](glinterleavedarrays.md)) 。

當您 \_ \_ 使用 [**glEnableClientState**](glenableclientstate.md)指定 GL 頂點陣列常數時，會啟用頂點陣列。 啟用時， [**glDrawArrays**](gldrawarrays.md)、 [**glDrawElements**](gldrawelements.md)和 [**glArrayElement**](glarrayelement.md) 會使用頂點陣列。 預設會停用頂點陣列。

您無法在顯示清單中包含 **glVertexPointer** 。

當您使用 **glVertexPointer** 指定頂點陣列時，所有函式之頂點陣列參數的值都會儲存在用戶端狀態中，而且可以快取靜態陣列元素。 因為頂點陣列參數是用戶端狀態，所以它們的值不會由 [**glPushAttrib**](glpushattrib.md) 和 **glPopAttrib** 儲存或還原。

雖然在 [**glBegin**](glbegin.md)和 [**glEnd**](glend.md)配對內呼叫 **glVertexPointer** 時不會產生任何錯誤，但結果未定義。

下列函式會取出與 **glVertexPointer** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 頂點 \_ 陣列 \_ 大小的 glGet

具有引數 GL \_ 頂點 \_ 陣列 \_ STRIDE 的 glGet

具有引數 GL \_ 頂點 \_ 陣列 \_ 計數的 glGet

具有引數 GL \_ 頂點 \_ 陣列 \_ 類型的 glGet

[](glgetpointerv.md)具有引數 GL \_ 頂點 \_ 陣列 \_ 指標的 glGetPointerv

[](glisenabled.md)具有引數 GL \_ 頂點 \_ 陣列的 glIsEnabled

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> </dl>

 

 





