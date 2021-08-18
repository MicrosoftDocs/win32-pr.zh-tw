---
title: 'glIndexPointer 函式 (Gl) '
description: GlIndexPointer 函式會定義色彩索引的陣列。
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- glIndexPointer 函式 OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27502420121f7373af5425e8aadffe3641ddec539a4521fe6c6bf55e6d807d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012146"
---
# <a name="glindexpointer-function"></a>glIndexPointer 函式

**GlIndexPointer** 函式會定義色彩索引的陣列。

## <a name="syntax"></a>語法


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*type* 
</dt> <dd>

陣列中每個色彩索引的資料類型，使用下列符號常數： GL \_ SHORT、gl \_ INT、GL \_ FLOAT、gl \_ DOUBLE。

</dd> <dt>

*大步* 
</dt> <dd>

連續色彩索引之間的位元組位移。 當 *stride* 為零時，色彩索引會緊密地封裝在陣列中。

</dd> <dt>

*指標* 
</dt> <dd>

陣列中第一個色彩索引的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                              | 意義                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>  | *類型* 不是可接受的值。<br/> |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl> | *stride* 或 *計數* 為負數。<br/> |



## <a name="remarks"></a>備註

**GlIndexPointer** 函式會指定轉譯時要使用之色彩索引陣列的位置和資料。 *Type* 參數指定每個色彩索引的資料類型 *，並決定* 從某個色彩索引到下一個色彩索引的位元組位移，以在單一陣列或不同陣列中的儲存區中封裝頂點和屬性。 在某些情況下，將頂點和屬性儲存在單一陣列中的效率可能比使用個別陣列更有效率。 如需詳細資訊，請參閱 [**glInterleavedArrays**](glinterleavedarrays.md)。

當您 \_ \_ 使用 [**glEnableClientState**](glenableclientstate.md)指定 GL 索引陣列常數時，會啟用色彩索引陣列。 啟用時， [**glDrawArrays**](gldrawarrays.md) 和 [**glArrayElement**](glarrayelement.md) 會使用色彩索引陣列。 預設會停用色彩索引陣列。

您無法在顯示清單中包含 **glIndexPointer** 。

當您使用 **glIndexPointer** 指定色彩索引陣列時，所有函式的色彩索引陣列參數值都會儲存在用戶端狀態，而且可以快取靜態陣列元素。 由於色彩索引陣列參數是用戶端狀態，因此 [**glPushAttrib**](glpushattrib.md) 和 **glPopAttrib** 不會儲存或還原它們的值。

雖然在 [**glBegin**](glbegin.md)和 **glEnd** 配對內呼叫 **glIndexPointer** 時不會產生任何錯誤，但結果未定義。

下列函式會取出與 **glIndexPointer** 相關的資訊：

[](glisenabled.md)具有引數 GL \_ 索引 \_ 陣列的 glIsEnabled

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 索引 \_ 陣列 \_ STRIDE 的 glGet

具有引數 GL \_ 索引 \_ 陣列 \_ 計數的 glGet

具有引數 GL \_ 索引 \_ 陣列 \_ 類型的 glGet

具有引數 GL \_ 索引 \_ 陣列 \_ 大小的 glGet

[](glgetpointerv.md)具有引數 GL \_ 索引 \_ 陣列 \_ 指標的 glGetPointerv

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

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





