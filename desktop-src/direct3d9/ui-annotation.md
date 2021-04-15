---
description: 使用此注釋，將效果參數與主機環境中的 UI 控制項產生關聯。 這可讓使用者透過主應用程式以互動方式控制效果參數。
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: UI 注釋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e873c83a01c5c2214cb49a93e75167e58a3389
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467931"
---
# <a name="ui-annotation"></a><span data-ttu-id="65114-104">UI 注釋</span><span class="sxs-lookup"><span data-stu-id="65114-104">UI Annotation</span></span>

<span data-ttu-id="65114-105">使用此注釋，將效果參數與主機環境中的 UI 控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="65114-105">Use this annotation to associate an effect parameter with a UI control in the host environment.</span></span> <span data-ttu-id="65114-106">這可讓使用者透過主應用程式以互動方式控制效果參數。</span><span class="sxs-lookup"><span data-stu-id="65114-106">This will allow a user to interactively control an effect parameter through the host application.</span></span>

<span data-ttu-id="65114-107">DXSAS 會定義一組標準控制項，以資料模型和效果作者可能會從主應用程式預期的基本行為為基礎。</span><span class="sxs-lookup"><span data-stu-id="65114-107">DXSAS defines a set of standard controls in terms of the data model and basic behavior that effect authors can expect from host applications.</span></span> <span data-ttu-id="65114-108">控制項注釋的使用方式如下：</span><span class="sxs-lookup"><span data-stu-id="65114-108">The control annotation is used like this:</span></span>


```
string SasUiControl = "ControlType";
```



<span data-ttu-id="65114-109">其中</span><span class="sxs-lookup"><span data-stu-id="65114-109">where</span></span>


```
ControlType
```



<span data-ttu-id="65114-110">是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="65114-110">is one of the following:</span></span>



