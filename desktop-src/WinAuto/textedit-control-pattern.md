---
title: Macos textedit 控制項模式
description: 介紹執行 ITextEditProvider 的指導方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9
keywords:
- 消費者介面自動化，執行 Macos textedit 控制項模式
- 消費者介面自動化，Macos textedit 控制項模式
- 控制項模式，Macos textedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf8512db4f676a263bf46bdbdfea7b6b7eaba11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316348"
---
# <a name="textedit-control-pattern"></a><span data-ttu-id="059a6-106">Macos textedit 控制項模式</span><span class="sxs-lookup"><span data-stu-id="059a6-106">TextEdit Control Pattern</span></span>

<span data-ttu-id="059a6-107">介紹執行 [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider)的指導方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="059a6-107">Introduces guidelines and conventions for implementing [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider), including information about properties and methods.</span></span> <span data-ttu-id="059a6-108">**Macos textedit** 控制項模式用於以程式設計方式存取修改文字的控制項，例如執行自動校正或啟用輸入組合的控制項。</span><span class="sxs-lookup"><span data-stu-id="059a6-108">The **TextEdit** control pattern is used for programmatic access to a control that modifies text, for example a control that performs auto-correction or enables input composition.</span></span>

> [!Note]  
> <span data-ttu-id="059a6-109">本主題中的「執行附注」指的是來自文字服務架構 (TSF) 的 Api。</span><span class="sxs-lookup"><span data-stu-id="059a6-109">Implementation notes in this topic refer to APIs that come from Text Services Framework (TSF).</span></span> <span data-ttu-id="059a6-110">如需 TSF 和 API 參考的詳細資訊，請參閱 [文字服務架構](/windows/desktop/TSF/text-services-framework)。</span><span class="sxs-lookup"><span data-stu-id="059a6-110">For more info about TSF and the API reference, see [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>

 

## <a name="required-members-for-itexteditprovider"></a><span data-ttu-id="059a6-111">**ITextEditProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="059a6-111">Required Members for **ITextEditProvider**</span></span>

<span data-ttu-id="059a6-112">執行 [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) 介面時需要這些屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="059a6-112">These properties and methods are required for implementing the [**ITextEditProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider) interface.</span></span>



| <span data-ttu-id="059a6-113">必要成員</span><span class="sxs-lookup"><span data-stu-id="059a6-113">Required members</span></span>                                                              | <span data-ttu-id="059a6-114">成員類型</span><span class="sxs-lookup"><span data-stu-id="059a6-114">Member type</span></span> | <span data-ttu-id="059a6-115">備註</span><span class="sxs-lookup"><span data-stu-id="059a6-115">Notes</span></span>                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="059a6-116">**GetActiveComposition**</span><span class="sxs-lookup"><span data-stu-id="059a6-116">**GetActiveComposition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getactivecomposition) | <span data-ttu-id="059a6-117">方法</span><span class="sxs-lookup"><span data-stu-id="059a6-117">Method</span></span>      | <span data-ttu-id="059a6-118">傳回目前轉換的範圍 (無（如果沒有轉換) ）。</span><span class="sxs-lookup"><span data-stu-id="059a6-118">Returns the range of the current conversion (none if there is no conversion).</span></span> <span data-ttu-id="059a6-119">傳回 TSF 中的使用中複合 (，這是由 GUID 成分 **\_ \_ 組成**) 標記的範圍。</span><span class="sxs-lookup"><span data-stu-id="059a6-119">Return the active composition (in TSF, this is the range marked by **GUID\_PROP\_COMPOSING**).</span></span> <span data-ttu-id="059a6-120">例如，使用 Microsoft 日文輸入法編輯器 (IME) ，這會是完整加底線的文字。</span><span class="sxs-lookup"><span data-stu-id="059a6-120">For example with the Microsoft Japanese Input Method Editor (IME), this would be the full underlined text.</span></span> |
| [<span data-ttu-id="059a6-121">**GetConversionTarget**</span><span class="sxs-lookup"><span data-stu-id="059a6-121">**GetConversionTarget**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itexteditprovider-getconversiontarget)   | <span data-ttu-id="059a6-122">方法</span><span class="sxs-lookup"><span data-stu-id="059a6-122">Method</span></span>      | <span data-ttu-id="059a6-123">如果沒有轉換) ，則傳回目前的轉換目標範圍 (無。</span><span class="sxs-lookup"><span data-stu-id="059a6-123">Returns the current conversion target range (none if no conversion).</span></span> <span data-ttu-id="059a6-124">在 TSF 中，這是標示為 **tf \_ attr \_ Target \_ NOTCONVERTED** 或 **tf \_ attr \_ target \_** （從 **tf \_ DISPLAYATTRIBUTE** 結構轉換）的字元範圍。</span><span class="sxs-lookup"><span data-stu-id="059a6-124">In TSF, this is the range of characters marked as **TF\_ATTR\_TARGET\_NOTCONVERTED** or **TF\_ATTR\_TARGET\_CONVERTED** from the **TF\_DISPLAYATTRIBUTE** structure.</span></span>                                               |



 

<span data-ttu-id="059a6-125">**TextEditTextChanged** 和 **ConversionTargetChanged** 事件必須由支援 **macos textedit** 模式的 Microsoft 消費者介面自動化元素所引發。</span><span class="sxs-lookup"><span data-stu-id="059a6-125">The **TextEditTextChanged** and **ConversionTargetChanged** events are required to be raised by Microsoft UI Automation elements supporting the **TextEdit** pattern.</span></span>

### <a name="textedittextchanged"></a><span data-ttu-id="059a6-126">**TextEditTextChanged**</span><span class="sxs-lookup"><span data-stu-id="059a6-126">**TextEditTextChanged**</span></span>

-   <span data-ttu-id="059a6-127">使用 [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) 函數來引發 **TextEditTextChanged** 事件。</span><span class="sxs-lookup"><span data-stu-id="059a6-127">Use the [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) function to raise the **TextEditTextChanged** event.</span></span>
-   <span data-ttu-id="059a6-128">下表列出您應該引發事件的案例，以及要使用的 [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) 參數。</span><span class="sxs-lookup"><span data-stu-id="059a6-128">The following table lists the cases when you should raise the event and the [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent) parameters to use.</span></span>



| <span data-ttu-id="059a6-129">TextEditChangeType</span><span class="sxs-lookup"><span data-stu-id="059a6-129">TextEditChangeType</span></span>                                            | <span data-ttu-id="059a6-130">事件裝載</span><span class="sxs-lookup"><span data-stu-id="059a6-130">Event Payload</span></span>                                | <span data-ttu-id="059a6-131">備註</span><span class="sxs-lookup"><span data-stu-id="059a6-131">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="059a6-132">**校正**</span><span class="sxs-lookup"><span data-stu-id="059a6-132">**AutoCorrect**</span></span>](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | <span data-ttu-id="059a6-133">新增的更正字串</span><span class="sxs-lookup"><span data-stu-id="059a6-133">New corrected string</span></span>                         | <span data-ttu-id="059a6-134">當控制項進行自動校正時引發。</span><span class="sxs-lookup"><span data-stu-id="059a6-134">Raised when an auto-correction is made by the control.</span></span> <span data-ttu-id="059a6-135">或每次透過 TSF 進行取代，而且範圍具有已套用之 **TKB \_ 替代 \_ 自動校正 \_** 的 **GUID 內容 \_ \_ TKB \_ 替換** 值。</span><span class="sxs-lookup"><span data-stu-id="059a6-135">Or whenever a replacement is made through TSF and the range has a **GUID\_PROP\_TKB\_ALTERNATES** value of **TKB\_ALTERNATES\_AUTOCORRECTION\_APPLIED**.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="059a6-136">**Composition**</span><span class="sxs-lookup"><span data-stu-id="059a6-136">**Composition**</span></span>](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype)          | <span data-ttu-id="059a6-137">更新的字串</span><span class="sxs-lookup"><span data-stu-id="059a6-137">The updated string</span></span>                           | <span data-ttu-id="059a6-138">承載必須只包含變更的字元 (不會傳送整個撰寫字串) 。</span><span class="sxs-lookup"><span data-stu-id="059a6-138">The payload must only include the characters that changed (do not send the entire composition string).</span></span> <span data-ttu-id="059a6-139">每次進行組合取代時引發。</span><span class="sxs-lookup"><span data-stu-id="059a6-139">Raised whenever a composition replacement is made.</span></span> <span data-ttu-id="059a6-140">在 TSF 中，會將組合取代定義為已設定 **GUID \_ \_ 組成** 旗標的取代。</span><span class="sxs-lookup"><span data-stu-id="059a6-140">In TSF, a composition replacement is defined as a replacement that has the **GUID\_PROP\_COMPOSING** flag set.</span></span> <span data-ttu-id="059a6-141">執行 TSF 的編輯控制項可以透過 **OnEndEdit** 通知來監視這些變更。</span><span class="sxs-lookup"><span data-stu-id="059a6-141">Edit controls implementing TSF can monitor for these changes via the **OnEndEdit** notification.</span></span><br/>         |
| [<span data-ttu-id="059a6-142">**CompositionFinalized**</span><span class="sxs-lookup"><span data-stu-id="059a6-142">**CompositionFinalized**</span></span>](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-texteditchangetype) | <span data-ttu-id="059a6-143">完成的組合字元串 (查看附注) </span><span class="sxs-lookup"><span data-stu-id="059a6-143">The finalized composition string (see Notes)</span></span> | <span data-ttu-id="059a6-144">在 TSF 中，要完成的轉換字串是由從組合中移除的 **GUID \_ \_ 組成** 旗標所定義。</span><span class="sxs-lookup"><span data-stu-id="059a6-144">In TSF, the conversion string being finalized is defined by the **GUID\_PROP\_COMPOSING** flag being removed from a composition.</span></span> <span data-ttu-id="059a6-145">執行 TSF 的編輯控制項應從 **EndComposition** 判斷已完成的字串，並在呼叫 **OnEndEdit** 時引發事件。</span><span class="sxs-lookup"><span data-stu-id="059a6-145">Edit controls implementing TSF should determine the finalized string from **EndComposition** and raise the event when **OnEndEdit** is called.</span></span><br/> <span data-ttu-id="059a6-146">如果組合已取消或刪除，則完成的組合字元串可能是空的。</span><span class="sxs-lookup"><span data-stu-id="059a6-146">The finalized composition string may be empty if composition was cancelled or deleted.</span></span><br/> |



 

