---
description: Session 物件的 EvaluateCondition 方法會評估包含符號和值的邏輯運算式。 這個方法會使用 MsiEvaluateCondition 函數。
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: EvaluateCondition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987164"
---
# <a name="sessionevaluatecondition-method"></a><span data-ttu-id="08d7d-104">EvaluateCondition 方法</span><span class="sxs-lookup"><span data-stu-id="08d7d-104">Session.EvaluateCondition method</span></span>

<span data-ttu-id="08d7d-105">[**Session**](session-object.md)物件的 **EvaluateCondition** 方法會評估包含符號和值的邏輯運算式。</span><span class="sxs-lookup"><span data-stu-id="08d7d-105">The **EvaluateCondition** method of the [**Session**](session-object.md) object evaluates a logical expression that contains symbols and values.</span></span> <span data-ttu-id="08d7d-106">這個方法會使用 [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) 函數。</span><span class="sxs-lookup"><span data-stu-id="08d7d-106">This method uses the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d7d-107">語法</span><span class="sxs-lookup"><span data-stu-id="08d7d-107">Syntax</span></span>


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a><span data-ttu-id="08d7d-108">參數</span><span class="sxs-lookup"><span data-stu-id="08d7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d7d-109">*條件*</span><span class="sxs-lookup"><span data-stu-id="08d7d-109">*condition*</span></span> 
</dt> <dd>

<span data-ttu-id="08d7d-110">包含邏輯運算式的必要字串。</span><span class="sxs-lookup"><span data-stu-id="08d7d-110">Required string that contains the logical expression.</span></span> <span data-ttu-id="08d7d-111">如需詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="08d7d-111">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d7d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="08d7d-112">Return value</span></span>

<span data-ttu-id="08d7d-113">這個方法會傳回整數，指出條件的評估。</span><span class="sxs-lookup"><span data-stu-id="08d7d-113">This method returns an integer that indicates the evaluation of the condition.</span></span>



| <span data-ttu-id="08d7d-114">常數</span><span class="sxs-lookup"><span data-stu-id="08d7d-114">Constant</span></span>                  | <span data-ttu-id="08d7d-115">值</span><span class="sxs-lookup"><span data-stu-id="08d7d-115">Value</span></span> | <span data-ttu-id="08d7d-116">描述</span><span class="sxs-lookup"><span data-stu-id="08d7d-116">Description</span></span>                               |
|---------------------------|-------|-------------------------------------------|
| <span data-ttu-id="08d7d-117">msiEvaluateConditionFalse</span><span class="sxs-lookup"><span data-stu-id="08d7d-117">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="08d7d-118">0</span><span class="sxs-lookup"><span data-stu-id="08d7d-118">0</span></span>     | <span data-ttu-id="08d7d-119">條件會評估為 false。</span><span class="sxs-lookup"><span data-stu-id="08d7d-119">The condition evaluates to false.</span></span>         |
| <span data-ttu-id="08d7d-120">msiEvaluateConditionTrue</span><span class="sxs-lookup"><span data-stu-id="08d7d-120">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="08d7d-121">1</span><span class="sxs-lookup"><span data-stu-id="08d7d-121">1</span></span>     | <span data-ttu-id="08d7d-122">條件評估為 true。</span><span class="sxs-lookup"><span data-stu-id="08d7d-122">The condition evaluates to true.</span></span>          |
| <span data-ttu-id="08d7d-123">msiEvaluateConditionNone</span><span class="sxs-lookup"><span data-stu-id="08d7d-123">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="08d7d-124">2</span><span class="sxs-lookup"><span data-stu-id="08d7d-124">2</span></span>     | <span data-ttu-id="08d7d-125">未提供條件運算式。</span><span class="sxs-lookup"><span data-stu-id="08d7d-125">A conditional expression is not provided.</span></span> |
| <span data-ttu-id="08d7d-126">msiEvaluateConditionError</span><span class="sxs-lookup"><span data-stu-id="08d7d-126">msiEvaluateConditionError</span></span> | <span data-ttu-id="08d7d-127">3</span><span class="sxs-lookup"><span data-stu-id="08d7d-127">3</span></span>     | <span data-ttu-id="08d7d-128">條件包含語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="08d7d-128">The condition contains a syntax error.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="08d7d-129">備註</span><span class="sxs-lookup"><span data-stu-id="08d7d-129">Remarks</span></span>

