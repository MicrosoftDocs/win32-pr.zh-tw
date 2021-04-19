---
description: ICE23 會驗證每個對話方塊的控制項定位順序。
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978217"
---
# <a name="ice23"></a><span data-ttu-id="22e64-103">ICE23</span><span class="sxs-lookup"><span data-stu-id="22e64-103">ICE23</span></span>

<span data-ttu-id="22e64-104">ICE23 會驗證每個對話方塊的控制項定位順序。</span><span class="sxs-lookup"><span data-stu-id="22e64-104">ICE23 validates the control tab order for each dialog box.</span></span>

<span data-ttu-id="22e64-105">ICE23 會驗證 [對話方塊資料表](dialog-table.md) 和 [控制資料表](control-table.md)中的下列各項：</span><span class="sxs-lookup"><span data-stu-id="22e64-105">ICE23 validates the following in the [Dialog table](dialog-table.md) and [Control table](control-table.md):</span></span>

-   <span data-ttu-id="22e64-106">對話方塊資料表中的每一筆記錄都會指定控制項第一個資料行中的控制項，該控制項 \_ 存在於對話方塊資料行所指定的對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="22e64-106">That every record in the Dialog table specifies a control in the Control\_First column that exists in the dialog box specified by the Dialog column.</span></span>
-   <span data-ttu-id="22e64-107">控制資料表中的每一筆記錄都會指定控制項下一個資料行中的控制項，該控制項位於與 \_ 控制項資料行中所列控制項相同的對話方塊上，或控制項 \_ 下一個包含 Null 值。</span><span class="sxs-lookup"><span data-stu-id="22e64-107">That every record in the Control table specifies a control in the Control\_Next column that is on the same dialog as the control listed in the Control column, or Control\_Next contains the Null value.</span></span>
-   <span data-ttu-id="22e64-108">在控制 \_ 資料表中，控制下一個控制項的下一個專案之後，會產生單一、關閉的迴圈，並傳回初始控制項。</span><span class="sxs-lookup"><span data-stu-id="22e64-108">That following the Control\_Next entries from control to control in the Control table makes a single, closed, loop that comes back to the initial control.</span></span> <span data-ttu-id="22e64-109">並非每個控制項都必須在迴圈中，但迴圈必須通過控制項下一個資料行中有專案的每個控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="22e64-109">Not every control needs to be in the loop, but the loop must pass through every control that has an entry in the Control\_Next column.</span></span>

## <a name="result"></a><span data-ttu-id="22e64-110">結果</span><span class="sxs-lookup"><span data-stu-id="22e64-110">Result</span></span>

<span data-ttu-id="22e64-111">如果控制項的定位順序未在對話方塊中形成單一封閉迴圈，ICE23 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="22e64-111">ICE23 posts an error message if the tab order of controls does not form a single closed loop in the dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="22e64-112">範例</span><span class="sxs-lookup"><span data-stu-id="22e64-112">Example</span></span>

<span data-ttu-id="22e64-113">ICE23 會針對所顯示的範例張貼下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="22e64-113">ICE23 would post the following error messages for the example shown.</span></span>

-   <span data-ttu-id="22e64-114">Dialog1 沒有先有控制權 \_ 。</span><span class="sxs-lookup"><span data-stu-id="22e64-114">Dialog1 has no Control\_First.</span></span>
-   <span data-ttu-id="22e64-115">\_對話方塊 Dialog2 的第一個控制項參考不存在的控制項 ControlX。</span><span class="sxs-lookup"><span data-stu-id="22e64-115">Control\_First of dialog Dialog2 refers to nonexistent control ControlX.</span></span>
-   <span data-ttu-id="22e64-116">Dialog3 在控制項 ControlB 中有不正確結束定位順序。</span><span class="sxs-lookup"><span data-stu-id="22e64-116">Dialog3 has dead-end tab order at control ControlB.</span></span>
-   <span data-ttu-id="22e64-117">Dialog4 在控制項 ControlC 有格式不正確的定位順序</span><span class="sxs-lookup"><span data-stu-id="22e64-117">Dialog4 has malformed tab order at control ControlC</span></span>
-   <span data-ttu-id="22e64-118">Dialog5 在控制項 ControlC 上的定位順序格式錯誤。</span><span class="sxs-lookup"><span data-stu-id="22e64-118">Dialog5 has malformed tab order at control ControlC.</span></span>
-   <span data-ttu-id="22e64-119">控制 \_ 控制項 Dialog6 的下一個。 ControlC 連結至未知的控制項。</span><span class="sxs-lookup"><span data-stu-id="22e64-119">Control\_Next of control Dialog6.ControlC links to unknown control.</span></span>

