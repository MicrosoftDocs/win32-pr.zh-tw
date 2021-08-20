---
title: 'glNormalPointer 函式 (Gl) '
description: GlNormalPointer 函式定義了法線的陣列。
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- glNormalPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f188a65a0a2bff0438188ae7521615de45341147b138a849d2fd375ed8a959b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938407"
---
# <a name="glnormalpointer-function"></a>glNormalPointer 函式

**GlNormalPointer** 函式定義了法線的陣列。

## <a name="syntax"></a>語法


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*type* 
</dt> <dd>

陣列中每個座標的資料類型，使用下列符號常數： GL \_ BYTE、gl \_ SHORT、GL \_ INT、GL \_ FLOAT 和 gl \_ DOUBLE。

</dd> <dt>

*大步* 
</dt> <dd>

連續法線之間的位元組位移。 當 *stride* 為零時，就會將法線緊密地封裝在陣列中。

</dd> <dt>

*指標* 
</dt> <dd>

陣列中第一個法線的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *類型* 不是可接受的值。<br/> |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | *stride* 或 *計數* 為負數。<br/> |



## <a name="remarks"></a>備註

**GlNormalPointer** 函式會指定轉譯時要使用之法線陣列的位置和資料。 *Type* 參數指定每個一般座標的資料類型。 *Stride* 參數會決定從一個標準到下一個標準的位元組位移，以便將單一陣列或儲存區中的頂點和屬性封裝成不同的陣列。 在某些執行中，將頂點和屬性儲存在單一陣列中的效率可能比使用個別陣列更有效率;如需詳細資訊，請參閱 [**glInterleavedArrays**](glinterleavedarrays.md) 。

當您 \_ \_ 使用 [**glEnableClientState**](glenableclientstate.md)指定 GL 一般陣列常數時，會啟用一般陣列。 啟用時， [**glDrawArrays**](gldrawarrays.md)、 [**glDrawElements**](gldrawelements.md) 和 [**glArrayElement**](glarrayelement.md) 會使用一般陣列。 預設會停用一般陣列。

您無法在顯示清單中包含 **glNormalPointer** 。

當您使用 **glNormalPointer** 指定一般陣列時，所有函式的一般陣列參數值都會儲存在用戶端狀態。 由於一般陣列參數會儲存在用戶端狀態中，因此 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md)不會儲存或還原它們的值。

雖然在 [**glBegin**](glbegin.md)和 [**glEnd**](glend.md)配對內呼叫 **glNormalPointer** 時不會產生任何錯誤，但結果未定義。

下列是與 **glNormalPointer** 相關聯的函式：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 標準 \_ 陣列 \_ STRIDE 的 glGet

具有引數 GL \_ 標準 \_ 陣列 \_ 計數的 glGet

具有引數 GL \_ 一般 \_ 陣列 \_ 類型的 glGet

具有引數 GL \_ 一般 \_ 陣列 \_ 指標的 glGetPointerv

[](glisenabled.md)具有引數 GL \_ 一般 \_ 陣列的 glIsEnabled

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> </dl>

 

 





