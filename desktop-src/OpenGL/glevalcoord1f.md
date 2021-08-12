---
title: 'glEvalCoord1f 函式 (Gl) '
description: GlEvalCoord1f 函數會評估啟用的一維對應。
ms.assetid: 520e2d31-b9c2-4b06-ab61-c2c7aa18448a
keywords:
- glEvalCoord1f 函式 OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38a935c8c330c856d0abfcff18e7df30617bff9ff2b0a757d49ebc875d92b678
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616205"
---
# <a name="glevalcoord1f-function"></a>glEvalCoord1f 函式

**GlEvalCoord1f** 函數會評估啟用的一維對應。

## <a name="syntax"></a>語法


```C++
void WINAPI glEvalCoord1f(
   GLfloat u
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*u* 
</dt> <dd>

值，這個值是在上一個 [**glMap1**](glmap1.md)函式中定義之基礎函數的域座標 *u* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GlEvalCoord1f** 函式會評估在引數 *u* 啟用一維的地圖。 使用 [**glMap1**](glmap1.md)定義對應。 使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md)來啟用或停用它們。

當發出其中一個 **glEvalCoord** 函式時，會評估指定維度目前啟用的所有對應。 然後，針對每個已啟用的對應，就像是以計算的值發出對應的 OpenGL 函數。 也就是說，如果 \_ \_ 已啟用 GL MAP1 INDEX 或 gl \_ list.map2 \_ 索引，則會模擬 [**glIndex**](glindex-functions.md) 函式。 如果 \_ \_ 已啟用 gl MAP1 color \_ 4 或 gl \_ list.map2 \_ color \_ 4，則會模擬 **glcolor** 函數。 如果 GL \_ MAP1 \_ NORMAL 或 gl \_ list.map2 \_ normal 已啟用，系統會產生一般向量，而且如果有任何 GL \_ MAP1 \_ 材質 \_ COORD \_ 1、gl \_ MAP1 \_ 材質 \_ COORD \_ 2、GL \_ MAP1 \_ 材質 \_ COORD \_ 3、GL \_ MAP1 \_ 材質 \_ COORD \_ 4、gl \_ list.map2 \_ 材質 \_ COORD \_ 1、gl \_ list.map2 \_ 材質 \_ COORD \_ 2、gl \_ list.map2 \_ 材質 \_ COORD \_ 3 和 gl \_ list.map2 \_ 材質 \_ COORD \_ 4 已啟用，則會模擬適當的 [**glTexCoord**](gltexcoord-functions.md) 函數。

OpenGL 會針對已啟用的評估使用評估值（而非目前的值），而針對色彩、色彩索引、標準和材質座標使用目前的值。 不過，評估的值不會更新目前的值。 因此，如果 [**glVertex**](glvertex-functions.md) 函式與 **glEvalCoord** 函數交錯，則與 **glVertex** 函式相關聯的色彩、標準和材質座標不會受到 **glEvalCoord** 函式所產生之值的影響，但只能由最新的 [**glColor**](glcolor-functions.md)、 [**glIndex**](glindex-functions.md)、 [**glNormal**](glnormal-functions.md)和 [**glTexCoord**](gltexcoord-functions.md) 函數所影響。

下列函式會取出與 **glEvalCoord1f** 函數相關的資訊：

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 頂點 \_ 3

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 頂點 \_ 4

[](glisenabled.md)具有引數 GL \_ MAP1 \_ 索引的 glIsEnabled

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 色彩 \_ 4

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ NORMAL

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 1

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 2

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 3

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 4

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 頂點 \_ 3

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 頂點 \_ 4

[](glisenabled.md)具有引數 GL \_ List.map2 \_ 索引的 glIsEnabled

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 色彩 \_ 4

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ NORMAL

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 1

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 2

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 3

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 4

具有引數 GL 的 [**glIsEnabled**](glisenabled.md) \_ 自動 \_ 正常

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





