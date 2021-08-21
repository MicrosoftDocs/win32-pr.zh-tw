---
title: 'glGetPointerv 函式 (Gl) '
description: GlGetPointerv 函數會傳回頂點資料陣列的位址。
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- glGetPointerv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbef5cc17a547e82dfa55876d927ef9fed87f106d9e5fa0d5d1c36a5ce269b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493918"
---
# <a name="glgetpointerv-function"></a>glGetPointerv 函式

**GlGetPointerv** 函數會傳回頂點資料陣列的位址。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pname* 
</dt> <dd>

要從下列符號常數傳回的陣列指標類型： GL \_ 色彩 \_ 陣列 \_ 指標、gl \_ EDGE 旗標 \_ \_ 陣列 \_ 指標、gl \_ 意見反應 \_ 緩衝區 \_ 指標、GL \_ 索引 \_ 陣列 \_ 指標、gl \_ 標準 \_ 陣列 \_ 指標、gl \_ 材質 \_ COORD \_ 陣列 \_ 指標、gl \_ 選取 \_ 緩衝區 \_ 指標，以及 gl \_ 頂點 \_ 陣列 \_ 指標。

</dd> <dt>

*params* 
</dt> <dd>

傳回 *pname* 所指定陣列指標的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                             | 意義                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl> | *pname* 不是可接受的值。<br/> |



## <a name="remarks"></a>備註

**GlGetPointerv** 函式會傳回陣列指標資訊。 *Pname* 參數是指定要傳回之陣列指標類型的符號常數，而 *params* 是指向放置傳回資料之位置的指標。

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

 

 