<span data-ttu-id="08d7d-130">條件運算式可以用來比較功能和元件狀態。</span><span class="sxs-lookup"><span data-stu-id="08d7d-130">Conditional expressions can be used to compare feature and component states.</span></span> <span data-ttu-id="08d7d-131">下表顯示 EvaluateCondition 方法所使用的功能和元件狀態。</span><span class="sxs-lookup"><span data-stu-id="08d7d-131">The following table shows the feature and component states that the EvaluateCondition method uses.</span></span>



| <span data-ttu-id="08d7d-132">狀態</span><span class="sxs-lookup"><span data-stu-id="08d7d-132">State</span></span>                 | <span data-ttu-id="08d7d-133">值</span><span class="sxs-lookup"><span data-stu-id="08d7d-133">Value</span></span> | <span data-ttu-id="08d7d-134">描述</span><span class="sxs-lookup"><span data-stu-id="08d7d-134">Description</span></span>                                              |
|-----------------------|-------|----------------------------------------------------------|
| <span data-ttu-id="08d7d-135">Null</span><span class="sxs-lookup"><span data-stu-id="08d7d-135">Null</span></span>                  | <span data-ttu-id="08d7d-136">Null</span><span class="sxs-lookup"><span data-stu-id="08d7d-136">Null</span></span>  | <span data-ttu-id="08d7d-137">未對功能或元件採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="08d7d-137">No action taken on feature or component.</span></span>                 |
| <span data-ttu-id="08d7d-138">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="08d7d-138">msiInstallStateAbsent</span></span> | <span data-ttu-id="08d7d-139">2</span><span class="sxs-lookup"><span data-stu-id="08d7d-139">2</span></span>     | <span data-ttu-id="08d7d-140">功能或元件不存在。</span><span class="sxs-lookup"><span data-stu-id="08d7d-140">Feature or component is not present.</span></span>                     |
| <span data-ttu-id="08d7d-141">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="08d7d-141">msiInstallStateLocal</span></span>  | <span data-ttu-id="08d7d-142">3</span><span class="sxs-lookup"><span data-stu-id="08d7d-142">3</span></span>     | <span data-ttu-id="08d7d-143">功能或元件安裝在本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="08d7d-143">Feature or component is installed on the local computer.</span></span> |
| <span data-ttu-id="08d7d-144">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="08d7d-144">msiInstallStateSource</span></span> | <span data-ttu-id="08d7d-145">4</span><span class="sxs-lookup"><span data-stu-id="08d7d-145">4</span></span>     | <span data-ttu-id="08d7d-146">已安裝功能或元件以從來源執行。</span><span class="sxs-lookup"><span data-stu-id="08d7d-146">Feature or component is installed to run from source.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="08d7d-147">在呼叫 [**SetInstallLevel**](session-setinstalllevel.md) 方法之前（不論是直接或透過 [CostFinalize 動作](costfinalize-action.md)），都不會設定狀態。</span><span class="sxs-lookup"><span data-stu-id="08d7d-147">The states are not set until the [**SetInstallLevel**](session-setinstalllevel.md) method is called, either directly or by the [CostFinalize Action](costfinalize-action.md).</span></span> <span data-ttu-id="08d7d-148">因此，狀態檢查只適用于動作順序資料表中的條件運算式。</span><span class="sxs-lookup"><span data-stu-id="08d7d-148">Therefore, state checking is only useful in conditional expression in an action sequence table.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08d7d-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="08d7d-149">Requirements</span></span>



| <span data-ttu-id="08d7d-150">需求</span><span class="sxs-lookup"><span data-stu-id="08d7d-150">Requirement</span></span> | <span data-ttu-id="08d7d-151">值</span><span class="sxs-lookup"><span data-stu-id="08d7d-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d7d-152">版本</span><span class="sxs-lookup"><span data-stu-id="08d7d-152">Version</span></span><br/> | <span data-ttu-id="08d7d-153">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="08d7d-153">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="08d7d-154">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="08d7d-154">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="08d7d-155">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="08d7d-155">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="08d7d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="08d7d-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="08d7d-157"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08d7d-157"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="08d7d-158">IID</span><span class="sxs-lookup"><span data-stu-id="08d7d-158">IID</span></span><br/>     | <span data-ttu-id="08d7d-159">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="08d7d-159">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="08d7d-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08d7d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d7d-161">條件陳述式語法</span><span class="sxs-lookup"><span data-stu-id="08d7d-161">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 




