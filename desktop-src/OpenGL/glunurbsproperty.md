---
title: 'gluNurbsProperty 函式 (X.glu 隊) '
description: GluNurbsProperty 函式會將非統一的有理 B 曲線 (NURBS) 屬性。
ms.assetid: c8c3b0c3-11b8-4123-91b6-75fed78932ce
keywords:
- gluNurbsProperty 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cbc52bd1405d15967db4aa1ef4941d0c4e166420d25d6d1fcb1ba4db0a6e744
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489028"
---
# <a name="glunurbsproperty-function"></a>gluNurbsProperty 函式

**GluNurbsProperty** 函式會將非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 屬性。

## <a name="syntax"></a>語法


```C++
void WINAPI gluNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nobj* 
</dt> <dd>

使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。

</dd> <dt>

*property* 
</dt> <dd>

要設定的屬性。 下列是有效值：



| 值                                                                                                                                                                                           | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_SAMPLING_TOLERANCE"></span><span id="glu_sampling_tolerance"></span><dl> <dt>**X.GLU 隊 \_ 取樣 \_ 容錯**</dt> </dl>       | 指定取樣方法設定為 X.GLU 隊路徑長度時要使用的最大長度（以圖元為單位） \_ \_ 。 預設值為50.0 圖元。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GLU_DISPLAY_MODE"></span><span id="glu_display_mode"></span><dl> <dt>**X.GLU 隊 \_ 顯示 \_ 模式**</dt> </dl>                         | *Value* 參數會定義要轉譯 NURBS 介面的方式。 您可以將 *值* 設定為 X.glu 隊 \_ 填滿、x.glu 隊 \_ 大綱 \_ 多邊形或 x.glu 隊 \_ 外框 \_ 修補程式。 <br/> X.GLU 隊 \_ 填滿。 介面會轉譯為一組多邊形。 這是預設值。 <br/> X.GLU 隊 \_ 外框 \_ 多邊形。 NURBS 程式庫只會繪製鑲嵌所建立之多邊形的外框。 <br/> X.GLU 隊 \_ 大綱 \_ 修補程式。 只會繪製由使用者定義之修補程式和修剪曲線的輪廓。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CULLING"></span><span id="glu_culling"></span><dl> <dt>**X.GLU 隊 \_ 剔除**</dt> </dl>                                         | *Value* 參數是布林值。 當值設定為 GL \_ TRUE 時，其控制點位於目前區外的 NURBS 曲線會在鑲嵌之前捨棄。 預設值為 GL \_ FALSE (，因為 NURBS 曲線不能完全落在其控制點) 的凸殼內。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GLU_AUTO_LOAD_MATRIX"></span><span id="glu_auto_load_matrix"></span><dl> <dt>**X.GLU 隊 \_ 自動 \_ 載入 \_ 矩陣**</dt> </dl>            | *Value* 參數是布林值。 當設定為 GL \_ TRUE 時，NURBS 程式碼會從 OpenGL 伺服器下載投影矩陣、模型矩陣和視口，以針對轉譯的每個 NURBS 曲線計算取樣和挑選矩陣。 需要取樣和挑選矩陣，才能將 NURBS 介面鑲嵌成直線線段或多邊形，以及在表面之外挑選非 NURBS 表面。 <br/> 如果此模式設定為 [GL \_ FALSE]，您就必須提供投射矩陣、模型矩陣和圖區，讓 NURBS 轉譯器用來建立取樣和挑選矩陣。 您可以使用 [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md) 函式來完成此動作。<br/> 此模式的預設值為 GL \_ TRUE。 將此模式從 GL \_ TRUE 變更為 gl FALSE，將 \_ 不會影響取樣和剔除矩陣，直到您呼叫 [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)為止。 <br/> X.GLU 隊1.1 版或更新版本支援下列屬性參數，且對於 X.GLU 隊1.0 版： X.GLU 隊 \_ 參數 \_ 容錯、X.glu 隊 \_ 取樣 \_ 方法、X.GLU 隊 \_ U \_ 步驟和 x.glu 隊 \_ V \_ 步驟而言是不正確。<br/> X.GLU 隊1.1 版或更新版本支援下列值參數，而且對於 X.GLU 隊1.0 版： X.GLU 隊 \_ 路徑 \_ 長度、X.glu 隊 \_ 參數化 \_ 錯誤和 x.glu 隊 \_ 網域 \_ 距離而言是不正確。<br/> |
| <span id="GLU_PARAMETRIC_TOLERANCE"></span><span id="glu_parametric_tolerance"></span><dl> <dt>**X.GLU 隊 \_ 參數 \_ 容錯**</dt> </dl> | 指定當取樣方法設定為 X.GLU 隊參數化錯誤時，所要使用的最大距離（以圖元為單位） \_ \_ 。 預設值為0.5。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_SAMPLING_METHOD"></span><span id="glu_sampling_method"></span><dl> <dt>**X.GLU 隊 \_ 取樣 \_ 方法**</dt> </dl>                | 指定如何 tessallate NURBS 表面。 X.GLU 隊 \_ 取樣 \_ 方法可以有下列三個值的其中一個。 <br/> X.GLU 隊 \_ 路徑 \_ 長度。 預設值。 指定使用鑲嵌式多邊形邊緣的最大長度（以圖元為單位）所呈現的表面，不大於 X.GLU 隊取樣容錯值所指定的值 \_ \_ 。 <br/> X.GLU 隊 \_ 參數化 \_ 錯誤。 指定在呈現介面時，X.GLU 隊 \_ 參數化容錯的值 \_ 會指定鑲嵌式多邊形與其近似表面之間的最大距離（以圖元為單位）。 <br/> X.GLU 隊 \_ 網域 \_ 距離。 指定在參數化座標中，要在 *u* 和 *v* 維度中採用的每個單位長度的樣本點數目。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GLU_U_STEP"></span><span id="glu_u_step"></span><dl> <dt>**X.GLU 隊 \_ U \_ 步驟**</dt> </dl>                                           | 指定在參數座標中，沿著 *u* 維度取得的每個單位長度的樣本點數目。 \_ \_ 當 X.glu 隊 \_ 取樣 \_ 方法設定為 x.glu 隊 \_ 網域距離時，會使用 x.glu 隊 U 步驟的值 \_ 。 預設值是 100。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GLU_V_STEP"></span><span id="glu_v_step"></span><dl> <dt>**X.GLU 隊 \_ V \_ 步驟**</dt> </dl>                                           | 指定在參數座標中，沿著 *v* 維度取得的每個單位長度的樣本點數目。 \_ \_ 當 X.glu 隊 \_ 取樣 \_ 方法設定為 x.glu 隊 \_ 網域距離時，會使用 x.glu 隊 V 步驟的值 \_ 。 預設值是 100。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*value* 
</dt> <dd>

要設定指定屬性的值。 *Value* 參數可以是數值或下列三個值的其中一個： X.glu 隊 \_ 路徑 \_ 長度、x.glu 隊 \_ 參數化 \_ 錯誤或 x.glu 隊 \_ 網域 \_ 距離。



| 值                                                                                                                                                                               | 意義                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_PATH_LENGTH"></span><span id="glu_path_length"></span><dl> <dt>**X.GLU 隊 \_ 路徑 \_ 長度**</dt> </dl>                | 預設值。 指定使用鑲嵌式多邊形邊緣的最大長度（以圖元為單位）所呈現的表面，不大於 X.GLU 隊取樣容錯值所指定的值 \_ \_ 。<br/> |
| <span id="GLU_PARAMETRIC_ERROR"></span><span id="glu_parametric_error"></span><dl> <dt>**X.GLU 隊 \_ 參數化 \_ 錯誤**</dt> </dl> | 指定在呈現介面時，X.GLU 隊 \_ 參數化容錯的值 \_ 會指定鑲嵌式多邊形與其近似表面之間的最大距離（以圖元為單位）。<br/>       |
| <span id="GLU_DOMAIN_DISTANCE"></span><span id="glu_domain_distance"></span><dl> <dt>**X.GLU 隊 \_ 網域 \_ 距離**</dt> </dl>    | 指定在參數化座標中，要在 *u* 和 *v* 維度中採用的每個單位長度的樣本點數目。<br/>                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

使用 **gluNurbsProperty** 來控制儲存在 NURBS 物件中的屬性。 這些屬性會影響 NURBS 曲線的呈現方式。





 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>X.glu 隊。h</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Glu32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluGetString**](glugetstring.md)
</dt> <dt>

[**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





