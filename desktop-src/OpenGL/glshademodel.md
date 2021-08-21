---
title: 'glShadeModel 函式 (Gl) '
description: GlShadeModel 函式會選取平面或平滑陰影。
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- glShadeModel 函式 OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 505ff0e2d74f9eb4f252e4e663ceec00fd86469b3d69374623b2763915a08b0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491608"
---
# <a name="glshademodel-function"></a>glShadeModel 函式

**GlShadeModel** 函式會選取平面或平滑陰影。

## <a name="syntax"></a>語法


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

代表陰影技術的符號值。 接受的值為 GL 一般 \_ 和 gl \_ 平滑。 預設值為 GL \_ 平滑。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *模式* 是 gl \_ GLAT 或 gl 平滑的值 \_ 。<br/>                                                                      |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

OpenGL 基本型別可以是平面或平滑的陰影。 平滑陰影（預設值）會使頂點的計算色彩插補，因為基本型別會進行柵格化，通常會將不同的色彩指派給每個產生的圖元片段。 一般陰影只會選取一個頂點的計算色彩，並將其指派給所有藉由將單一基本型別來產生的圖元片段。 無論是哪一種情況，頂點的計算色彩都是光源的結果、如果已啟用光源，或是在指定頂點時的目前色彩（如果已停用光源的話）。

點的平面和平滑陰影不區分。 從1計算頂點和基本專案，從發出 [**glBegin**](glbegin.md) 時開始，每個平面陰影線條區段 *i* 都具有頂點 *i* + 1 的計算色彩（第二個頂點）。 從1開始計算，每個平面陰影多邊形都會獲得下表所列之頂點的計算色彩。 這是在所有案例中指定多邊形的最後一個頂點，但在單一多邊形中，第一個頂點指定平面陰影色彩。



| 多邊形 i 的基本類型 | 頂點   |
|-----------------------------|----------|
| 單一多邊形 (*I*= 1)       | 1        |
| 三角形條紋              | *i* + 2  |
| 三角形風扇                | *i* + 2  |
| 獨立三角形        | 3 *I*     |
| 四帶狀                  | 2 *i* + 2 |
| 獨立的四            | 4 *I*     |



 

平面和平滑陰影是由 **glShadeModel** 所指定， *模式* 分別設定為 gl \_ 和 gl \_ 。

下列函式會抓取 **glShadeModel** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 陰影 \_ 模型的 glGet

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

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





