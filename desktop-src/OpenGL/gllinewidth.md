---
title: 'glLineWidth 函式 (Gl) '
description: GlLineWidth 函式會指定柵格線的寬度。
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- glLineWidth 函式 OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad5af24170f47125136e87e055413a576821bf75d3f5f87532d026d0bb2fd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492968"
---
# <a name="gllinewidth-function"></a>glLineWidth 函式

**GlLineWidth** 函式會指定柵格線的寬度。

## <a name="syntax"></a>語法


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*width* (寬度) 
</dt> <dd>

柵格線的寬度。 預設值為1.0。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 小於或等於零。<br/>                                                                                    |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlLineWidth** 函式會指定鋸齒和反鋸齒線條的點陣化寬度。 使用1.0 以外的線條寬度有不同的效果，這取決於是否已啟用行消除鋸齒功能。 藉由呼叫 [**glEnable**](glenable.md) 和 **glDisable** ，並將引數 GL \_ 行平滑，以控制線條消除鋸齒 \_ 。

如果停用行消除鋸齒，則會將提供的寬度四捨五入至最接近的整數，以決定實際寬度。  (如果舍入結果的值為0.0，則會像行寬度是 1.0) If \| ？ x \|  =  \| ？ y \| ， *i* 圖元會填入每個柵格化的資料行，其中 *i* 是 *寬度* 的舍入值。 否則，系統會在每個已點陣化的資料列中填入 *i* 圖元。

如果已啟用消除鋸齒功能，則線條柵格化會針對每個圖元正方形產生一個片段，該矩形的寬度等於目前的線條寬度、長度等於線條的實際長度，並以數學線線段為中心。 每個片段的涵蓋範圍值是矩形區域與對應圖元正方形交集的視窗座標區域。 此值會儲存並用於最後的點陣化步驟中。

啟用線條消除鋸齒功能時，並非所有寬度都可支援。 如果要求的寬度不受支援，則會使用最接近的支援寬度。 只保證支援寬度 1.0;其他則取決於執行。 您可以藉由呼叫 **glGet** 與引數 GL \_ 行 \_ 寬度 \_ 範圍和 GL \_ 行 \_ 寬度 \_ 的資料細微性，來查詢範圍中支援的寬度和大小差異。

當查詢 GL 行寬時，一律會傳回 **glLineWidth** 所指定的線條寬度 \_ \_ 。 別名和反鋸齒線條的固定和舍入不會影響指定的值。

非反鋸齒線條寬度可能會壓制為與執行相關的最大值。 雖然無法查詢這個最大值，但它必須小於反鋸齒線的最大值，舍入到最接近的整數值。

下列函式會取出與 **glLineWidth** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 行 \_ 寬的 glGet

具有引數 GL \_ 行 \_ 寬 \_ 範圍的 glGet

具有引數 GL \_ 行 \_ 寬 \_ 細微性的 glGet

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ 行 \_ 平滑

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

 

 





