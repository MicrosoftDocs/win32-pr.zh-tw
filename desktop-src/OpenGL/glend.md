---
title: 'glEnd 函式 (Gl) '
description: 'GlBegin 和 glend 函式會分隔基本或類似基本類型群組的頂點。 |glEnd 函式 (Gl) '
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- glEnd 函式 OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986466"
---
# <a name="glend-function"></a>glEnd 函式

[**GlBegin**](glbegin.md)和 **glend** 函式會分隔基本或類似基本類型群組的頂點。

## <a name="syntax"></a>語法


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | **GlVertex**、 **glColor**、 **glIndex**、 **glNormal**、 **glTexCoord**、 **glEvalCoord**、 **glEvalPoint**、 **glMaterial**、 **glEdgeFlag**、 **glCallList** 或 **glCallLists** 以外的函式會在 **glBegin** 與對應的 **glEnd** 之間呼叫。 函數 **glEnd** 是在呼叫對應的 **glBegin** 之前呼叫，或在 **glBegin** / **glEnd** 序列內呼叫 glBegin。 <br/> |



## <a name="remarks"></a>備註

[**GlBegin**](glbegin.md)和 **glend** 函式會分隔定義基本或類似基本類型群組的頂點。 **GlBegin** 函式會接受單一引數，以指定頂點所組成的10個基本類型。 從1開始，將 *n* 做為整數計數，而 *n* 則是指定的頂點總數，如下所示：

-   您只能在 **glBegin** 與 **GlEnd** 之間使用 OpenGL 函數的子集。 您可以使用的函數如下：

    -   [**glVertex**](glvertex-functions.md)
    -   [**glColor**](glcolor-functions.md)
    -   [**glIndex**](glindex-functions.md)
    -   [**glNormal**](glnormal-functions.md)
    -   [**glTexCoord**](gltexcoord-functions.md)
    -   [**glEvalCoord**](glevalcoord-functions.md)
    -   [**glEvalPoint**](glevalpoint.md)
    -   [**glMaterial**](glmaterial-functions.md)
    -   [**glEdgeFlag**](gledgeflag-functions.md)

    您也可以使用 [**glCallList**](glcalllist.md) 或 [**glCallLists**](glcalllists.md) 來執行只包含上述函式的顯示清單。 如果在 **glBegin** 和 **glEnd** 之間呼叫任何其他 OpenGL 函數，則會設定錯誤旗標，並忽略函式。

-   無論在 **glBegin** 中為 *模式* 選擇的值為何，您可以在 **glBegin** 和 **glEnd** 之間定義的頂點數目沒有任何限制。 未完整指定的線條、三角形、quadrilaterals 和多邊形都不會繪製。 當提供的頂點太少以指定單一基本或指定了不正確的頂點倍數時，不完整的規格結果。 忽略不完整的基本類型;繪製完整的基本專案。
-   每個基本類型頂點的最小規格為： 

    | 頂點的最小數目 | 基本類型 |
    |----------------------------|-------------------|
    | 1                          | 點             |
    | 2                          | line              |
    | 3                          | 三角形          |
    | 4                          | 四邊形     |
    | 3                          | 多邊形           |

    

     

-   需要特定多個頂點的模式為 GL \_ 行 (2) 、gl \_ 三角形 (3) 、gl \_ 四邊形 (4) 和 GL 四 \_ \_ 個 () 。

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

[**glBegin**](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