<span data-ttu-id="22e64-120">[對話方塊資料表](dialog-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="22e64-120">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="22e64-121">對話</span><span class="sxs-lookup"><span data-stu-id="22e64-121">Dialog</span></span>  | <span data-ttu-id="22e64-122">\_先控制項</span><span class="sxs-lookup"><span data-stu-id="22e64-122">Control\_First</span></span> |
|---------|----------------|
| <span data-ttu-id="22e64-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="22e64-123">Dialog1</span></span> |                |
| <span data-ttu-id="22e64-124">Dialog2</span><span class="sxs-lookup"><span data-stu-id="22e64-124">Dialog2</span></span> | <span data-ttu-id="22e64-125">ControlX</span><span class="sxs-lookup"><span data-stu-id="22e64-125">ControlX</span></span>       |
| <span data-ttu-id="22e64-126">Dialog3</span><span class="sxs-lookup"><span data-stu-id="22e64-126">Dialog3</span></span> | <span data-ttu-id="22e64-127">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-127">ControlA</span></span>       |
| <span data-ttu-id="22e64-128">Dialog4</span><span class="sxs-lookup"><span data-stu-id="22e64-128">Dialog4</span></span> | <span data-ttu-id="22e64-129">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-129">ControlA</span></span>       |
| <span data-ttu-id="22e64-130">Dialog5</span><span class="sxs-lookup"><span data-stu-id="22e64-130">Dialog5</span></span> | <span data-ttu-id="22e64-131">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-131">ControlA</span></span>       |



 

<span data-ttu-id="22e64-132">[控制資料表](control-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="22e64-132">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="22e64-133">對話</span><span class="sxs-lookup"><span data-stu-id="22e64-133">Dialog</span></span>  | <span data-ttu-id="22e64-134">控制</span><span class="sxs-lookup"><span data-stu-id="22e64-134">Control</span></span>  | <span data-ttu-id="22e64-135">控制 \_ 下一步</span><span class="sxs-lookup"><span data-stu-id="22e64-135">Control\_Next</span></span> |
|---------|----------|---------------|
| <span data-ttu-id="22e64-136">Dialog1</span><span class="sxs-lookup"><span data-stu-id="22e64-136">Dialog1</span></span> | <span data-ttu-id="22e64-137">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-137">ControlA</span></span> |               |
| <span data-ttu-id="22e64-138">Dialog1</span><span class="sxs-lookup"><span data-stu-id="22e64-138">Dialog1</span></span> | <span data-ttu-id="22e64-139">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-139">ControlB</span></span> | <span data-ttu-id="22e64-140">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-140">ControlA</span></span>      |
| <span data-ttu-id="22e64-141">Dialog2</span><span class="sxs-lookup"><span data-stu-id="22e64-141">Dialog2</span></span> | <span data-ttu-id="22e64-142">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-142">ControlA</span></span> | <span data-ttu-id="22e64-143">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-143">ControlB</span></span>      |
| <span data-ttu-id="22e64-144">Dialog2</span><span class="sxs-lookup"><span data-stu-id="22e64-144">Dialog2</span></span> | <span data-ttu-id="22e64-145">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-145">ControlB</span></span> | <span data-ttu-id="22e64-146">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-146">ControlA</span></span>      |
| <span data-ttu-id="22e64-147">Dialog3</span><span class="sxs-lookup"><span data-stu-id="22e64-147">Dialog3</span></span> | <span data-ttu-id="22e64-148">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-148">ControlA</span></span> | <span data-ttu-id="22e64-149">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-149">ControlB</span></span>      |
| <span data-ttu-id="22e64-150">Dialog3</span><span class="sxs-lookup"><span data-stu-id="22e64-150">Dialog3</span></span> | <span data-ttu-id="22e64-151">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-151">ControlB</span></span> |               |
| <span data-ttu-id="22e64-152">Dialog4</span><span class="sxs-lookup"><span data-stu-id="22e64-152">Dialog4</span></span> | <span data-ttu-id="22e64-153">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-153">ControlA</span></span> | <span data-ttu-id="22e64-154">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-154">ControlB</span></span>      |
| <span data-ttu-id="22e64-155">Dialog4</span><span class="sxs-lookup"><span data-stu-id="22e64-155">Dialog4</span></span> | <span data-ttu-id="22e64-156">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-156">ControlB</span></span> | <span data-ttu-id="22e64-157">ControlC</span><span class="sxs-lookup"><span data-stu-id="22e64-157">ControlC</span></span>      |
| <span data-ttu-id="22e64-158">Dialog4</span><span class="sxs-lookup"><span data-stu-id="22e64-158">Dialog4</span></span> | <span data-ttu-id="22e64-159">ControlC</span><span class="sxs-lookup"><span data-stu-id="22e64-159">ControlC</span></span> | <span data-ttu-id="22e64-160">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-160">ControlB</span></span>      |
| <span data-ttu-id="22e64-161">Dialog5</span><span class="sxs-lookup"><span data-stu-id="22e64-161">Dialog5</span></span> | <span data-ttu-id="22e64-162">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-162">ControlA</span></span> | <span data-ttu-id="22e64-163">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-163">ControlB</span></span>      |
| <span data-ttu-id="22e64-164">Dialog5</span><span class="sxs-lookup"><span data-stu-id="22e64-164">Dialog5</span></span> | <span data-ttu-id="22e64-165">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-165">ControlB</span></span> | <span data-ttu-id="22e64-166">ControlC</span><span class="sxs-lookup"><span data-stu-id="22e64-166">ControlC</span></span>      |
| <span data-ttu-id="22e64-167">Dialog5</span><span class="sxs-lookup"><span data-stu-id="22e64-167">Dialog5</span></span> | <span data-ttu-id="22e64-168">ControlC</span><span class="sxs-lookup"><span data-stu-id="22e64-168">ControlC</span></span> | <span data-ttu-id="22e64-169">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-169">ControlA</span></span>      |
| <span data-ttu-id="22e64-170">Dialog5</span><span class="sxs-lookup"><span data-stu-id="22e64-170">Dialog5</span></span> | <span data-ttu-id="22e64-171">ControlD</span><span class="sxs-lookup"><span data-stu-id="22e64-171">ControlD</span></span> | <span data-ttu-id="22e64-172">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-172">ControlA</span></span>      |
| <span data-ttu-id="22e64-173">Dialog6</span><span class="sxs-lookup"><span data-stu-id="22e64-173">Dialog6</span></span> | <span data-ttu-id="22e64-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-174">ControlA</span></span> | <span data-ttu-id="22e64-175">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-175">ControlB</span></span>      |
| <span data-ttu-id="22e64-176">Dialog6</span><span class="sxs-lookup"><span data-stu-id="22e64-176">Dialog6</span></span> | <span data-ttu-id="22e64-177">ControlB</span><span class="sxs-lookup"><span data-stu-id="22e64-177">ControlB</span></span> | <span data-ttu-id="22e64-178">ControlC</span><span class="sxs-lookup"><span data-stu-id="22e64-178">ControlC</span></span>      |
| <span data-ttu-id="22e64-179">Dialog6</span><span class="sxs-lookup"><span data-stu-id="22e64-179">Dialog6</span></span> | <span data-ttu-id="22e64-180">ControlC</span><span class="sxs-lookup"><span data-stu-id="22e64-180">ControlC</span></span> | <span data-ttu-id="22e64-181">ControlX</span><span class="sxs-lookup"><span data-stu-id="22e64-181">ControlX</span></span>      |
| <span data-ttu-id="22e64-182">Dialog6</span><span class="sxs-lookup"><span data-stu-id="22e64-182">Dialog6</span></span> | <span data-ttu-id="22e64-183">ControlD</span><span class="sxs-lookup"><span data-stu-id="22e64-183">ControlD</span></span> | <span data-ttu-id="22e64-184">ControlA</span><span class="sxs-lookup"><span data-stu-id="22e64-184">ControlA</span></span>      |



 

<span data-ttu-id="22e64-185">若要修正這些錯誤，請注意上述表格中的下列各項，並進行指定的變更。</span><span class="sxs-lookup"><span data-stu-id="22e64-185">To fix these errors note the following in the above tables and make the indicated changes.</span></span>

<span data-ttu-id="22e64-186">並非對話方塊資料表中的每個資料列都有控制項第一個資料行中指定的控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="22e64-186">Not every row in the Dialog table has a control specified in the Control\_First column.</span></span> <span data-ttu-id="22e64-187">將 \_ 對話方塊資料表中 Dialog1 記錄的控制項第一個資料行變更為存在於 Dialog1 中的控制項。</span><span class="sxs-lookup"><span data-stu-id="22e64-187">Change the Control\_First column of the Dialog1 record in the Dialog table to a control that exists in Dialog1.</span></span>

<span data-ttu-id="22e64-188">並非對話方塊資料表中的每個資料列都有在對話方塊的控制項第一個資料行中指定的控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="22e64-188">Not every row in the Dialog table has a control specified in the Control\_First column that exists on the dialog box.</span></span> <span data-ttu-id="22e64-189">將 Dialog2 的 Control \_ First 資料行變更為存在於 Dialog2 中的控制項。</span><span class="sxs-lookup"><span data-stu-id="22e64-189">Change the Control\_First column of the Dialog2 to a control that exists in Dialog2.</span></span>

<span data-ttu-id="22e64-190">將 control 資料表中的 \_ 下一個控制項下的專案控制從控制項變更為，並不會在每一種情況下都進行關閉迴圈。</span><span class="sxs-lookup"><span data-stu-id="22e64-190">Following the Control\_Next entries in the Control table from control to control does not make a closed loop in every case.</span></span> <span data-ttu-id="22e64-191">將 \_ Dialog3 中 ControlB 的 [下一欄] 控制項變更為 ControlA。</span><span class="sxs-lookup"><span data-stu-id="22e64-191">Change the Control\_Next column for ControlB in Dialog3 to ControlA.</span></span>

<span data-ttu-id="22e64-192">將 control 資料表中的 \_ 下一個專案從 control 控制項移至 control 之後，不會在每個案例中導致初始控制項。</span><span class="sxs-lookup"><span data-stu-id="22e64-192">Following the Control\_Next entries in the Control table from control to control does not lead back to the initial control in every case.</span></span> <span data-ttu-id="22e64-193">將 \_ Dialog4 中 ControlC 的 [控制項下一欄] 變更為參考 ControlA。</span><span class="sxs-lookup"><span data-stu-id="22e64-193">Change the Control\_Next column for ControlC in Dialog4 to refer to ControlA.</span></span>

<span data-ttu-id="22e64-194">將 control 資料表中的下一個專案從 control 控制項下，控制項中的 \_ 下一個專案不會通過控制項下一個資料行中具有專案的對話方塊中的每個控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="22e64-194">Following the Control\_Next entries in the Control table from control to control does not pass through every control in the dialog box having an entry in the Control\_Next column.</span></span> <span data-ttu-id="22e64-195">將 \_ Dialog5 中 ControlC 的 [下一欄] 控制項變更為 ControlD。</span><span class="sxs-lookup"><span data-stu-id="22e64-195">Change the Control\_Next column for ControlC in Dialog5 to ControlD.</span></span>

<span data-ttu-id="22e64-196">[ \_ 下一步] 不是指與控制項資料行中所列控制項位於相同對話方塊中的有效控制項。</span><span class="sxs-lookup"><span data-stu-id="22e64-196">Control\_Next does not refer to a valid control that is in the same dialog as the control listed in the Control column.</span></span> <span data-ttu-id="22e64-197">將 \_ Dialog6 中 ControlC 的 [控制項下一欄] 變更為參考 ControlD。</span><span class="sxs-lookup"><span data-stu-id="22e64-197">Change the Control\_Next column for ControlC in Dialog6 to refer to ControlD.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22e64-198">相關主題</span><span class="sxs-lookup"><span data-stu-id="22e64-198">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22e64-199">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="22e64-199">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



