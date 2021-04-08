---
title: 使用宏進行錯誤處理
description: COM 會定義許多宏，讓您更輕鬆地使用 HRESULT 值。
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683138"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="167e9-103">使用宏進行錯誤處理</span><span class="sxs-lookup"><span data-stu-id="167e9-103">Using Macros for Error Handling</span></span>

<span data-ttu-id="167e9-104">COM 會定義許多宏，讓您更輕鬆地使用 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="167e9-104">COM defines a number of macros that make it easier to work with **HRESULT** values.</span></span>

<span data-ttu-id="167e9-105">下表將說明錯誤處理宏。</span><span class="sxs-lookup"><span data-stu-id="167e9-105">The error handling macros are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="167e9-106">巨集</span><span class="sxs-lookup"><span data-stu-id="167e9-106">Macro</span></span></th>
<th><span data-ttu-id="167e9-107">Description</span><span class="sxs-lookup"><span data-stu-id="167e9-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="167e9-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-108"><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-109">傳回包含<strong>hresult</strong>的嚴重性位、設備碼和錯誤碼的<strong>HRESULT</strong> 。</span><span class="sxs-lookup"><span data-stu-id="167e9-109">Returns an <strong>HRESULT</strong> given the severity bit, facility code, and error code that comprise the <strong>HRESULT</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="167e9-110">針對 S_OK 驗證呼叫 <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> 會帶來效能上的負面影響。</span><span class="sxs-lookup"><span data-stu-id="167e9-110">Calling <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> for S_OK verification carries a performance penalty.</span></span> <span data-ttu-id="167e9-111">您不應該定期使用 <strong>MAKE_HRESULT</strong> 來取得成功的結果。</span><span class="sxs-lookup"><span data-stu-id="167e9-111">You should not routinely use <strong>MAKE_HRESULT</strong> for successful results.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="167e9-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-112"><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-113">傳回 <strong>SCODE</strong> ，指定包含 <strong>SCODE</strong>的嚴重性位、設施碼和錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="167e9-113">Returns an <strong>SCODE</strong> given the severity bit, facility code, and error code that comprise the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="167e9-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-114"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-115">解壓縮 <strong>HRESULT</strong>的錯誤碼部分。</span><span class="sxs-lookup"><span data-stu-id="167e9-115">Extracts the error code portion of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="167e9-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-116"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-117">解壓縮 <strong>HRESULT</strong>的設備程式碼。</span><span class="sxs-lookup"><span data-stu-id="167e9-117">Extracts the facility code of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="167e9-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-118"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-119">解壓縮 <strong>HRESULT</strong>的嚴重性位。</span><span class="sxs-lookup"><span data-stu-id="167e9-119">Extracts the severity bit of the <strong>HRESULT</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="167e9-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-120"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-121">解壓縮 <strong>SCODE</strong>的錯誤碼部分。</span><span class="sxs-lookup"><span data-stu-id="167e9-121">Extracts the error code portion of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="167e9-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-122"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-123">將 <strong>SCODE</strong>的設備碼解壓縮。</span><span class="sxs-lookup"><span data-stu-id="167e9-123">Extracts the facility code of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="167e9-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-124"><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-125">將 <strong>SCODE</strong>的嚴重性欄位解壓縮。</span><span class="sxs-lookup"><span data-stu-id="167e9-125">Extracts the severity field of the <strong>SCODE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="167e9-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>成功</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-126"><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-127">測試 <strong>SCODE</strong> 或 <strong>HRESULT</strong>的嚴重性位;如果嚴重性為零，則傳回 <strong>TRUE</strong> ，如果是，則傳回 <strong>FALSE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="167e9-127">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is zero and <strong>FALSE</strong> if it is one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="167e9-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>失敗</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-128"><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FAILED</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-129">測試 <strong>SCODE</strong> 或 <strong>HRESULT</strong>的嚴重性位;如果嚴重性是1，則傳回 <strong>TRUE</strong> ，如果是零，則傳回 <strong>FALSE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="167e9-129">Tests the severity bit of the <strong>SCODE</strong> or <strong>HRESULT</strong>; returns <strong>TRUE</strong> if the severity is one and <strong>FALSE</strong> if it is zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="167e9-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-130"><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-131">提供任何狀態值的一般測試錯誤。</span><span class="sxs-lookup"><span data-stu-id="167e9-131">Provides a generic test for errors on any status value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="167e9-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-132"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-133">將 <a href="/windows/desktop/Debug/system-error-codes">系統錯誤碼</a> 對應至 <strong>HRESULT</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="167e9-133">Maps a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> to an <strong>HRESULT</strong> value.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="167e9-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span><span class="sxs-lookup"><span data-stu-id="167e9-134"><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a></span></span><br/></td>
<td><span data-ttu-id="167e9-135">將 NT 狀態值對應至 <strong>HRESULT</strong> 值。</span><span class="sxs-lookup"><span data-stu-id="167e9-135">Maps an NT status value to an <strong>HRESULT</strong> value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="167e9-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="167e9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="167e9-137">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="167e9-137">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