|             |                                                                                                                                                                                 |                                                                                                    |                                                                                                              |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65114-111">ControlType</span><span class="sxs-lookup"><span data-stu-id="65114-111">ControlType</span></span> | <span data-ttu-id="65114-112">Description</span><span class="sxs-lookup"><span data-stu-id="65114-112">Description</span></span>                                                                                                                                                                     | <span data-ttu-id="65114-113">內部資料類型</span><span class="sxs-lookup"><span data-stu-id="65114-113">Internal Data Type</span></span>                                                                                 | <span data-ttu-id="65114-114">控制項屬性注釋</span><span class="sxs-lookup"><span data-stu-id="65114-114">Control Property Annotations</span></span>                                                                                 |
| <span data-ttu-id="65114-115">無</span><span class="sxs-lookup"><span data-stu-id="65114-115">None</span></span>        | <span data-ttu-id="65114-116">不應顯示任何控制項。</span><span class="sxs-lookup"><span data-stu-id="65114-116">No control should be shown.</span></span> <span data-ttu-id="65114-117">請注意，如果 [SasUiVisible](#sasuivisible) 為 True，而且控制項類型是 [無] 以外的任何類型，就會顯示控制項。</span><span class="sxs-lookup"><span data-stu-id="65114-117">Note that a control is visible if [SasUiVisible](#sasuivisible) is True and the control type is any type other than None.</span></span>                           | <span data-ttu-id="65114-118">n/a</span><span class="sxs-lookup"><span data-stu-id="65114-118">n/a</span></span>                                                                                                | <span data-ttu-id="65114-119">n/a</span><span class="sxs-lookup"><span data-stu-id="65114-119">n/a</span></span>                                                                                                          |
| <span data-ttu-id="65114-120">任意</span><span class="sxs-lookup"><span data-stu-id="65114-120">Any</span></span>         | <span data-ttu-id="65114-121">這表示不會要求任何特殊的控制項。</span><span class="sxs-lookup"><span data-stu-id="65114-121">This implies that no special control is requested.</span></span> <span data-ttu-id="65114-122">呈現的控制項是應用程式定義的行為結果。</span><span class="sxs-lookup"><span data-stu-id="65114-122">The control presented is the result of application-defined behavior.</span></span>                                                         | <span data-ttu-id="65114-123">n/a</span><span class="sxs-lookup"><span data-stu-id="65114-123">n/a</span></span>                                                                                                | <span data-ttu-id="65114-124">n/a</span><span class="sxs-lookup"><span data-stu-id="65114-124">n/a</span></span>                                                                                                          |
| <span data-ttu-id="65114-125">ColorPicker</span><span class="sxs-lookup"><span data-stu-id="65114-125">ColorPicker</span></span> | <span data-ttu-id="65114-126">將色彩值表示為色樣。</span><span class="sxs-lookup"><span data-stu-id="65114-126">Represent a color value as a color swatch.</span></span> <span data-ttu-id="65114-127">值會封裝到相關聯向量的 XYZ 元件中。</span><span class="sxs-lookup"><span data-stu-id="65114-127">The value is packed into the XYZ components of the associated vector.</span></span> <span data-ttu-id="65114-128">相關聯向量的 W 元件一律設定為一個。</span><span class="sxs-lookup"><span data-stu-id="65114-128">The W component of the associated vector is always set to one.</span></span> | <span data-ttu-id="65114-129">float *n* ，其中 *N* 是1到4（含）。</span><span class="sxs-lookup"><span data-stu-id="65114-129">float *N* where *N* is 1 to 4 inclusive.</span></span>                                                            | [<span data-ttu-id="65114-130">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="65114-130">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="65114-131">方向</span><span class="sxs-lookup"><span data-stu-id="65114-131">Direction</span></span>   | <span data-ttu-id="65114-132">方向向量。</span><span class="sxs-lookup"><span data-stu-id="65114-132">A direction vector.</span></span>                                                                                                                                                             | <span data-ttu-id="65114-133">float *n* ，其中 *N* 是2到4（含）。</span><span class="sxs-lookup"><span data-stu-id="65114-133">float *N* where *N* is 2 to 4 inclusive.</span></span>                                                            | <span data-ttu-id="65114-134">無</span><span class="sxs-lookup"><span data-stu-id="65114-134">None</span></span>                                                                                                         |
| <span data-ttu-id="65114-135">FilePicker</span><span class="sxs-lookup"><span data-stu-id="65114-135">FilePicker</span></span>  | <span data-ttu-id="65114-136">可讓使用者流覽和選取檔案的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="65114-136">A dialog box that allows the user to browse and select a file.</span></span>                                                                                                                  | <span data-ttu-id="65114-137">字串</span><span class="sxs-lookup"><span data-stu-id="65114-137">string</span></span>                                                                                             | <span data-ttu-id="65114-138">無</span><span class="sxs-lookup"><span data-stu-id="65114-138">None</span></span>                                                                                                         |
| <span data-ttu-id="65114-139">ListPicker</span><span class="sxs-lookup"><span data-stu-id="65114-139">ListPicker</span></span>  | <span data-ttu-id="65114-140">字串值的清單，使用者可以從中選取一個專案。</span><span class="sxs-lookup"><span data-stu-id="65114-140">A list of string values from which the user can select one entry.</span></span> <span data-ttu-id="65114-141">這些值是從 [SasUiEnum](#sasuienum) 批註產生的。</span><span class="sxs-lookup"><span data-stu-id="65114-141">The values are generated from the [SasUiEnum](#sasuienum) annotation.</span></span>                                         | <span data-ttu-id="65114-142">字串的陣列，以及包含所選字串值索引的整數值。</span><span class="sxs-lookup"><span data-stu-id="65114-142">An array of strings along with an integer value containing the index of the selected string value.</span></span> | [<span data-ttu-id="65114-143">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="65114-143">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="65114-144">數值</span><span class="sxs-lookup"><span data-stu-id="65114-144">Numeric</span></span>     | <span data-ttu-id="65114-145">一組數位輸入控制項 (例如文字方塊) 。</span><span class="sxs-lookup"><span data-stu-id="65114-145">A set of numerical input controls (such as text boxes).</span></span>                                                                                                                         | <span data-ttu-id="65114-146">浮點數 *m* x *N* ，其中 *M* 和 *N* 是1到4（含）。</span><span class="sxs-lookup"><span data-stu-id="65114-146">float *M* x *N* where *M* and *N* are 1 to 4 inclusive.</span></span>                                               | <span data-ttu-id="65114-147">[SasUiMin](#sasuimin)、 [SasUiMax](#sasuimax)、 [SasUiStride](#sasuistride)</span><span class="sxs-lookup"><span data-stu-id="65114-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span></span>                                    |
| <span data-ttu-id="65114-148">滑桿</span><span class="sxs-lookup"><span data-stu-id="65114-148">Slider</span></span>      | <span data-ttu-id="65114-149">一組滑杆。</span><span class="sxs-lookup"><span data-stu-id="65114-149">A set of sliders.</span></span>                                                                                                                                                               | <span data-ttu-id="65114-150">浮點數 *m* x *N* ，其中 *M* 和 *N* 是1到4（含）</span><span class="sxs-lookup"><span data-stu-id="65114-150">float *M* x *N* where *M* and *N* are 1 to 4 inclusive</span></span>                                                | <span data-ttu-id="65114-151">[SasUiMin](#sasuimin)、 [SasUiMax](#sasuimax)、 [SasUiSteps](#sasuisteps)、 [SasUiStepsPower](#sasuistepspower)</span><span class="sxs-lookup"><span data-stu-id="65114-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span></span> |
| <span data-ttu-id="65114-152">String</span><span class="sxs-lookup"><span data-stu-id="65114-152">String</span></span>      | <span data-ttu-id="65114-153">用來編輯字串內容的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="65114-153">An text box for editing string content.</span></span>                                                                                                                                         | <span data-ttu-id="65114-154">字串</span><span class="sxs-lookup"><span data-stu-id="65114-154">string</span></span>                                                                                             | <span data-ttu-id="65114-155">無</span><span class="sxs-lookup"><span data-stu-id="65114-155">None</span></span>                                                                                                         |



 

<span data-ttu-id="65114-156">如果內部資料類型與相關聯的參數類型不相同，則會在資料從主應用程式參數傳輸到效果參數時進行轉換。</span><span class="sxs-lookup"><span data-stu-id="65114-156">If the internal data type is not identical to the associated parameter's type, casting will occur when data is transferred from the host application parameter to the effect parameter.</span></span>

<span data-ttu-id="65114-157">預設值為 "None" 字串。</span><span class="sxs-lookup"><span data-stu-id="65114-157">The default is the string "None".</span></span>

## <a name="ui-common-properties"></a><span data-ttu-id="65114-158">UI 通用屬性</span><span class="sxs-lookup"><span data-stu-id="65114-158">UI Common Properties</span></span>

### <a name="sasuidescription"></a><span data-ttu-id="65114-159">SasUiDescription</span><span class="sxs-lookup"><span data-stu-id="65114-159">SasUiDescription</span></span>

<span data-ttu-id="65114-160">您可以使用這個批註來指定用來描述工具的字串。</span><span class="sxs-lookup"><span data-stu-id="65114-160">Use this annotation to specify a string to describe a tool.</span></span> <span data-ttu-id="65114-161">這可用於 UI 元素，例如工具提示。</span><span class="sxs-lookup"><span data-stu-id="65114-161">This could be used for UI elements such as tool tips.</span></span>


```
string SasUiDescription = "descriptive string";
```



<span data-ttu-id="65114-162">例如：</span><span class="sxs-lookup"><span data-stu-id="65114-162">For instance:</span></span>


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



<span data-ttu-id="65114-163">預設為空字串。</span><span class="sxs-lookup"><span data-stu-id="65114-163">The default is an empty string.</span></span>

### <a name="sasuilabel"></a><span data-ttu-id="65114-164">SasUiLabel</span><span class="sxs-lookup"><span data-stu-id="65114-164">SasUiLabel</span></span>

<span data-ttu-id="65114-165">使用這個批註來指定字串，以標記任何 UI 控制項。</span><span class="sxs-lookup"><span data-stu-id="65114-165">Use this annotation to specify a string to label any UI control.</span></span>


```
string SasUiLabel = "some label;
```



<span data-ttu-id="65114-166">請看以下範例：</span><span class="sxs-lookup"><span data-stu-id="65114-166">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



<span data-ttu-id="65114-167">預設為空字串。</span><span class="sxs-lookup"><span data-stu-id="65114-167">The default is an empty string.</span></span>

### <a name="sasuivisible"></a><span data-ttu-id="65114-168">SasUiVisible</span><span class="sxs-lookup"><span data-stu-id="65114-168">SasUiVisible</span></span>

<span data-ttu-id="65114-169">您可以使用這個批註來指定是否應該向使用者顯示相關聯的參數。</span><span class="sxs-lookup"><span data-stu-id="65114-169">Use this annotation to specify whether the associated parameter should be displayed to the user.</span></span>


```
bool SasUiVisible = false;
```



<span data-ttu-id="65114-170">如果設定為 True，則主應用程式應該會顯示 UI 控制項來編輯批註效果參數。</span><span class="sxs-lookup"><span data-stu-id="65114-170">If set to True, the host application should display a UI control for editing the annotated effect parameter.</span></span> <span data-ttu-id="65114-171">若為 false，則不會在主應用程式中顯示任何 UI。</span><span class="sxs-lookup"><span data-stu-id="65114-171">If false, no UI is displayed in the host application.</span></span>

<span data-ttu-id="65114-172">請看以下範例：</span><span class="sxs-lookup"><span data-stu-id="65114-172">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



<span data-ttu-id="65114-173">預設值為 True。</span><span class="sxs-lookup"><span data-stu-id="65114-173">The default is True.</span></span>

## <a name="ui-control-properties"></a><span data-ttu-id="65114-174">UI 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="65114-174">UI Control Properties</span></span>

<span data-ttu-id="65114-175">控制項屬性批註是額外的修飾詞，可協助您判斷特定控制項的運作方式。</span><span class="sxs-lookup"><span data-stu-id="65114-175">Control property annotations are additional modifiers that help determine how a particular control operates.</span></span>

### <a name="sasuienum"></a><span data-ttu-id="65114-176">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="65114-176">SasUiEnum</span></span>

<span data-ttu-id="65114-177">這個批註可讓您限制控制項的值範圍。</span><span class="sxs-lookup"><span data-stu-id="65114-177">This annotation allows you to restrict the range of values for a control.</span></span> <span data-ttu-id="65114-178">批註包含以逗號分隔的值字串。</span><span class="sxs-lookup"><span data-stu-id="65114-178">The annotation contains a string of values delimited by commas.</span></span>

<span data-ttu-id="65114-179">預設為空字串。</span><span class="sxs-lookup"><span data-stu-id="65114-179">The default is an empty string.</span></span>

### <a name="sasuimax"></a><span data-ttu-id="65114-180">SasUiMax</span><span class="sxs-lookup"><span data-stu-id="65114-180">SasUiMax</span></span>

<span data-ttu-id="65114-181">此批註會指定相關聯參數的最大值。</span><span class="sxs-lookup"><span data-stu-id="65114-181">This annotation specifies the maximum value of the associated parameter.</span></span> <span data-ttu-id="65114-182">它只能與數位類型參數相關聯。</span><span class="sxs-lookup"><span data-stu-id="65114-182">It can only be associated with a numerically-typed parameter.</span></span> <span data-ttu-id="65114-183">參數的最大值會實際計算如下：</span><span class="sxs-lookup"><span data-stu-id="65114-183">The maximum value of the parameter will actually be calculated as:</span></span>


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



<span data-ttu-id="65114-184">最大參數 \_ 類型 \_ 是關聯參數所使用之類型的最大值。</span><span class="sxs-lookup"><span data-stu-id="65114-184">PARAMETER\_TYPE\_MAX is the maximum value for the type used by the associated parameter.</span></span> <span data-ttu-id="65114-185">這表示，將 [SasUiMax](#sasuimax) 注釋納入考慮的參數值會計算為：</span><span class="sxs-lookup"><span data-stu-id="65114-185">This means that the value of the parameter, taking into account the [SasUiMax](#sasuimax) annotation is calculated as:</span></span>


```
ParameterValue = min(NewParameterValue, MaxValue);
```



<span data-ttu-id="65114-186">預設值是 FLT \_ MAX，如 Math 中所定義。</span><span class="sxs-lookup"><span data-stu-id="65114-186">The default value is FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuimin"></a><span data-ttu-id="65114-187">SasUiMin</span><span class="sxs-lookup"><span data-stu-id="65114-187">SasUiMin</span></span>

<span data-ttu-id="65114-188">此批註會指定相關聯參數的最小值。</span><span class="sxs-lookup"><span data-stu-id="65114-188">This annotation specifies the minimum value of the associated parameter.</span></span> <span data-ttu-id="65114-189">它只能與任何數數值型別的參數相關聯。</span><span class="sxs-lookup"><span data-stu-id="65114-189">It can only be associated with any numerically-typed parameter.</span></span> <span data-ttu-id="65114-190">參數的最小值會實際計算如下：</span><span class="sxs-lookup"><span data-stu-id="65114-190">The minimum value of the parameter will actually be calculated as:</span></span>


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



<span data-ttu-id="65114-191">參數 \_ 類型 \_ MIN 是關聯參數所使用之類型的最小值。</span><span class="sxs-lookup"><span data-stu-id="65114-191">PARAMETER\_TYPE\_MIN is the minimum value for the type used by the associated parameter.</span></span> <span data-ttu-id="65114-192">這表示，將 [SasUiMin](#sasuimin) 注釋納入考慮的參數值會計算為：</span><span class="sxs-lookup"><span data-stu-id="65114-192">This means that the value of the parameter, taking into account the [SasUiMin](#sasuimin) annotation is calculated as:</span></span>


```
ParameterValue = max(NewParameterValue, MinValue);
```



<span data-ttu-id="65114-193">預設值為-FLT \_ MAX，如 Math. h 中所定義。</span><span class="sxs-lookup"><span data-stu-id="65114-193">The default value is -FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuisteps"></a><span data-ttu-id="65114-194">SasUiSteps</span><span class="sxs-lookup"><span data-stu-id="65114-194">SasUiSteps</span></span>

<span data-ttu-id="65114-195">這個批註會指定遞增或遞減相關聯的參數值時，可使用的步驟數目。</span><span class="sxs-lookup"><span data-stu-id="65114-195">This annotation specifies the number of steps that can be used when incrementing or decrementing the associated parameter value.</span></span> <span data-ttu-id="65114-196">批註只對具數位類型的參數有意義。</span><span class="sxs-lookup"><span data-stu-id="65114-196">The annotation is only meaningful on a numerically-typed parameter.</span></span> <span data-ttu-id="65114-197">零指定主機應用程式將會選擇合理數目的步驟。</span><span class="sxs-lookup"><span data-stu-id="65114-197">Zero specifies that the host application will choose a reasonable number of steps.</span></span>

<span data-ttu-id="65114-198">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="65114-198">The default value is 0.</span></span>

### <a name="sasuistepspower"></a><span data-ttu-id="65114-199">SasUiStepsPower</span><span class="sxs-lookup"><span data-stu-id="65114-199">SasUiStepsPower</span></span>

<span data-ttu-id="65114-200">此批註會在 power 函式中指定指數，其範圍為 \[ 0.0 f、1.0 f \] 。</span><span class="sxs-lookup"><span data-stu-id="65114-200">This annotation specifies the exponent in the power function, which has the range \[0.0f, 1.0f\].</span></span> <span data-ttu-id="65114-201">在計算參數值時，主應用程式必須執行下列方法：</span><span class="sxs-lookup"><span data-stu-id="65114-201">Host applications must implement the following method when calculating parameter values:</span></span>


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



<span data-ttu-id="65114-202">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="65114-202">The default value is 1.0f.</span></span>

### <a name="sasuistride"></a><span data-ttu-id="65114-203">SasUiStride</span><span class="sxs-lookup"><span data-stu-id="65114-203">SasUiStride</span></span>

<span data-ttu-id="65114-204">這個批註會指定遞增或遞減此值時應使用的增量。</span><span class="sxs-lookup"><span data-stu-id="65114-204">This annotation specifies the increment that should be used when incrementing or decrementing this value.</span></span> <span data-ttu-id="65114-205">不同于 [SasUiSteps](#sasuisteps)， [SasUiStride](#sasuistride) 對微調控制項很有用，例如，資料未系結，使用者會以 stride 遞增參數值，而不是預先定義的步驟數目。</span><span class="sxs-lookup"><span data-stu-id="65114-205">Unlike [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) is useful with a spinner control, for instance, where the data is unbounded and the user would rather increment the parameter value by stride rather than by a pre-defined number of steps.</span></span> <span data-ttu-id="65114-206">主機應用程式應該根據 SasUiStride 值所) 的控制項行為來遞增 (或遞減，如下所示：</span><span class="sxs-lookup"><span data-stu-id="65114-206">Host applications should increment (or decrement depending on the control behavior) by the value of SasUiStride as follows:</span></span>


```
ParameterValue = ParameterValue +/- SasUiStride
```



<span data-ttu-id="65114-207">預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="65114-207">The default value is 1.0f.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65114-208">相關主題</span><span class="sxs-lookup"><span data-stu-id="65114-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65114-209">DirectX 標準注釋和語義參考</span><span class="sxs-lookup"><span data-stu-id="65114-209">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