### <a name="conversiontargetchanged"></a><span data-ttu-id="059a6-147">**ConversionTargetChanged**</span><span class="sxs-lookup"><span data-stu-id="059a6-147">**ConversionTargetChanged**</span></span>

-   <span data-ttu-id="059a6-148">當轉換目標從某個目標變更為另一個目標時，就會發生 **ConversionTargetChanged** 。</span><span class="sxs-lookup"><span data-stu-id="059a6-148">**ConversionTargetChanged** occurs when conversion target changes from one target to another.</span></span>
-   <span data-ttu-id="059a6-149">您可以使用 [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent) 函數來引發 **ConversionTargetChanged** 事件， (傳遞 [**UIA \_ macos textedit \_ ConversionTargetChangedEventId**](https://www.bing.com/search?q=**UIA\_TextEdit\_ConversionTargetChangedEventId**) 事件識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="059a6-149">Use the [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent) function to raise the **ConversionTargetChanged** event (pass the [**UIA\_TextEdit\_ConversionTargetChangedEventId**](https://www.bing.com/search?q=**UIA\_TextEdit\_ConversionTargetChangedEventId**) event identifier).</span></span>
-   <span data-ttu-id="059a6-150">當目標的內容變更時，不應引發 **ConversionTargetChanged** 。</span><span class="sxs-lookup"><span data-stu-id="059a6-150">**ConversionTargetChanged** should not be raised when the content of the target changes.</span></span> <span data-ttu-id="059a6-151">如果目標變更同時與組合變更發生，則必須在引發任何組合事件之後引發目標變更事件。</span><span class="sxs-lookup"><span data-stu-id="059a6-151">If the target change occurs simultaneous with a composition change, the target change event must be raised after any composition events have already been raised.</span></span>
-   <span data-ttu-id="059a6-152">在 TSF 中，轉換目標是由從 **tf \_ DISPLAYATTRIBUTE** 結構 **\_ \_ \_ 轉換成設定的 tf ATTR 目標** 值所定義。</span><span class="sxs-lookup"><span data-stu-id="059a6-152">In TSF, the conversion target is defined by the value **TF\_ATTR\_TARGET\_CONVERTED** being set from the **TF\_DISPLAYATTRIBUTE** structure.</span></span> <span data-ttu-id="059a6-153">您可以使用 **OnEndEdit** 來監視變更。</span><span class="sxs-lookup"><span data-stu-id="059a6-153">Changes can be monitored using **OnEndEdit**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="059a6-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="059a6-154">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="059a6-155">**概念**</span><span class="sxs-lookup"><span data-stu-id="059a6-155">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="059a6-156">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="059a6-156">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="059a6-157">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="059a6-157">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="059a6-158">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="059a6-158">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

