---
title: 'glEdgeFlagPointer 函式 (Gl) '
description: GlEdgeFlagPointer 函式會定義邊緣旗標的陣列。
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- glEdgeFlagPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa648a15542a3f3f2f35f577760991da74bc978c0464c1373c8eddea38941a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061636"
---
# <a name="gledgeflagpointer-function"></a>glEdgeFlagPointer 函式

**GlEdgeFlagPointer** 函式會定義邊緣旗標的陣列。

## <a name="syntax"></a>語法


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*大步* 
</dt> <dd>

連續邊緣旗標之間的位元組位移。 當 *stride* 為零時，邊緣旗標會緊密地封裝在陣列中。

</dd> <dt>

*指標* 
</dt> <dd>

陣列中第一個邊緣旗標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                             | 意義                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl> | *stride* 或 *計數* 為負數。<br/> |



## <a name="remarks"></a>備註

**GlEdgeFlagPointer** 函式會指定轉譯時要使用的布林邊緣旗標陣列的位置和資料。 *Stride* 參數會決定從某個邊緣旗標到下一個邊緣旗標的位元組位移，這可將單一陣列或儲存區中的頂點和屬性封裝成不同的陣列。 在某些情況下，將頂點和屬性儲存在單一陣列中的效率可能比使用個別陣列更有效率。

當您 \_ 使用 glEnableClientState 指定 GL edge \_ 旗標 \_ 陣列常數[](glenableclientstate.md)時，會啟用邊緣旗標陣列。 啟用時， [**glDrawArrays**](gldrawarrays.md) 或 [**glArrayElement**](glarrayelement.md) 會使用邊緣旗標陣列。 Edge 旗標陣列預設為停用。

您可以使用 **glDrawArrays** 來建立一系列的基本類型， (預先指定頂點和頂點屬性陣列中) 的所有相同型別。 您可以使用 **glArrayElement** ，藉由為頂點和頂點屬性編制索引來指定基本專案，並透過編制頂點和頂點屬性的索引， [**glDrawElements**](gldrawelements.md) 來建立基本類型的序列。

您無法在顯示清單中包含 **glEdgeFlagPointer** 。

當您使用 **glEdgeFlagPointer** 指定邊緣旗標陣列時，所有函式的邊緣旗標陣列參數值都會儲存在用戶端狀態中，而且可以快取靜態陣列元素。 由於 edge 旗標陣列參數處於用戶端狀態， [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 不會儲存或還原它們的值。

雖然在 [**glBegin**](glbegin.md) / [**glend**](glend.md)配對內呼叫 glEdgeFlagPointer 並不會產生錯誤，但結果是未定義的。

下列函式會取出與 **glEdgeFlagPointer** 函數相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 邊緣 \_ 旗標 \_ 陣列 \_ STRIDE 的 glGet

具有引數 GL \_ EDGE \_ 旗標 \_ 陣列 \_ 計數的 glGet

[](glgetpointerv.md)具有引數 GL \_ EDGE \_ 旗標 \_ 陣列 \_ 指標的 glGetPointerv

[](glisenabled.md)具有引數 GL \_ EDGE \_ 旗標 \_ 陣列的 glIsEnabled

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

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
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

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





