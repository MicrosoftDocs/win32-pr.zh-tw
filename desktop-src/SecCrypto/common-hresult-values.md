---
description: 以下是最常見的 HRESULT 值。 Winerror.h 標頭檔中包含更多的值。
ms.assetid: ce52efc3-92c7-40e4-ac49-0c54049e169f
title: 一般 HRESULT 值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a64d042d9531d026cda548b2a699ed60c0bebd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848664"
---
# <a name="common-hresult-values"></a><span data-ttu-id="8c400-104">一般 HRESULT 值</span><span class="sxs-lookup"><span data-stu-id="8c400-104">Common HRESULT Values</span></span>

<span data-ttu-id="8c400-105">以下是最常見的 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="8c400-105">The following HRESULT values are the most common.</span></span> <span data-ttu-id="8c400-106">Winerror.h 標頭檔中包含更多的值。</span><span class="sxs-lookup"><span data-stu-id="8c400-106">More values are contained in the header file Winerror.h.</span></span>

<span data-ttu-id="8c400-107">以下是依名稱字母順序列出的值。</span><span class="sxs-lookup"><span data-stu-id="8c400-107">Here are the values listed alphabetically by name.</span></span>



| <span data-ttu-id="8c400-108">Name</span><span class="sxs-lookup"><span data-stu-id="8c400-108">Name</span></span>            | <span data-ttu-id="8c400-109">描述</span><span class="sxs-lookup"><span data-stu-id="8c400-109">Description</span></span>                         | <span data-ttu-id="8c400-110">值</span><span class="sxs-lookup"><span data-stu-id="8c400-110">Value</span></span>      |
|-----------------|-------------------------------------|------------|
| <span data-ttu-id="8c400-111">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="8c400-111">S\_OK</span></span>           | <span data-ttu-id="8c400-112">作業已順利完成</span><span class="sxs-lookup"><span data-stu-id="8c400-112">Operation successful</span></span>                | <span data-ttu-id="8c400-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c400-113">0x00000000</span></span> |
| <span data-ttu-id="8c400-114">E \_ 中止</span><span class="sxs-lookup"><span data-stu-id="8c400-114">E\_ABORT</span></span>        | <span data-ttu-id="8c400-115">作業已中止</span><span class="sxs-lookup"><span data-stu-id="8c400-115">Operation aborted</span></span>                   | <span data-ttu-id="8c400-116">0x80004004</span><span class="sxs-lookup"><span data-stu-id="8c400-116">0x80004004</span></span> |
| <span data-ttu-id="8c400-117">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="8c400-117">E\_ACCESSDENIED</span></span> | <span data-ttu-id="8c400-118">一般拒絕存取錯誤</span><span class="sxs-lookup"><span data-stu-id="8c400-118">General access denied error</span></span>         | <span data-ttu-id="8c400-119">0x80070005</span><span class="sxs-lookup"><span data-stu-id="8c400-119">0x80070005</span></span> |
| <span data-ttu-id="8c400-120">E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="8c400-120">E\_FAIL</span></span>         | <span data-ttu-id="8c400-121">未指定的失敗</span><span class="sxs-lookup"><span data-stu-id="8c400-121">Unspecified failure</span></span>                 | <span data-ttu-id="8c400-122">0x80004005</span><span class="sxs-lookup"><span data-stu-id="8c400-122">0x80004005</span></span> |
| <span data-ttu-id="8c400-123">E \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="8c400-123">E\_HANDLE</span></span>       | <span data-ttu-id="8c400-124">不正確控制碼</span><span class="sxs-lookup"><span data-stu-id="8c400-124">Handle that is not valid</span></span>            | <span data-ttu-id="8c400-125">0x80070006</span><span class="sxs-lookup"><span data-stu-id="8c400-125">0x80070006</span></span> |
| <span data-ttu-id="8c400-126">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8c400-126">E\_INVALIDARG</span></span>   | <span data-ttu-id="8c400-127">一或多個引數無效</span><span class="sxs-lookup"><span data-stu-id="8c400-127">One or more arguments are not valid</span></span> | <span data-ttu-id="8c400-128">0x80070057</span><span class="sxs-lookup"><span data-stu-id="8c400-128">0x80070057</span></span> |
| <span data-ttu-id="8c400-129">E \_ NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="8c400-129">E\_NOINTERFACE</span></span>  | <span data-ttu-id="8c400-130">不支援這類介面</span><span class="sxs-lookup"><span data-stu-id="8c400-130">No such interface supported</span></span>         | <span data-ttu-id="8c400-131">0x80004002</span><span class="sxs-lookup"><span data-stu-id="8c400-131">0x80004002</span></span> |
| <span data-ttu-id="8c400-132">E \_ >NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="8c400-132">E\_NOTIMPL</span></span>      | <span data-ttu-id="8c400-133">未實作</span><span class="sxs-lookup"><span data-stu-id="8c400-133">Not implemented</span></span>                     | <span data-ttu-id="8c400-134">0x80004001</span><span class="sxs-lookup"><span data-stu-id="8c400-134">0x80004001</span></span> |
| <span data-ttu-id="8c400-135">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="8c400-135">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="8c400-136">無法配置所需的記憶體</span><span class="sxs-lookup"><span data-stu-id="8c400-136">Failed to allocate necessary memory</span></span> | <span data-ttu-id="8c400-137">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="8c400-137">0x8007000E</span></span> |
| <span data-ttu-id="8c400-138">E \_ 指標</span><span class="sxs-lookup"><span data-stu-id="8c400-138">E\_POINTER</span></span>      | <span data-ttu-id="8c400-139">不正確指標</span><span class="sxs-lookup"><span data-stu-id="8c400-139">Pointer that is not valid</span></span>           | <span data-ttu-id="8c400-140">且顯示0x80004003</span><span class="sxs-lookup"><span data-stu-id="8c400-140">0x80004003</span></span> |
| <span data-ttu-id="8c400-141">E 未 \_ 預期</span><span class="sxs-lookup"><span data-stu-id="8c400-141">E\_UNEXPECTED</span></span>   | <span data-ttu-id="8c400-142">未預期的失敗</span><span class="sxs-lookup"><span data-stu-id="8c400-142">Unexpected failure</span></span>                  | <span data-ttu-id="8c400-143">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="8c400-143">0x8000FFFF</span></span> |



 

