---
title: 錯誤處理策略
description: 錯誤處理策略
ms.assetid: 8d03ede8-0661-43dc-adaf-3c1f5fc1687e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c594a8b1e5baf0eab3d928b8f1b861b7f0160d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "104462692"
---
# <a name="error-handling-strategies"></a><span data-ttu-id="898a3-103">錯誤處理策略</span><span class="sxs-lookup"><span data-stu-id="898a3-103">Error Handling Strategies</span></span>

<span data-ttu-id="898a3-104">因為介面方法是虛擬的，所以呼叫端不可能知道任何一個呼叫可能傳回的一組完整值。</span><span class="sxs-lookup"><span data-stu-id="898a3-104">Because interface methods are virtual, it is not possible for a caller to know the full set of values that may be returned from any one call.</span></span> <span data-ttu-id="898a3-105">方法的一種實值可能會傳回五個值;另一個可能會傳回八個。</span><span class="sxs-lookup"><span data-stu-id="898a3-105">One implementation of a method may return five values; another may return eight.</span></span>

<span data-ttu-id="898a3-106">檔會列出每個方法可能傳回的常見值;這些是您必須在程式碼中檢查和處理的值，因為它們具有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="898a3-106">The documentation lists common values that may be returned for each method; these are the values that you must check for and handle in your code because they have special meanings.</span></span> <span data-ttu-id="898a3-107">可能會傳回其他值，但因為它們沒有意義，所以您不需要撰寫特殊的程式碼來處理它們。</span><span class="sxs-lookup"><span data-stu-id="898a3-107">Other values may be returned, but because they are not meaningful, you do not need to write special code to handle them.</span></span> <span data-ttu-id="898a3-108">零或非零的簡單檢查即已足夠。</span><span class="sxs-lookup"><span data-stu-id="898a3-108">A simple check for zero or nonzero is adequate.</span></span>

## <a name="hresult-values"></a><span data-ttu-id="898a3-109">HRESULT 值</span><span class="sxs-lookup"><span data-stu-id="898a3-109">HRESULT Values</span></span>

<span data-ttu-id="898a3-110">COM 函數和方法的傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="898a3-110">The return value of COM functions and methods is an **HRESULT**.</span></span> <span data-ttu-id="898a3-111">某些 Hresult 的值已在 COM 中變更，以消除所有重複和與系統錯誤碼重迭的情況。</span><span class="sxs-lookup"><span data-stu-id="898a3-111">The values of some HRESULTs have been changed in COM to eliminate all duplication and overlapping with the system error codes.</span></span> <span data-ttu-id="898a3-112">重複系統錯誤碼的系統已變更為 [設備 \_ WIN32]，而重迭的則會保留在設備 \_ Null 中。</span><span class="sxs-lookup"><span data-stu-id="898a3-112">Those that duplicate system error codes have been changed to FACILITY\_WIN32, and those that overlap remain in FACILITY\_NULL.</span></span> <span data-ttu-id="898a3-113">下表列出常見的 **HRESULT** 值和其值。</span><span class="sxs-lookup"><span data-stu-id="898a3-113">Common **HRESULT** values and their values are listed in the following table.</span></span>



