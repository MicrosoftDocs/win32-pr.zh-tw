---
title: 'glPointSize 函式 (Gl) '
description: GlPointSize 函式會指定柵格點的直徑。
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- glPointSize 函式 OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969788"
---
# <a name="glpointsize-function"></a>glPointSize 函式

**GlPointSize** 函式會指定柵格點的直徑。

## <a name="syntax"></a>語法


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*size* 
</dt> <dd>

柵格化點的直徑。 預設值為1.0。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *大小* 小於或等於零。<br/>                                                                                     |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlPointSize** 函式會指定鋸齒和反鋸齒點的柵格化直徑。 使用1.0 以外的點大小有不同的效果，取決於是否已啟用點消除鋸齒。 點消除鋸齒是藉由呼叫 [**glEnable**](glenable.md) 和 **glDisable** 和引數 GL \_ 點平滑來控制 \_ 。

如果停用點消除鋸齒，則會將提供的大小四捨五入至最接近的整數來決定實際大小。  (如果四捨五入結果的值為0，則會如同點大小為1。 ) 如果舍入大小為奇數，則表示該點之圖元片段的中心點 (*x*，*y*) 會計算為

 (*x*<sub>w</sub> + .5， *y*<sub>w</sub> +. 5) 

*w* 注標表示視窗座標。 在四捨五入大小的正方形方格內的所有圖元都位於 (*x*，*y*) 組成片段。 如果大小為偶數，則中心點為

 (*x*<sub>w</sub> + .5， *y*<sub>w</sub> +. 5) 

柵格化片段的中心是在四捨五入大小的正方形內的半整數視窗座標，以 *x (x*，*y*) 為中心。 在將 nonantialiased 點進行柵格化時所產生的所有圖元片段都會指派相同的關聯資料;對應到點的頂點。

如果已啟用消除鋸齒功能，則點柵格化會為每個圖元正方形產生一個片段，而該正方形與目前的點大小 <sub>相等，並</sub>以 *y*<sub>w</sub> )  (*x* 的點為中心。 每個片段的涵蓋範圍值都是迴圈區域與對應圖元正方形交集的視窗座標區域。 此值會儲存並用於最後的點陣化步驟中。 與每個片段相關聯的資料是與正在進行柵格化的點相關聯的資料。

當點消除鋸齒啟用時，不支援所有的大小。 如果要求的大小不受支援，則會使用最接近的支援大小。 只保證支援大小 1.0;其他則取決於執行。 您可以藉由呼叫 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 點 \_ 大小 \_ 範圍和 GL \_ 點 \_ 大小 \_ 的資料細微性，來查詢範圍內支援的大小和大小差異。

當查詢 GL 點大小時，一律會傳回 **glPointSize** 所指定的點大小 \_ \_ 。 別名和反鋸齒點的固定和舍入對指定的值沒有任何作用。

非反鋸齒的點大小可能會壓制為與執行相關的最大值。 雖然無法查詢這個最大值，但它必須小於反鋸齒點的最大值，舍入到最接近的整數值。

下列函式會取出與 **glPointSize** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 點 \_ 大小的 glGet

具有引數 GL \_ 點 \_ 大小 \_ 範圍的 glGet

具有引數 GL \_ 點 \_ 大小 \_ 細微性的 glGet

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 點 \_ 平滑

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





