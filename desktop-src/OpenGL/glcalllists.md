---
title: 'glCallLists 函式 (Gl) '
description: GlCallLists 函式會執行顯示清單清單。
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- glCallLists 函式 OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934514"
---
# <a name="glcalllists-function"></a>glCallLists 函式

**GlCallLists** 函式會執行顯示清單清單。

## <a name="syntax"></a>語法


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*n* 
</dt> <dd>

要執行的顯示清單數目。

</dd> <dt>

*type* 
</dt> <dd>

*清單* 中的數值型別。 接受下列符號常數。



| 值                                                                                                                                                                      | 意義                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ 位元組**</dt> </dl>                                | List *參數會* 被視為帶正負號之位元組的陣列，每個都在128到127的範圍中。<br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL 不 \_ 帶正負號的 \_ 位元組**</dt> </dl>    | *Lists* 參數會被視為不帶正負號的位元組陣列，每個都在0到255的範圍內。<br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ 短期**</dt> </dl>                             | *Lists* 參數會被視為帶正負號的2位元組整數陣列，每個都在範圍-32768 到32767之間。<br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL 不 \_ 帶正負號 \_ 簡短**</dt> </dl> | *Lists* 參數會被視為不帶正負號的2位元組整數陣列，每個都在0到65535的範圍內。<br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | *Lists* 參數會被視為帶正負號之4位元組整數的陣列。<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL 不 \_ 帶正負號 \_ INT**</dt> </dl>       | *Lists* 參數會被視為不帶正負號4位元組整數的陣列。<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | *Lists* 參數會被視為4位元組、浮點值的陣列。<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <dt>**GL \_ 2 \_ 個位元組**</dt> </dl>                      | *Lists* 參數會被視為不帶正負號的位元組陣列。 每一對位元組都指定單一顯示清單名稱。 配對的值會計算為第一個位元組不帶正負號值的256倍加上第二個位元組的不帶正負號值。<br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <dt>**GL \_ 3 \_ 位元組**</dt> </dl>                      | *Lists* 參數會被視為不帶正負號的位元組陣列。 每三個位元組都指定單一顯示清單名稱。 三元的值會計算為第一個位元組不帶正負號值的65536倍，加上第二個位元組不帶正負號值的256倍，再加上第三個位元組的不帶正負號值。<br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <dt>**GL \_ 4 \_ 位元組**</dt> </dl>                      | *Lists* 參數會被視為不帶正負號的位元組陣列。 每個位元組 quadruplet 會指定單一顯示清單名稱。 Quadruplet 的值會計算為第一個位元組不帶正負號值的16777216倍，加上第二個位元組不帶正負號值的65536倍，加上第三個位元組不帶正負號值的256倍，再加上第四個位元組的不帶正負號值。<br/> |



 

</dd> <dt>

*清單* 
</dt> <dd>

顯示清單中名稱位移陣列的位址。 指標類型為 void，因為位移可以是位元組、短、整數或浮點數，這取決於 *類型* 的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GlCallLists** 函式會將名稱清單中的每個顯示清單視為 *要執行的清單。* 因此，儲存在每個顯示清單中的函式會依序執行，就像在不使用顯示清單的情況下呼叫一樣。 未定義的顯示清單名稱將會被忽略。

**GlCallLists** 函式提供一種有效率的方式來執行顯示清單。 *N* 參數會指定) **glCallLists** 執行的 *類型* 參數所指定的不同名稱格式 (清單數目。

顯示清單名稱的清單不是以 null 結束。 相反地， *n* 指定要從 *清單* 中取得多少名稱。

[**GlListBase**](gllistbase.md)函式可提供額外的間接取值層級。 **GlListBase** 函式會指定不帶正負號的位移，該位移會新增至 *清單* 中指定的每個顯示清單名稱，再執行該顯示清單。

**GlCallLists** 函數可以出現在顯示清單中。 為了避免因為顯示清單彼此呼叫而產生無限遞迴的可能性，在顯示清單執行期間，會在顯示清單的嵌套層級上設定限制。 此限制必須至少為64，且取決於執行。

在呼叫 **glCallLists** 時，不會儲存並還原 OpenGL 狀態。 因此，在執行完成之後，在顯示清單執行期間對 OpenGL 狀態所做的變更仍會保留。 使用 [**glPushAttrib**](glpushattrib.md)、 [**glPopAttrib**](glpopattrib.md)、 [**glPushMatrix**](glpushmatrix.md)和 [**glPopMatrix**](glpopmatrix.md) ，可在 **glCallLists** 呼叫之間保留 OpenGL 狀態。

只要顯示清單只包含此間隔中允許的函式，您就可以在呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間執行顯示清單。

下列函式會取出與 **glCallLists** 函數相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 清單 \_ 基底的 glGet

具有引數 GL \_ 最大 \_ 清單 \_ 嵌套的 glGet

[**glIsList**](glislist.md)

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glListBase**](gllistbase.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