| <span data-ttu-id="898a3-114">HRESULT</span><span class="sxs-lookup"><span data-stu-id="898a3-114">HRESULT</span></span>                    | <span data-ttu-id="898a3-115">值</span><span class="sxs-lookup"><span data-stu-id="898a3-115">Value</span></span>                 | <span data-ttu-id="898a3-116">描述</span><span class="sxs-lookup"><span data-stu-id="898a3-116">Description</span></span>                                                                                                                                        |
|----------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="898a3-117">E \_ 中止</span><span class="sxs-lookup"><span data-stu-id="898a3-117">E\_ABORT</span></span><br/>        | <span data-ttu-id="898a3-118">0x80004004</span><span class="sxs-lookup"><span data-stu-id="898a3-118">0x80004004</span></span><br/> | <span data-ttu-id="898a3-119">作業已中止，因為發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="898a3-119">The operation was aborted because of an unspecified error.</span></span><br/>                                                                              |
| <span data-ttu-id="898a3-120">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="898a3-120">E\_ACCESSDENIED</span></span><br/> | <span data-ttu-id="898a3-121">0x80070005</span><span class="sxs-lookup"><span data-stu-id="898a3-121">0x80070005</span></span><br/> | <span data-ttu-id="898a3-122">一般拒絕存取的錯誤。</span><span class="sxs-lookup"><span data-stu-id="898a3-122">A general access-denied error.</span></span><br/>                                                                                                          |
| <span data-ttu-id="898a3-123">E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="898a3-123">E\_FAIL</span></span><br/>         | <span data-ttu-id="898a3-124">0x80004005</span><span class="sxs-lookup"><span data-stu-id="898a3-124">0x80004005</span></span><br/> | <span data-ttu-id="898a3-125">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="898a3-125">An unspecified failure has occurred.</span></span><br/>                                                                                                    |
| <span data-ttu-id="898a3-126">E \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="898a3-126">E\_HANDLE</span></span><br/>       | <span data-ttu-id="898a3-127">0x80070006</span><span class="sxs-lookup"><span data-stu-id="898a3-127">0x80070006</span></span><br/> | <span data-ttu-id="898a3-128">使用了不正確控制碼。</span><span class="sxs-lookup"><span data-stu-id="898a3-128">An invalid handle was used.</span></span><br/>                                                                                                             |
| <span data-ttu-id="898a3-129">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="898a3-129">E\_INVALIDARG</span></span><br/>   | <span data-ttu-id="898a3-130">0x80070057</span><span class="sxs-lookup"><span data-stu-id="898a3-130">0x80070057</span></span><br/> | <span data-ttu-id="898a3-131">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="898a3-131">One or more arguments are invalid.</span></span><br/>                                                                                                      |
| <span data-ttu-id="898a3-132">E \_ NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="898a3-132">E\_NOINTERFACE</span></span><br/>  | <span data-ttu-id="898a3-133">0x80004002</span><span class="sxs-lookup"><span data-stu-id="898a3-133">0x80004002</span></span><br/> | <span data-ttu-id="898a3-134">[**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))方法無法辨識要求的介面。</span><span class="sxs-lookup"><span data-stu-id="898a3-134">The [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) method did not recognize the requested interface.</span></span> <span data-ttu-id="898a3-135">不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="898a3-135">The interface is not supported.</span></span><br/> |
| <span data-ttu-id="898a3-136">E \_ >NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="898a3-136">E\_NOTIMPL</span></span><br/>      | <span data-ttu-id="898a3-137">0x80004001</span><span class="sxs-lookup"><span data-stu-id="898a3-137">0x80004001</span></span><br/> | <span data-ttu-id="898a3-138">此方法尚未實作。</span><span class="sxs-lookup"><span data-stu-id="898a3-138">The method is not implemented.</span></span><br/>                                                                                                          |
| <span data-ttu-id="898a3-139">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="898a3-139">E\_OUTOFMEMORY</span></span><br/>  | <span data-ttu-id="898a3-140">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="898a3-140">0x8007000E</span></span><br/> | <span data-ttu-id="898a3-141">方法無法配置所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="898a3-141">The method failed to allocate necessary memory.</span></span><br/>                                                                                         |
| <span data-ttu-id="898a3-142">E \_ 暫止</span><span class="sxs-lookup"><span data-stu-id="898a3-142">E\_PENDING</span></span><br/>      | <span data-ttu-id="898a3-143">0x8000000A</span><span class="sxs-lookup"><span data-stu-id="898a3-143">0x8000000A</span></span><br/> | <span data-ttu-id="898a3-144">尚未提供完成作業所需的資料。</span><span class="sxs-lookup"><span data-stu-id="898a3-144">The data necessary to complete the operation is not yet available.</span></span><br/>                                                                      |
| <span data-ttu-id="898a3-145">E \_ 指標</span><span class="sxs-lookup"><span data-stu-id="898a3-145">E\_POINTER</span></span><br/>      | <span data-ttu-id="898a3-146">且顯示0x80004003</span><span class="sxs-lookup"><span data-stu-id="898a3-146">0x80004003</span></span><br/> | <span data-ttu-id="898a3-147">使用了不正確指標。</span><span class="sxs-lookup"><span data-stu-id="898a3-147">An invalid pointer was used.</span></span><br/>                                                                                                            |
| <span data-ttu-id="898a3-148">E 未 \_ 預期</span><span class="sxs-lookup"><span data-stu-id="898a3-148">E\_UNEXPECTED</span></span><br/>   | <span data-ttu-id="898a3-149">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="898a3-149">0x8000FFFF</span></span><br/> | <span data-ttu-id="898a3-150">發生嚴重失敗。</span><span class="sxs-lookup"><span data-stu-id="898a3-150">A catastrophic failure has occurred.</span></span><br/>                                                                                                    |
| <span data-ttu-id="898a3-151">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="898a3-151">S\_FALSE</span></span><br/>        | <span data-ttu-id="898a3-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="898a3-152">0x00000001</span></span><br/> | <span data-ttu-id="898a3-153">方法成功，並傳回布林值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="898a3-153">The method succeeded and returned the boolean value **FALSE**.</span></span><br/>                                                                          |
| <span data-ttu-id="898a3-154">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="898a3-154">S\_OK</span></span><br/>           | <span data-ttu-id="898a3-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="898a3-155">0x00000000</span></span><br/> | <span data-ttu-id="898a3-156">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="898a3-156">The method succeeded.</span></span> <span data-ttu-id="898a3-157">如果預期會傳回布林值，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="898a3-157">If a boolean return value is expected, the returned value is **TRUE**.</span></span><br/>                                            |



 

