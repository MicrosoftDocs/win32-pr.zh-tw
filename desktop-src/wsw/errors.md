---
title: Errors
description: 本節將概述在執行命令失敗時，Windows Web 服務功能可能會發生的錯誤。
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Windows 的錯誤 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839583"
---
# <a name="errors"></a><span data-ttu-id="1ff51-106">Errors</span><span class="sxs-lookup"><span data-stu-id="1ff51-106">Errors</span></span>

<span data-ttu-id="1ff51-107">本節將概述在執行命令失敗時，Windows Web 服務功能可能會發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1ff51-107">This section outlines error that may be issues by Windows Web Services functions in result of a failure to execute the command.</span></span>

-   [<span data-ttu-id="1ff51-108">Out 參數</span><span class="sxs-lookup"><span data-stu-id="1ff51-108">Out Parameters</span></span>](#out-parameters)
-   [<span data-ttu-id="1ff51-109">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1ff51-109">Error Codes</span></span>](#error-codes)
-   [<span data-ttu-id="1ff51-110">豐富的錯誤</span><span class="sxs-lookup"><span data-stu-id="1ff51-110">Rich Errors</span></span>](#rich-errors)
-   [<span data-ttu-id="1ff51-111">錯誤和錯誤</span><span class="sxs-lookup"><span data-stu-id="1ff51-111">Faults and Errors</span></span>](#faults-and-errors)
-   [<span data-ttu-id="1ff51-112">語言敏感性錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="1ff51-112">Language Sensitive Error Information</span></span>](#language-sensitive-error-information)
-   [<span data-ttu-id="1ff51-113">標準錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1ff51-113">Canonical Error Codes</span></span>](#canonical-error-codes)
-   [<span data-ttu-id="1ff51-114">API 使用方式無效</span><span class="sxs-lookup"><span data-stu-id="1ff51-114">Invalid API Usage</span></span>](#invalid-api-usage)
-   [<span data-ttu-id="1ff51-115">安全性</span><span class="sxs-lookup"><span data-stu-id="1ff51-115">Security</span></span>](#security)

## <a name="out-parameters"></a><span data-ttu-id="1ff51-116">Out 參數</span><span class="sxs-lookup"><span data-stu-id="1ff51-116">Out Parameters</span></span>

<span data-ttu-id="1ff51-117">一般來說，如果函式失敗，就不會修改 out 參數的值。</span><span class="sxs-lookup"><span data-stu-id="1ff51-117">As a general rule, the value of out parameters are not modified if a function fails.</span></span>

<span data-ttu-id="1ff51-118">如果函式失敗，則會有一些會修改 out 參數的實例。</span><span class="sxs-lookup"><span data-stu-id="1ff51-118">There are a few instances where out parameters are modified if the function fails.</span></span> <span data-ttu-id="1ff51-119">這些案例會在每個參數的檔中明確地呼叫。</span><span class="sxs-lookup"><span data-stu-id="1ff51-119">These cases are explicitly called out in the documentation for each parameter.</span></span> <span data-ttu-id="1ff51-120">如果檔未提及在失敗情況下修改 out 參數的任何專案，則您可以安全地假設函式不會修改它們。</span><span class="sxs-lookup"><span data-stu-id="1ff51-120">If the documentation does not mention anything about modifying out parameters in the case of failure, then you can safely assume that the function will not modify them.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1ff51-121">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1ff51-121">Error Codes</span></span>

<span data-ttu-id="1ff51-122">所有錯誤傳回碼都是 Hresult。</span><span class="sxs-lookup"><span data-stu-id="1ff51-122">All error return codes are HRESULTs.</span></span> <span data-ttu-id="1ff51-123">此 API 會在設備 WEBSERVICES 範圍中定義一組 Hresult \_ ，但也會傳回 WINDOWS API 中其他位置所定義的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1ff51-123">This API defines a set of HRESULTs in the FACILITY\_WEBSERVICES range, but also returns errors defined elsewhere in the Windows API.</span></span>

<span data-ttu-id="1ff51-124">請參閱特定 API 的檔，以瞭解傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1ff51-124">Refer to the documentation for specific API's to learn about which error codes are returned.</span></span> <span data-ttu-id="1ff51-125">此清單並非針對每個 API 提供詳盡的清單，而是一份錯誤碼清單，其中包含明確處理的常見案例。</span><span class="sxs-lookup"><span data-stu-id="1ff51-125">The list is not intended to be exhaustive for each API, but rather a list of error codes for which there are common scenarios for explicit handling.</span></span> <span data-ttu-id="1ff51-126">呼叫端應該一律假設任何 API 都有其他錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1ff51-126">A caller should always assume other error codes are possible from any API.</span></span>

<span data-ttu-id="1ff51-127">此 API 會定義相對較少的錯誤碼，這會對應至程式會想要根據錯誤採取動作的案例。</span><span class="sxs-lookup"><span data-stu-id="1ff51-127">This API defines a relatively small number of error codes, which correspond to scenarios where a program will want to take action based on the error.</span></span> <span data-ttu-id="1ff51-128">單獨使用錯誤碼可能不足以判斷發生錯誤的原因，或為了提供問題給使用者的良好描述。</span><span class="sxs-lookup"><span data-stu-id="1ff51-128">Error codes alone may not be sufficient in order to determine what went wrong, or in order to provide a good description of the problem to the user.</span></span> <span data-ttu-id="1ff51-129">最瞭解問題的原因是使用豐富的錯誤，如下所述。</span><span class="sxs-lookup"><span data-stu-id="1ff51-129">The best understanding of the problem comes from using Rich Errors, as described below.</span></span>

## <a name="rich-errors"></a><span data-ttu-id="1ff51-130">豐富的錯誤</span><span class="sxs-lookup"><span data-stu-id="1ff51-130">Rich Errors</span></span>

<span data-ttu-id="1ff51-131">若要傳回錯誤碼，呼叫者可以選擇性地傳遞非 **Null** 的 [WS \_ error](ws-error.md)物件，要求任何 API 呼叫的豐富錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="1ff51-131">In additional to returning an error code, a caller may optionally request rich error information for any API call by passing a non-**NULL**[WS\_ERROR](ws-error.md) object.</span></span> <span data-ttu-id="1ff51-132">若要建立錯誤物件，請使用 [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror)。</span><span class="sxs-lookup"><span data-stu-id="1ff51-132">To create an error object, use [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror).</span></span> <span data-ttu-id="1ff51-133">如果發生錯誤，則造成錯誤的 API 將會在錯誤物件中填入有關錯誤狀況的其他內容。</span><span class="sxs-lookup"><span data-stu-id="1ff51-133">If there is an error, then the API that caused the error will fill the error object with additional context about the error situation.</span></span> <span data-ttu-id="1ff51-134">如果沒有發生錯誤，則錯誤物件是未修改的。</span><span class="sxs-lookup"><span data-stu-id="1ff51-134">If there is no error, then the error object is unmodified.</span></span> <span data-ttu-id="1ff51-135">傳遞 **Null** 錯誤物件表示呼叫端對豐富的錯誤資訊不感興趣。</span><span class="sxs-lookup"><span data-stu-id="1ff51-135">Passing a **NULL** error object indicates that the caller is not interested in rich error information.</span></span> <span data-ttu-id="1ff51-136">被呼叫端 (包括回呼) 必須準備處理 **Null** 錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="1ff51-136">Callees (including callbacks) must be prepared to handle **NULL** error objects.</span></span>

<span data-ttu-id="1ff51-137">請注意，相同的錯誤物件可以用於多個 API 呼叫，但是一次只能用於一個 API 呼叫 (因為它是單一執行緒) 。</span><span class="sxs-lookup"><span data-stu-id="1ff51-137">Note that the same error object can be used for multiple API calls, but may only be used for one API call at a time (as it is single threaded).</span></span> <span data-ttu-id="1ff51-138">每次發生錯誤時，就會將錯誤資訊附加至 error 物件。</span><span class="sxs-lookup"><span data-stu-id="1ff51-138">Each time an error occurs, error information is appended to the error object.</span></span> <span data-ttu-id="1ff51-139">當呼叫鏈回溯時，多個函式可能會將資訊新增至 error 物件，以提供有關錯誤的其他內容。</span><span class="sxs-lookup"><span data-stu-id="1ff51-139">As a call chain unwinds, multiple functions may add information to the error object to provide additional context about the error.</span></span> <span data-ttu-id="1ff51-140">若要在重複使用之前清除 error 物件的內容 () 發生錯誤時，請使用 [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror)。</span><span class="sxs-lookup"><span data-stu-id="1ff51-140">To clear the contents of the error object before reusing it (after an error occurs), use [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror).</span></span> <span data-ttu-id="1ff51-141">如果未發生任何錯誤，在重複使用之前，不需要重設錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="1ff51-141">If no error occurs, it is not necessary to reset the error object before reusing it.</span></span>

<span data-ttu-id="1ff51-142">豐富的錯誤資訊包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="1ff51-142">Rich error information consists of the following:</span></span>

-   <span data-ttu-id="1ff51-143">一組屬性值，提供錯誤的其他相關資訊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="1ff51-143">A set of property values, which provide additional information about the error if present.</span></span> <span data-ttu-id="1ff51-144">請參閱 [**WS \_ ERROR \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)。</span><span class="sxs-lookup"><span data-stu-id="1ff51-144">See [**WS\_ERROR\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).</span></span>
-   <span data-ttu-id="1ff51-145">零或多個錯誤字串。</span><span class="sxs-lookup"><span data-stu-id="1ff51-145">Zero or more error strings.</span></span> <span data-ttu-id="1ff51-146">您可以使用 [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)來新增字串，並且可以使用 [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring)來查詢。</span><span class="sxs-lookup"><span data-stu-id="1ff51-146">The strings are added using [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring), and can be queried using using [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring).</span></span> <span data-ttu-id="1ff51-147">您可以使用 [**WS \_ ERROR \_ PROPERTY \_ STRING \_ COUNT**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)來查詢字串的數目。</span><span class="sxs-lookup"><span data-stu-id="1ff51-147">The number of strings can be queried using [**WS\_ERROR\_PROPERTY\_STRING\_COUNT**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span></span>

## <a name="faults-and-errors"></a><span data-ttu-id="1ff51-148">錯誤和錯誤</span><span class="sxs-lookup"><span data-stu-id="1ff51-148">Faults and Errors</span></span>

<span data-ttu-id="1ff51-149">如需有關錯誤和錯誤如何相關的詳細資訊，請參閱 [錯誤](faults.md) 。</span><span class="sxs-lookup"><span data-stu-id="1ff51-149">See [Faults](faults.md) for information about how errors and faults relate.</span></span>

## <a name="language-sensitive-error-information"></a><span data-ttu-id="1ff51-150">語言敏感性錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="1ff51-150">Language Sensitive Error Information</span></span>

<span data-ttu-id="1ff51-151">建立錯誤物件時，會指定所需語言翻譯的 LANGID，以取得錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="1ff51-151">When creating an error object, the LANGID of the desired language translation for error information is specified.</span></span> <span data-ttu-id="1ff51-152">這是在將錯誤資訊加入錯誤物件時使用。</span><span class="sxs-lookup"><span data-stu-id="1ff51-152">This is used when adding error information to the error object.</span></span>

<span data-ttu-id="1ff51-153">您可以使用 [**WS \_ ERROR \_ 屬性 \_ LANGID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)來抓取或設定此語言值。</span><span class="sxs-lookup"><span data-stu-id="1ff51-153">This language value can be retrieved or set using [**WS\_ERROR\_PROPERTY\_LANGID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).</span></span>

## <a name="canonical-error-codes"></a><span data-ttu-id="1ff51-154">標準錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1ff51-154">Canonical Error Codes</span></span>

<span data-ttu-id="1ff51-155">此 API 提供一組標準的錯誤碼 (WS \_ E \_ \*) ，可讓您使用不同的通訊技術，而不需要依賴特定基礎執行的特定錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1ff51-155">This API provides a canonical set of error codes (WS\_E\_\*) that allow for different communication technologies to be used without having to depend on the specific error codes of the specific underlying implementation.</span></span> <span data-ttu-id="1ff51-156">如需這些錯誤碼的完整清單，請參閱 [Windows Web 服務傳回值](windows-web-services-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="1ff51-156">For a complete list of these error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="1ff51-157">例如，這可讓程式檢查是否有使用 TCP、UDP 或 HTTP 的錯誤代碼 **WS \_ E \_ 端點 \_ \_** ，並採取一些動作 (例如嘗試使用不同的端點) 。</span><span class="sxs-lookup"><span data-stu-id="1ff51-157">This allows, for example, a program to check for the error code **WS\_E\_ENDPOINT\_NOT\_FOUND** whether using TCP, UDP, or HTTP, and take some action (like attempting to use a different endpoint).</span></span>

<span data-ttu-id="1ff51-158">當執行特定錯誤碼對應至標準錯誤時，原始錯誤碼會儲存在錯誤物件中，而且可能仍可供診斷之用。</span><span class="sxs-lookup"><span data-stu-id="1ff51-158">When an implementation specific error code is mapped to a canonical error, the original error code is saved in the error object, and may still be accessed for diagnostic purposes.</span></span> <span data-ttu-id="1ff51-159">如需詳細資訊，請參閱 [**WS \_ error \_ 屬性 \_ 原始 \_ 錯誤碼 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) 。</span><span class="sxs-lookup"><span data-stu-id="1ff51-159">See [**WS\_ERROR\_PROPERTY\_ORIGINAL\_ERROR\_CODE**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) for more information.</span></span>

## <a name="invalid-api-usage"></a><span data-ttu-id="1ff51-160">API 使用方式無效</span><span class="sxs-lookup"><span data-stu-id="1ff51-160">Invalid API Usage</span></span>

<span data-ttu-id="1ff51-161">下列錯誤碼保留給不正確 API 使用，在其他情況下則不會傳回。</span><span class="sxs-lookup"><span data-stu-id="1ff51-161">The following error codes are reserved for invalid API usage, and will not be returned in other circumstances.</span></span> <span data-ttu-id="1ff51-162">如果傳回任何錯誤，則可能是應用程式錯誤的指示。</span><span class="sxs-lookup"><span data-stu-id="1ff51-162">If any of these errors are returned it may be an indication of an application bug.</span></span>

-   <span data-ttu-id="1ff51-163">**WS \_ E \_ 不正確作業 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-163">**WS\_E\_INVALID\_OPERATION**</span></span>
-   <span data-ttu-id="1ff51-164">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="1ff51-164">**E\_INVALIDARG**</span></span>

<span data-ttu-id="1ff51-165">下列列舉是追蹤的一部分：</span><span class="sxs-lookup"><span data-stu-id="1ff51-165">The following enumerations are part of tracing:</span></span>

-   [<span data-ttu-id="1ff51-166">**WS \_ ERROR \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="1ff51-166">**WS\_ERROR\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [<span data-ttu-id="1ff51-167">**WS \_ 例外狀況 \_ 代碼**</span><span class="sxs-lookup"><span data-stu-id="1ff51-167">**WS\_EXCEPTION\_CODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

<span data-ttu-id="1ff51-168">下列錯誤碼屬於追蹤的一部分：</span><span class="sxs-lookup"><span data-stu-id="1ff51-168">The following error codes are part of tracing:</span></span>

-   <span data-ttu-id="1ff51-169">**CERT \_ E \_ CN \_ 沒有 \_ 相符**</span><span class="sxs-lookup"><span data-stu-id="1ff51-169">**CERT\_E\_CN\_NO\_MATCH**</span></span>
-   <span data-ttu-id="1ff51-170">**CERT \_ E 已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="1ff51-170">**CERT\_E\_EXPIRED**</span></span>
-   <span data-ttu-id="1ff51-171">**CERT \_ E \_ UNTRUSTEDROOT**</span><span class="sxs-lookup"><span data-stu-id="1ff51-171">**CERT\_E\_UNTRUSTEDROOT**</span></span>
-   <span data-ttu-id="1ff51-172">**CERT \_ E \_ 錯誤的 \_ 使用方式**</span><span class="sxs-lookup"><span data-stu-id="1ff51-172">**CERT\_E\_WRONG\_USAGE**</span></span>
-   <span data-ttu-id="1ff51-173">**\_離線 CRYPT 電子 \_ 撤銷 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-173">**CRYPT\_E\_REVOCATION\_OFFLINE**</span></span>
-   <span data-ttu-id="1ff51-174">**E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="1ff51-174">**E\_INVALIDARG**</span></span>
-   <span data-ttu-id="1ff51-175">**E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="1ff51-175">**E\_OUTOFMEMORY**</span></span>
-   <span data-ttu-id="1ff51-176">**\_ \_ \_ 使用中的 WS E 位址 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-176">**WS\_E\_ADDRESS\_IN\_USE**</span></span>
-   <span data-ttu-id="1ff51-177">**WS \_ E \_ 位址 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="1ff51-177">**WS\_E\_ADDRESS\_NOT\_AVAILABLE**</span></span>
-   <span data-ttu-id="1ff51-178">**WS \_ E \_ ENDPOINT \_ \_ 拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="1ff51-178">**WS\_E\_ENDPOINT\_ACCESS\_DENIED**</span></span>
-   <span data-ttu-id="1ff51-179">**\_ \_ \_ \_ 不支援 WS E 端點 \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="1ff51-179">**WS\_E\_ENDPOINT\_ACTION\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="1ff51-180">**WS \_ E \_ 端點已 \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="1ff51-180">**WS\_E\_ENDPOINT\_DISCONNECTED**</span></span>
-   <span data-ttu-id="1ff51-181">**WS \_ E \_ 端點 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="1ff51-181">**WS\_E\_ENDPOINT\_FAILURE**</span></span>
-   <span data-ttu-id="1ff51-182">**\_已收到 WS E \_ 端點 \_ 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-182">**WS\_E\_ENDPOINT\_FAULT\_RECEIVED**</span></span>
-   <span data-ttu-id="1ff51-183">**WS \_ E \_ 端點 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="1ff51-183">**WS\_E\_ENDPOINT\_NOT\_AVAILABLE**</span></span>
-   <span data-ttu-id="1ff51-184">**\_ \_ \_ \_ 找不到 WS E 端點**</span><span class="sxs-lookup"><span data-stu-id="1ff51-184">**WS\_E\_ENDPOINT\_NOT\_FOUND**</span></span>
-   <span data-ttu-id="1ff51-185">**WS \_ E \_ 端點 \_ 太 \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="1ff51-185">**WS\_E\_ENDPOINT\_TOO\_BUSY**</span></span>
-   <span data-ttu-id="1ff51-186">**無法連線到 WS \_ E \_ 端點 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-186">**WS\_E\_ENDPOINT\_UNREACHABLE**</span></span>
-   <span data-ttu-id="1ff51-187">**WS \_ E \_ 不正確 \_ 端點 \_ URL**</span><span class="sxs-lookup"><span data-stu-id="1ff51-187">**WS\_E\_INVALID\_ENDPOINT\_URL**</span></span>
-   <span data-ttu-id="1ff51-188">**WS \_ E \_ 不正確 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="1ff51-188">**WS\_E\_INVALID\_FORMAT**</span></span>
-   <span data-ttu-id="1ff51-189">**WS \_ E \_ 不正確作業 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-189">**WS\_E\_INVALID\_OPERATION**</span></span>
-   <span data-ttu-id="1ff51-190">**\_ \_ 不支援 WS \_ E**</span><span class="sxs-lookup"><span data-stu-id="1ff51-190">**WS\_E\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="1ff51-191">**WS \_ E \_ 沒有 \_ 翻譯 \_ 可用**</span><span class="sxs-lookup"><span data-stu-id="1ff51-191">**WS\_E\_NO\_TRANSLATION\_AVAILABLE**</span></span>
-   <span data-ttu-id="1ff51-192">**WS \_ E \_ 數值 \_ 溢位**</span><span class="sxs-lookup"><span data-stu-id="1ff51-192">**WS\_E\_NUMERIC\_OVERFLOW**</span></span>
-   <span data-ttu-id="1ff51-193">**WS \_ E \_ 物件發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-193">**WS\_E\_OBJECT\_FAULTED**</span></span>
-   <span data-ttu-id="1ff51-194">**已 \_ 放棄 WS E \_ 操作 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-194">**WS\_E\_OPERATION\_ABANDONED**</span></span>
-   <span data-ttu-id="1ff51-195">**WS \_ E 作業已 \_ \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="1ff51-195">**WS\_E\_OPERATION\_ABORTED**</span></span>
-   <span data-ttu-id="1ff51-196">**WS \_ E \_ 作業 \_ 超時 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-196">**WS\_E\_OPERATION\_TIMED\_OUT**</span></span>
-   <span data-ttu-id="1ff51-197">**WS \_ E \_ OTHER**</span><span class="sxs-lookup"><span data-stu-id="1ff51-197">**WS\_E\_OTHER**</span></span>
-   <span data-ttu-id="1ff51-198">**\_拒絕 WS E \_ PROXY \_ 存取 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-198">**WS\_E\_PROXY\_ACCESS\_DENIED**</span></span>
-   <span data-ttu-id="1ff51-199">**WS \_ E \_ PROXY \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="1ff51-199">**WS\_E\_PROXY\_FAILURE**</span></span>
-   <span data-ttu-id="1ff51-200">**WS \_ E \_ PROXY \_ 需要 \_ 基本 \_ 身份驗證**</span><span class="sxs-lookup"><span data-stu-id="1ff51-200">**WS\_E\_PROXY\_REQUIRES\_BASIC\_AUTH**</span></span>
-   <span data-ttu-id="1ff51-201">**WS \_ E \_ PROXY \_ 需要 \_ 摘要式 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="1ff51-201">**WS\_E\_PROXY\_REQUIRES\_DIGEST\_AUTH**</span></span>
-   <span data-ttu-id="1ff51-202">**WS \_ E \_ PROXY \_ 需要 \_ 協商 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="1ff51-202">**WS\_E\_PROXY\_REQUIRES\_NEGOTIATE\_AUTH**</span></span>
-   <span data-ttu-id="1ff51-203">**WS \_ E \_ PROXY \_ 需要 \_ NTLM \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="1ff51-203">**WS\_E\_PROXY\_REQUIRES\_NTLM\_AUTH**</span></span>
-   <span data-ttu-id="1ff51-204">**\_超過 WS E \_ 配額 \_**</span><span class="sxs-lookup"><span data-stu-id="1ff51-204">**WS\_E\_QUOTA\_EXCEEDED**</span></span>
-   <span data-ttu-id="1ff51-205">**WS \_ E \_ 安全性 \_ 系統 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="1ff51-205">**WS\_E\_SECURITY\_SYSTEM\_FAILURE**</span></span>
-   <span data-ttu-id="1ff51-206">**WS \_ E \_ 安全性 \_ 權杖已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="1ff51-206">**WS\_E\_SECURITY\_TOKEN\_EXPIRED**</span></span>
-   <span data-ttu-id="1ff51-207">**WS \_ E \_ 安全性 \_ 驗證 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="1ff51-207">**WS\_E\_SECURITY\_VERIFICATION\_FAILURE**</span></span>
-   <span data-ttu-id="1ff51-208">**WS \_ E \_ SERVER \_ 需要 \_ 基本 \_ 身份驗證**</span><span class="sxs-lookup"><span data-stu-id="1ff51-208">**WS\_E\_SERVER\_REQUIRES\_BASIC\_AUTH**</span></span>
-   <span data-ttu-id="1ff51-209">**WS \_ E \_ SERVER \_ 需要 \_ 摘要式 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="1ff51-209">**WS\_E\_SERVER\_REQUIRES\_DIGEST\_AUTH**</span></span>
-   <span data-ttu-id="1ff51-210">**WS \_ E \_ SERVER \_ 需要 \_ 協商 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="1ff51-210">**WS\_E\_SERVER\_REQUIRES\_NEGOTIATE\_AUTH**</span></span>
-   <span data-ttu-id="1ff51-211">**WS \_ E \_ SERVER \_ 需要 \_ NTLM \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="1ff51-211">**WS\_E\_SERVER\_REQUIRES\_NTLM\_AUTH**</span></span>
-   <span data-ttu-id="1ff51-212">**WS \_ S \_ 非同步**</span><span class="sxs-lookup"><span data-stu-id="1ff51-212">**WS\_S\_ASYNC**</span></span>
-   <span data-ttu-id="1ff51-213">**WS \_ S \_ END**</span><span class="sxs-lookup"><span data-stu-id="1ff51-213">**WS\_S\_END**</span></span>

<span data-ttu-id="1ff51-214">下列函數是追蹤的一部分：</span><span class="sxs-lookup"><span data-stu-id="1ff51-214">The following functions are part of tracing:</span></span>

-   [<span data-ttu-id="1ff51-215">**WS \_ ERROR \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="1ff51-215">**WS\_ERROR\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [<span data-ttu-id="1ff51-216">**WS \_ 例外狀況 \_ 代碼**</span><span class="sxs-lookup"><span data-stu-id="1ff51-216">**WS\_EXCEPTION\_CODE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

<span data-ttu-id="1ff51-217">下列控制碼是追蹤的一部分：</span><span class="sxs-lookup"><span data-stu-id="1ff51-217">The following handle is part of tracing:</span></span>

-   [<span data-ttu-id="1ff51-218">WS \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="1ff51-218">WS\_ERROR</span></span>](ws-error.md)

<span data-ttu-id="1ff51-219">下列結構是追蹤的一部分：</span><span class="sxs-lookup"><span data-stu-id="1ff51-219">The following structure is part of tracing:</span></span>

-   [<span data-ttu-id="1ff51-220">**WS \_ ERROR \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="1ff51-220">**WS\_ERROR\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a><span data-ttu-id="1ff51-221">安全性</span><span class="sxs-lookup"><span data-stu-id="1ff51-221">Security</span></span>

<span data-ttu-id="1ff51-222">錯誤物件的使用者應該注意的一些安全性考慮如下：</span><span class="sxs-lookup"><span data-stu-id="1ff51-222">There are a number of security considerations that the user of the error object should be aware of:</span></span>

-   <span data-ttu-id="1ff51-223">錯誤物件可能包含不受信任的資料。</span><span class="sxs-lookup"><span data-stu-id="1ff51-223">The error object may contain untrusted data.</span></span> <span data-ttu-id="1ff51-224">這兩個範例包括： WS \_ 錯誤和錯誤字串，兩者都可以根據未受信任通道所收到的資訊儲存在錯誤物件中。</span><span class="sxs-lookup"><span data-stu-id="1ff51-224">Examples of this are: the WS\_FAULT, and the error strings, both of which can be stored in the error object based on information received over an untrusted channel.</span></span> <span data-ttu-id="1ff51-225">當您檢查 error 物件中的資訊，並根據其值做出決策時，錯誤物件的使用者應該要小心。</span><span class="sxs-lookup"><span data-stu-id="1ff51-225">The user of the error object should be careful when inspecting the information in the error object and making decisions based on its values.</span></span>
-   <span data-ttu-id="1ff51-226">錯誤物件的使用者應該在檢查有關錯誤的資訊之後，呼叫 [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) 。</span><span class="sxs-lookup"><span data-stu-id="1ff51-226">A user of the error object should call [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) after inspecting the information about the error.</span></span> <span data-ttu-id="1ff51-227">如果無法這麼做，可能會導致記憶體累積。</span><span class="sxs-lookup"><span data-stu-id="1ff51-227">Failing to do so can lead to memory accumulation.</span></span>
-   <span data-ttu-id="1ff51-228">使用 \_ ws 錯誤洩漏列舉的 ws 完整錯誤洩漏值時，錯誤物件的使用者應該非常小心 \_ \_ ，因為產生的錯誤可能包含在錯誤記錄過程中累積的私用資訊。 [**\_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)</span><span class="sxs-lookup"><span data-stu-id="1ff51-228">A user of the error object should be very careful when using the WS\_FULL\_FAULT\_DISCLOSURE value of the [**WS\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) enumeration, because the generated fault could contain private information that was accumulated as part of the error recording process.</span></span>

 

 