<span data-ttu-id="8c400-144">以下是依值排序的數值順序中所列的值。</span><span class="sxs-lookup"><span data-stu-id="8c400-144">Here are the values listed in numeric order by value.</span></span>



| <span data-ttu-id="8c400-145">值</span><span class="sxs-lookup"><span data-stu-id="8c400-145">Value</span></span>      | <span data-ttu-id="8c400-146">名稱</span><span class="sxs-lookup"><span data-stu-id="8c400-146">Name</span></span>            | <span data-ttu-id="8c400-147">描述</span><span class="sxs-lookup"><span data-stu-id="8c400-147">Description</span></span>                         |
|------------|-----------------|-------------------------------------|
| <span data-ttu-id="8c400-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8c400-148">0x00000000</span></span> | <span data-ttu-id="8c400-149">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="8c400-149">S\_OK</span></span>           | <span data-ttu-id="8c400-150">作業已順利完成</span><span class="sxs-lookup"><span data-stu-id="8c400-150">Operation successful</span></span>                |
| <span data-ttu-id="8c400-151">0x80004001</span><span class="sxs-lookup"><span data-stu-id="8c400-151">0x80004001</span></span> | <span data-ttu-id="8c400-152">E \_ >NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="8c400-152">E\_NOTIMPL</span></span>      | <span data-ttu-id="8c400-153">未實作</span><span class="sxs-lookup"><span data-stu-id="8c400-153">Not implemented</span></span>                     |
| <span data-ttu-id="8c400-154">0x80004002</span><span class="sxs-lookup"><span data-stu-id="8c400-154">0x80004002</span></span> | <span data-ttu-id="8c400-155">E \_ NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="8c400-155">E\_NOINTERFACE</span></span>  | <span data-ttu-id="8c400-156">不支援這類介面</span><span class="sxs-lookup"><span data-stu-id="8c400-156">No such interface supported</span></span>         |
| <span data-ttu-id="8c400-157">且顯示0x80004003</span><span class="sxs-lookup"><span data-stu-id="8c400-157">0x80004003</span></span> | <span data-ttu-id="8c400-158">E \_ 指標</span><span class="sxs-lookup"><span data-stu-id="8c400-158">E\_POINTER</span></span>      | <span data-ttu-id="8c400-159">不正確指標</span><span class="sxs-lookup"><span data-stu-id="8c400-159">Pointer that is not valid</span></span>           |
| <span data-ttu-id="8c400-160">0x80004004</span><span class="sxs-lookup"><span data-stu-id="8c400-160">0x80004004</span></span> | <span data-ttu-id="8c400-161">E \_ 中止</span><span class="sxs-lookup"><span data-stu-id="8c400-161">E\_ABORT</span></span>        | <span data-ttu-id="8c400-162">作業已中止</span><span class="sxs-lookup"><span data-stu-id="8c400-162">Operation aborted</span></span>                   |
| <span data-ttu-id="8c400-163">0x80004005</span><span class="sxs-lookup"><span data-stu-id="8c400-163">0x80004005</span></span> | <span data-ttu-id="8c400-164">E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="8c400-164">E\_FAIL</span></span>         | <span data-ttu-id="8c400-165">未指定的失敗</span><span class="sxs-lookup"><span data-stu-id="8c400-165">Unspecified failure</span></span>                 |
| <span data-ttu-id="8c400-166">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="8c400-166">0x8000FFFF</span></span> | <span data-ttu-id="8c400-167">E 未 \_ 預期</span><span class="sxs-lookup"><span data-stu-id="8c400-167">E\_UNEXPECTED</span></span>   | <span data-ttu-id="8c400-168">未預期的失敗</span><span class="sxs-lookup"><span data-stu-id="8c400-168">Unexpected failure</span></span>                  |
| <span data-ttu-id="8c400-169">0x80070005</span><span class="sxs-lookup"><span data-stu-id="8c400-169">0x80070005</span></span> | <span data-ttu-id="8c400-170">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="8c400-170">E\_ACCESSDENIED</span></span> | <span data-ttu-id="8c400-171">一般拒絕存取錯誤</span><span class="sxs-lookup"><span data-stu-id="8c400-171">General access denied error</span></span>         |
| <span data-ttu-id="8c400-172">0x80070006</span><span class="sxs-lookup"><span data-stu-id="8c400-172">0x80070006</span></span> | <span data-ttu-id="8c400-173">E \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="8c400-173">E\_HANDLE</span></span>       | <span data-ttu-id="8c400-174">不正確控制碼</span><span class="sxs-lookup"><span data-stu-id="8c400-174">Handle that is not valid</span></span>            |
| <span data-ttu-id="8c400-175">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="8c400-175">0x8007000E</span></span> | <span data-ttu-id="8c400-176">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="8c400-176">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="8c400-177">無法配置所需的記憶體</span><span class="sxs-lookup"><span data-stu-id="8c400-177">Failed to allocate necessary memory</span></span> |
| <span data-ttu-id="8c400-178">0x80070057</span><span class="sxs-lookup"><span data-stu-id="8c400-178">0x80070057</span></span> | <span data-ttu-id="8c400-179">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8c400-179">E\_INVALIDARG</span></span>   | <span data-ttu-id="8c400-180">一或多個引數無效</span><span class="sxs-lookup"><span data-stu-id="8c400-180">One or more arguments are not valid</span></span> |



 

 

 