## <a name="network-errors"></a><span data-ttu-id="898a3-158">網路錯誤</span><span class="sxs-lookup"><span data-stu-id="898a3-158">Network Errors</span></span>

<span data-ttu-id="898a3-159">如果錯誤碼的前四個數字為8007，這表示系統或網路錯誤。</span><span class="sxs-lookup"><span data-stu-id="898a3-159">If the first four digits of the error code are 8007, this indicates a system or network error.</span></span> <span data-ttu-id="898a3-160">您可以使用 **net** 命令來解碼這些類型的錯誤。</span><span class="sxs-lookup"><span data-stu-id="898a3-160">You can use the **net** command to decode these types of errors.</span></span> <span data-ttu-id="898a3-161">若要解碼錯誤，請先將十六進位錯誤碼的最後四個數字轉換成 decimal。</span><span class="sxs-lookup"><span data-stu-id="898a3-161">To decode the error, first convert the last four digits of the hexadecimal error code to decimal.</span></span> <span data-ttu-id="898a3-162">然後，在命令提示字元中輸入下列命令，其中的十進位碼會以您要解碼的傳回值取代：</span><span class="sxs-lookup"><span data-stu-id="898a3-162">Then, at the command prompt, type the following, where decimal code is replaced with the return value you want to decode:</span></span>

<span data-ttu-id="898a3-163">**net helpmsg <***十進位 \_ 碼***>**</span><span class="sxs-lookup"><span data-stu-id="898a3-163">**net helpmsg <***decimal\_code***>**</span></span>

<span data-ttu-id="898a3-164">Net 命令會傳回錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="898a3-164">The net command returns a description of the error.</span></span> <span data-ttu-id="898a3-165">例如，如果 COM 傳回錯誤8007054B，請將054B 轉換為 decimal (1355) 。</span><span class="sxs-lookup"><span data-stu-id="898a3-165">For example, if COM returns the error 8007054B, convert the 054B to decimal (1355).</span></span> <span data-ttu-id="898a3-166">接著輸入下列內容：</span><span class="sxs-lookup"><span data-stu-id="898a3-166">Then type the following:</span></span>

<span data-ttu-id="898a3-167">**net helpmsg 1355**</span><span class="sxs-lookup"><span data-stu-id="898a3-167">**net helpmsg 1355**</span></span>

<span data-ttu-id="898a3-168">Net 命令會傳回錯誤描述：「指定的網域不存在」。</span><span class="sxs-lookup"><span data-stu-id="898a3-168">The net command returns the error description: "The specified domain did not exist".</span></span>

## <a name="related-topics"></a><span data-ttu-id="898a3-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="898a3-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="898a3-170">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="898a3-170">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 





