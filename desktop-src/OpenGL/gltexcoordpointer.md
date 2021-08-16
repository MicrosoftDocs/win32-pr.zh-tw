---
title: 'glTexCoordPointer 函式 (Gl) '
description: GlTexCoordPointer 函式會定義材質座標的陣列。
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- glTexCoordPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0892f06b3fd5027939710be9ac74a2ae18c0dc0d712572d094b9a54fd6bb5b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888248"
---
# <a name="gltexcoordpointer-function"></a>glTexCoordPointer 函式

**GlTexCoordPointer** 函式會定義材質座標的陣列。

## <a name="syntax"></a>語法


```C++
void WINAPI glTexCoordPointer(
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

每個陣列元素的座標數目。 *大小* 的值必須是1、2、3或4。

</dd> <dt>

*type* 
</dt> <dd>

陣列中每個材質座標的資料類型，使用下列符號常數： **GL \_ SHORT**、 **gl \_ INT**、 **gl \_ FLOAT** 和 **gl \_ DOUBLE**。

</dd> <dt>

*大步* 
</dt> <dd>

連續陣列元素之間的位元組位移。 當 *stride* 為零時，陣列元素會緊密地封裝在陣列中。

</dd> <dt>

*指標* 
</dt> <dd>

陣列中第一個元素的第一個座標指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                              | 意義                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>  | *類型* 不是可接受的值。<br/> |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl> | *大小* 不是1、2、3或4。<br/>     |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl> | *stride* 為負數。<br/>            |



## <a name="remarks"></a>備註

**GlTexCoordPointer** 函式會指定轉譯時要使用之材質座標陣列的位置和資料。*Size* 參數會指定陣列中每個元素所使用的座標數目。*Type* 參數指定每個材質座標的資料類型。 *Stride* 參數會決定從某個陣列元素到下一個陣列專案的位元組位移，以便將單一陣列或儲存區中的頂點和屬性封裝成不同的陣列。 在某些情況下，將頂點和屬性儲存在單一陣列中的效率可能比使用個別陣列更有效率。 如需詳細資訊，請參閱 [**glInterleavedArrays**](glinterleavedarrays.md)。 當指定紋理座標陣列時，大小、類型、跨距和指標都會儲存用戶端狀態。

當您使用 [**glEnableClientState**](glenableclientstate.md)指定 **GL \_ 紋理 \_ COORD \_ 陣列** 常數時，會啟用紋理座標陣列。 啟用時， [**glDrawArrays**](gldrawarrays.md)、 [**glDrawElements**](gldrawelements.md)和 [**glArrayElement**](glarrayelement.md) 會使用材質座標陣列。 紋理座標陣列預設為停用。

您無法在顯示清單中包含 **glTexCoordPointer** 。

當您使用 **glTexCoordPointer** 指定紋理座標陣列時，所有函式的材質座標陣列參數值都會儲存在用戶端狀態中，而且可以快取靜態陣列元素。 因為材質座標陣列參數是用戶端狀態，所以它們的值不會由 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md)儲存或還原。

雖然在 [**glBegin**](glbegin.md)和 [**glEnd**](glend.md)配對內呼叫 **glTexCoordPointer** 時不會產生任何錯誤，但結果未定義。

下列函式會取出與 **glTexCoordPointer** 相關的資訊：

具有引數 **GL \_ 紋理 \_ COORD \_ 陣列** 的 [**glIsEnabled**](glisenabled.md)

具有引數 **GL \_ 紋理 \_ COORD \_ 陣列 \_ 大小** 的 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)

**glGet** 與引數 **GL \_ 紋理 \_ COORD \_ 陣列 \_ STRIDE**

具有引數 **GL \_ 紋理 \_ COORD \_ 陣列 \_ 計數** 的 **glGet**

具有引數 **GL \_ 紋理 \_ COORD \_ 陣列 \_ 類型** 的 **glGet**

具有引數 **GL \_ 紋理 \_ COORD \_ 陣列 \_ 指標** 的 [**glGetPointerv**](glgetpointerv.md)

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
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

[**glPopClientAttrib**](glpopclientattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





