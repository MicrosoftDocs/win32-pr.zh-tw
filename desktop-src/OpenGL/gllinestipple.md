---
title: 'glLineStipple 函式 (Gl) '
description: GlLineStipple 函數會指定行 stipple 模式。
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- glLineStipple 函式 OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f350611afa0621c1bf883e8f2ac7dc24e50362912296f15d1443e2c638b7bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493018"
---
# <a name="gllinestipple-function"></a>glLineStipple 函式

**GlLineStipple** 函數會指定行 stipple 模式。

## <a name="syntax"></a>語法


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*因素* 
</dt> <dd>

行 stipple 模式中每個位的乘數。 例如，如果 *因數* 為3，則在使用模式中的下一個位之前，會使用模式中的每個位三次。 *因數* 參數壓制至範圍 \[ 1，256， \] 預設值為一。

</dd> <dt>

*模式* 
</dt> <dd>

16位整數，其位模式會決定何時要繪製線條的片段。 第一個是使用位零，預設模式是所有的。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlLineStipple** 函數會指定行 stipple 模式。 Line stippling 會將點陣化所產生的特定片段遮罩;將不會繪製這些片段。 遮罩的達成方式是使用三個參數：16位行 stipple 模式 *模式*、重複計數 *因數*，以及整數 stipple 計數器 *s*。

每當呼叫 [**glBegin**](glbegin.md)時，計數器 *s* 就會重設為零，而在 **glBegin** (GL 行的每個行區段之前，會 \_ 產生) /**glEnd** 序列。 它會在產生單元寬度別名的每個片段之後，或在每次產生 *i* 寬線線段的每 *個片段之後* 遞增。 如果 *模式* 位 (*s*    /  *因數*) mod 16 為零，則與 count s 相關聯的 i 個片段會被遮罩。 否則會將這些片段傳送至畫面格緩衝區。 *模式* 的位零是最不重要的位。

基於 stippling 的目的，反鋸齒程式列會被視為一系列的 1x *寬度* 矩形。 矩形 *s* 會根據為別名行所描述的片段規則進行柵格化，它會計算矩形，而不是片段群組。

使用 [**glEnable**](glenable.md) 和 **glDisable** 搭配引數 GL 行 STIPPLE 來啟用或停用行 stippling \_ \_ 。 啟用時，會如上面所述套用行 stipple 模式。 停用時，就像模式是全部一樣。 一開始，行 stippling 已停用。

下列函式會取出與 **glLineStipple** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 行 \_ STIPPLE \_ 模式的 glGet

**glGet** 與引數 GL \_ 行 \_ STIPPLE \_ 重複

[](glisenabled.md)具有引數 GL \_ 行 \_ STIPPLE 的 glIsEnabled

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

[**glEnd**](glend.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





