---
title: 'glCallList 函式 (Gl) '
description: GlCallList 函式會執行顯示清單。
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- glCallList 函式 OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104130"
---
# <a name="glcalllist-function"></a>glCallList 函式

**GlCallList** 函式會執行顯示清單。

## <a name="syntax"></a>語法


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*list* 
</dt> <dd>

要執行之顯示清單的整數名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

叫用 **glCallList** 函式會開始執行命名的顯示清單。 儲存在顯示清單中的函式會依序執行，就如同您在未使用顯示清單的情況下呼叫它們一樣。 如果 *清單* 尚未定義為顯示清單，則會忽略 **glCallList** 。

**GlCallList** 函數可以出現在顯示清單中。 為了避免因為顯示清單彼此呼叫而產生無限遞迴的可能性，在顯示清單執行期間，會將限制放在顯示清單的嵌套層級上。 這項限制至少為64，但相依于執行。

在呼叫 **glCallList** 時，不會儲存並還原 OpenGL 狀態。 因此，在顯示清單執行期間，在顯示清單執行期間所做的變更會保留下來。 若要保留跨 **glCallList** 呼叫的 OpenGL 狀態，請使用 [**glPushAttrib**](glpushattrib.md)、 [**glPopAttrib**](glpopattrib.md)、 [**glPushMatrix**](glpushmatrix.md)和 [**glPopMatrix**](glpopmatrix.md)。

只要顯示清單只包含此間隔中允許的函式，您就可以在呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間執行顯示清單。

下列函式會取出與 **glCallList** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ 清單 \_ 嵌套的 glGet

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

[**glCallLists**](glcalllists.md)
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

 

 





