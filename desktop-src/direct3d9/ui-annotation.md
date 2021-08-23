---
description: 使用此注釋，將效果參數與主機環境中的 UI 控制項產生關聯。 這可讓使用者透過主應用程式以互動方式控制效果參數。
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: UI 注釋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9e8816bb34ada52794694a2c6ae63ff663787a5db7419e9bf27a40f5aa0cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044066"
---
# <a name="ui-annotation"></a>UI 注釋

使用此注釋，將效果參數與主機環境中的 UI 控制項產生關聯。 這可讓使用者透過主應用程式以互動方式控制效果參數。

DXSAS 會定義一組標準控制項，以資料模型和效果作者可能會從主應用程式預期的基本行為為基礎。 控制項注釋的使用方式如下：


```
string SasUiControl = "ControlType";
```



其中


```
ControlType
```



是下列其中一項：



| ControlType | 描述                                                                                                                                                                     | 內部資料類型                                                                                 | 控制項屬性注釋                                                                                 |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| 無        | 不應顯示任何控制項。 請注意，如果 [SasUiVisible](#sasuivisible) 為 True，而且控制項類型是 [無] 以外的任何類型，就會顯示控制項。                           | n/a                                                                                                | n/a                                                                                                          |
| 任意         | 這表示不會要求任何特殊的控制項。 呈現的控制項是應用程式定義的行為結果。                                                         | n/a                                                                                                | n/a                                                                                                          |
| ColorPicker | 將色彩值表示為色樣。 值會封裝到相關聯向量的 XYZ 元件中。 相關聯向量的 W 元件一律設定為一個。 | float *n* ，其中 *N* 是1到4（含）。                                                            | [SasUiEnum](#sasuienum)                                                                                      |
| 方向   | 方向向量。                                                                                                                                                             | float *n* ，其中 *N* 是2到4（含）。                                                            | 無                                                                                                         |
| FilePicker  | 可讓使用者流覽和選取檔案的對話方塊。                                                                                                                  | 字串                                                                                             | 無                                                                                                         |
| ListPicker  | 字串值的清單，使用者可以從中選取一個專案。 這些值是從 [SasUiEnum](#sasuienum) 批註產生的。                                         | 字串的陣列，以及包含所選字串值索引的整數值。 | [SasUiEnum](#sasuienum)                                                                                      |
| 數值     | 一組數位輸入控制項 (例如文字方塊) 。                                                                                                                         | 浮點數 *m* x *N* ，其中 *M* 和 *N* 是1到4（含）。                                               | [SasUiMin](#sasuimin)、 [SasUiMax](#sasuimax)、 [SasUiStride](#sasuistride)                                    |
| Slider      | 一組滑杆。                                                                                                                                                               | 浮點數 *m* x *N* ，其中 *M* 和 *N* 是1到4（含）                                                | [SasUiMin](#sasuimin)、 [SasUiMax](#sasuimax)、 [SasUiSteps](#sasuisteps)、 [SasUiStepsPower](#sasuistepspower) |
| String      | 用來編輯字串內容的文字方塊。                                                                                                                                         | 字串                                                                                             | 無                                                                                                         |



 

如果內部資料類型與相關聯的參數類型不相同，則會在資料從主應用程式參數傳輸到效果參數時進行轉換。

預設值為 "None" 字串。

## <a name="ui-common-properties"></a>UI 通用屬性

### <a name="sasuidescription"></a>SasUiDescription

您可以使用這個批註來指定用來描述工具的字串。 這可用於 UI 元素，例如工具提示。


```
string SasUiDescription = "descriptive string";
```



例如：


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



預設為空字串。

### <a name="sasuilabel"></a>SasUiLabel

使用這個批註來指定字串，以標記任何 UI 控制項。


```
string SasUiLabel = "some label;
```



以下是範例：


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



預設為空字串。

### <a name="sasuivisible"></a>SasUiVisible

您可以使用這個批註來指定是否應該向使用者顯示相關聯的參數。


```
bool SasUiVisible = false;
```



如果設定為 True，則主應用程式應該會顯示 UI 控制項來編輯批註效果參數。 若為 false，則不會在主應用程式中顯示任何 UI。

以下是範例：


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



預設值為 True。

## <a name="ui-control-properties"></a>UI 控制項屬性

控制項屬性批註是額外的修飾詞，可協助您判斷特定控制項的運作方式。

### <a name="sasuienum"></a>SasUiEnum

這個批註可讓您限制控制項的值範圍。 批註包含以逗號分隔的值字串。

預設為空字串。

### <a name="sasuimax"></a>SasUiMax

此批註會指定相關聯參數的最大值。 它只能與數位類型參數相關聯。 參數的最大值會實際計算如下：


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



最大參數 \_ 類型 \_ 是關聯參數所使用之類型的最大值。 這表示，將 [SasUiMax](#sasuimax) 注釋納入考慮的參數值會計算為：


```
ParameterValue = min(NewParameterValue, MaxValue);
```



預設值是 FLT \_ MAX，如 Math 中所定義。

### <a name="sasuimin"></a>SasUiMin

此批註會指定相關聯參數的最小值。 它只能與任何數數值型別的參數相關聯。 參數的最小值會實際計算如下：


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



參數 \_ 類型 \_ MIN 是關聯參數所使用之類型的最小值。 這表示，將 [SasUiMin](#sasuimin) 注釋納入考慮的參數值會計算為：


```
ParameterValue = max(NewParameterValue, MinValue);
```



預設值為-FLT \_ MAX，如 Math. h 中所定義。

### <a name="sasuisteps"></a>SasUiSteps

這個批註會指定遞增或遞減相關聯的參數值時，可使用的步驟數目。 批註只對具數位類型的參數有意義。 零指定主機應用程式將會選擇合理數目的步驟。

預設值為 0。

### <a name="sasuistepspower"></a>SasUiStepsPower

此批註會在 power 函式中指定指數，其範圍為 \[ 0.0 f、1.0 f \] 。 在計算參數值時，主應用程式必須執行下列方法：


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



預設值為 1.0 f。

### <a name="sasuistride"></a>SasUiStride

這個批註會指定遞增或遞減此值時應使用的增量。 不同于 [SasUiSteps](#sasuisteps)， [SasUiStride](#sasuistride) 對微調控制項很有用，例如，資料未系結，使用者會以 stride 遞增參數值，而不是預先定義的步驟數目。 主機應用程式應該根據 SasUiStride 值所) 的控制項行為來遞增 (或遞減，如下所示：


```
ParameterValue = ParameterValue +/- SasUiStride
```



預設值為 1.0 f。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX 標準注釋和語義參考](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



