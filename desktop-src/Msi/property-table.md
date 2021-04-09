---
description: 屬性工作表包含安裝中所有已定義屬性的屬性名稱和值。 具有 Null 值的屬性不會出現在資料表中。
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: 屬性工作表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692963"
---
# <a name="property-table"></a><span data-ttu-id="fb27a-104">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="fb27a-104">Property Table</span></span>

<span data-ttu-id="fb27a-105">屬性工作表包含安裝中所有已定義屬性的屬性名稱和值。</span><span class="sxs-lookup"><span data-stu-id="fb27a-105">The Property table contains the property names and values for all defined properties in the installation.</span></span> <span data-ttu-id="fb27a-106">具有 Null 值的屬性不會出現在資料表中。</span><span class="sxs-lookup"><span data-stu-id="fb27a-106">Properties with Null values are not present in the table.</span></span>

<span data-ttu-id="fb27a-107">屬性資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="fb27a-107">The Property table has the following columns.</span></span>



| <span data-ttu-id="fb27a-108">Column</span><span class="sxs-lookup"><span data-stu-id="fb27a-108">Column</span></span>   | <span data-ttu-id="fb27a-109">類型</span><span class="sxs-lookup"><span data-stu-id="fb27a-109">Type</span></span>                         | <span data-ttu-id="fb27a-110">答案</span><span class="sxs-lookup"><span data-stu-id="fb27a-110">Key</span></span> | <span data-ttu-id="fb27a-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="fb27a-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="fb27a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fb27a-112">Property</span></span> | [<span data-ttu-id="fb27a-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="fb27a-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="fb27a-114">Y</span><span class="sxs-lookup"><span data-stu-id="fb27a-114">Y</span></span>   | <span data-ttu-id="fb27a-115">N</span><span class="sxs-lookup"><span data-stu-id="fb27a-115">N</span></span>        |
| <span data-ttu-id="fb27a-116">值</span><span class="sxs-lookup"><span data-stu-id="fb27a-116">Value</span></span>    | [<span data-ttu-id="fb27a-117">Text</span><span class="sxs-lookup"><span data-stu-id="fb27a-117">Text</span></span>](text.md)             | <span data-ttu-id="fb27a-118">N</span><span class="sxs-lookup"><span data-stu-id="fb27a-118">N</span></span>   | <span data-ttu-id="fb27a-119">N</span><span class="sxs-lookup"><span data-stu-id="fb27a-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fb27a-120">資料行</span><span class="sxs-lookup"><span data-stu-id="fb27a-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fb27a-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產</span><span class="sxs-lookup"><span data-stu-id="fb27a-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="fb27a-122">屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb27a-122">The name of a property.</span></span> <span data-ttu-id="fb27a-123">請參閱 [屬性](properties.md)。</span><span class="sxs-lookup"><span data-stu-id="fb27a-123">See [Properties](properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb27a-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="fb27a-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="fb27a-125">屬性的可當地語系化字串值。</span><span class="sxs-lookup"><span data-stu-id="fb27a-125">A localizable string value for the property.</span></span> <span data-ttu-id="fb27a-126">這可能永遠不會是 Null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="fb27a-126">This may never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb27a-127">備註</span><span class="sxs-lookup"><span data-stu-id="fb27a-127">Remarks</span></span>

<span data-ttu-id="fb27a-128">請注意，您不能使用屬性工作表將屬性設為另一個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="fb27a-128">Note that you cannot use the Property table to set a property to the value of another property.</span></span> <span data-ttu-id="fb27a-129">安裝程式在屬性資料行中設定屬性之前，不會對 [值] 資料行中輸入的文字字串執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="fb27a-129">The installer does nothing to the text string entered in the Value column before setting the property in the Property column.</span></span> <span data-ttu-id="fb27a-130">如果在屬性資料行中輸入 FirstProperty \[ ，並 \] 在 [值] 資料行中 SecondProperty，則 FirstProperty 的值會設定為文字字串 " \[ SecondProperty \] "，而非 SecondProperty 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="fb27a-130">If FirstProperty is entered into the Property column and \[SecondProperty\] in the Value column, the value of FirstProperty is set to the text string "\[SecondProperty\]" and not to the value of the SecondProperty property.</span></span> <span data-ttu-id="fb27a-131">這是防止在屬性工作表中建立迴圈參考的必要動作。</span><span class="sxs-lookup"><span data-stu-id="fb27a-131">This is necessary to prevent creating circular references in the Property table.</span></span> <span data-ttu-id="fb27a-132">相反地，您可以使用 [自訂動作類型 51](custom-action-type-51.md)，將一個屬性設定為另一個。</span><span class="sxs-lookup"><span data-stu-id="fb27a-132">Instead, you can set one property to another by using a [Custom Action Type 51](custom-action-type-51.md).</span></span>

<span data-ttu-id="fb27a-133">請注意， [**AdminProperties**](adminproperties.md) 屬性可以用來覆寫 [系統管理安裝](administrative-installation.md)期間屬性工作表中的值。</span><span class="sxs-lookup"><span data-stu-id="fb27a-133">Note that the [**AdminProperties**](adminproperties.md) property can be used to override the values in the Property table during an [Administrative Installation](administrative-installation.md).</span></span>

<span data-ttu-id="fb27a-134">請勿將屬性用於密碼或其他必須保持安全的資訊。</span><span class="sxs-lookup"><span data-stu-id="fb27a-134">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="fb27a-135">安裝程式可以將撰寫的屬性值寫入至記錄檔或系統登錄中，或在執行時間建立的屬性值。</span><span class="sxs-lookup"><span data-stu-id="fb27a-135">The installer may write the value of a property authored into the Property table, or created at runtime, into a log or the system registry.</span></span>

## <a name="validation"></a><span data-ttu-id="fb27a-136">驗證</span><span class="sxs-lookup"><span data-stu-id="fb27a-136">Validation</span></span>

<dl>

[<span data-ttu-id="fb27a-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="fb27a-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="fb27a-138">ICE05</span><span class="sxs-lookup"><span data-stu-id="fb27a-138">ICE05</span></span>](ice05.md)  
[<span data-ttu-id="fb27a-139">ICE06</span><span class="sxs-lookup"><span data-stu-id="fb27a-139">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="fb27a-140">ICE16</span><span class="sxs-lookup"><span data-stu-id="fb27a-140">ICE16</span></span>](ice16.md)  
[<span data-ttu-id="fb27a-141">ICE24</span><span class="sxs-lookup"><span data-stu-id="fb27a-141">ICE24</span></span>](ice24.md)  
[<span data-ttu-id="fb27a-142">ICE31</span><span class="sxs-lookup"><span data-stu-id="fb27a-142">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="fb27a-143">ICE34</span><span class="sxs-lookup"><span data-stu-id="fb27a-143">ICE34</span></span>](ice34.md)  
[<span data-ttu-id="fb27a-144">ICE36</span><span class="sxs-lookup"><span data-stu-id="fb27a-144">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="fb27a-145">ICE40</span><span class="sxs-lookup"><span data-stu-id="fb27a-145">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="fb27a-146">ICE46</span><span class="sxs-lookup"><span data-stu-id="fb27a-146">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="fb27a-147">ICE48</span><span class="sxs-lookup"><span data-stu-id="fb27a-147">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="fb27a-148">ICE52</span><span class="sxs-lookup"><span data-stu-id="fb27a-148">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="fb27a-149">ICE61</span><span class="sxs-lookup"><span data-stu-id="fb27a-149">ICE61</span></span>](ice61.md)  
[<span data-ttu-id="fb27a-150">ICE73</span><span class="sxs-lookup"><span data-stu-id="fb27a-150">ICE73</span></span>](ice73.md)  
[<span data-ttu-id="fb27a-151">ICE74</span><span class="sxs-lookup"><span data-stu-id="fb27a-151">ICE74</span></span>](ice74.md)  
[<span data-ttu-id="fb27a-152">ICE80</span><span class="sxs-lookup"><span data-stu-id="fb27a-152">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="fb27a-153">ICE87</span><span class="sxs-lookup"><span data-stu-id="fb27a-153">ICE87</span></span>](ice87.md)  
[<span data-ttu-id="fb27a-154">ICE88</span><span class="sxs-lookup"><span data-stu-id="fb27a-154">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="fb27a-155">ICE91</span><span class="sxs-lookup"><span data-stu-id="fb27a-155">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="fb27a-156">ICE99</span><span class="sxs-lookup"><span data-stu-id="fb27a-156">ICE99</span></span>](ice99.md)  
</dl>

 

 



