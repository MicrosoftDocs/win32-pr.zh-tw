---
title: 'glInterleavedArrays 函式 (Gl) '
description: GlInterleavedArrays 函式會同時指定並啟用大型匯總陣列中的數個交錯陣列。
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- glInterleavedArrays 函式 OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3b37186614fa431585c1e5a932edab946afd6d881ba1cf8eb5c5690220f603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938559"
---
# <a name="glinterleavedarrays-function"></a>glInterleavedArrays 函式

**GlInterleavedArrays** 函式會同時指定並啟用大型匯總陣列中的數個交錯陣列。

## <a name="syntax"></a>語法


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*format* 
</dt> <dd>

要啟用的陣列類型。 參數可以採用下列其中一個符號值： GL \_ V2F、gl \_ V3F、gl \_ C4UB \_ V2F、GL \_ C4UB \_ V3F、gl \_ C3F \_ V3F、gl \_ N3F V3F、gl C4F N3F V3F、 \_ \_ gl T2F \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ V3F、gl T4F V4F、gl T2F C4UB V3F、gl T2F C3F V3F、gl T2F N3F V3F、gl T2F C4F N3F V3F 或 gl T4F C4F N3F V4F。

</dd> <dt>

*大步* 
</dt> <dd>

每個匯總陣列元素之間的位移（以位元組為單位）。

</dd> <dt>

*指標* 
</dt> <dd>

匯總陣列中第一個元素的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *格式* 不是可接受的值。<br/>                                                                                        |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *stride* 為負數值。<br/>                                                                                             |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

使用 **glInterleavedArrays** 函式，您可以同時指定並啟用數個交錯色彩、標準、材質和頂點陣列，其專案是較大的匯總陣列元素的一部分。 針對某些記憶體架構，這比個別指定陣列更有效率。

如果 *stride* 參數為零，則會連續儲存匯總陣列元素;否則，在匯總陣列元素之間會發生 *跨距* 位元組。

*Format* 參數可做為描述如何從匯總陣列解壓縮個別陣列的索引鍵：

-   如果 *格式* 包含 T，則會從交錯的陣列中解壓縮紋理座標。
-   如果有 C，則會將色彩值解壓縮。
-   如果有 N，則會將一般座標解壓縮。
-   一律會將頂點座標解壓縮。
-   數位2、3和4表示要解壓縮的值數目。
-   F 表示將值解壓縮為浮點值。
-   如果4UB 遵循 C，則色彩也可以解壓縮為4個不帶正負號的位元組。 如果將色彩解壓縮為4個不帶正負號的位元組，後面的頂點陣列元素會位於第一個可能的浮點對齊位址。

如果您在編譯顯示清單時呼叫 **glInterleavedArrays** ，它不會編譯成清單，而是會立即執行。

在對 [**glBegin**](glbegin.md)的呼叫和 **glEnd** 的對應呼叫之間，不能包含 **glDisableClientState** 的 **glInterleavedArrays** 呼叫。

> [!Note]  
> **GlInterleavedArrays** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

**GlInterleavedArrays** 函式是在不含通訊協定的用戶端上執行。 因為頂點陣列參數是用戶端狀態，所以它們不會由 [**glPushAttrib**](glpushattrib.md) 和 **glPopAttrib** 儲存或還原。 請改用 [**glPushClientAttrib**](glpushclientattrib.md) 和 **glPopClientAttrib** 。

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

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





