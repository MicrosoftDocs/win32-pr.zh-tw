---
description: 有數種類型的查詢是設計用來查詢資源的狀態。
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: " (Direct3D 9) 的查詢"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845732"
---
# <a name="queries-direct3d-9"></a><span data-ttu-id="2d648-103"> (Direct3D 9) 的查詢</span><span class="sxs-lookup"><span data-stu-id="2d648-103">Queries (Direct3D 9)</span></span>

<span data-ttu-id="2d648-104">有數種類型的查詢是設計用來查詢資源的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-104">There are several types of queries which are designed to query the status of resources.</span></span> <span data-ttu-id="2d648-105">指定資源的狀態包括圖形處理單位 (GPU) 狀態、驅動程式狀態或執行時間狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-105">The status of a given resource includes graphics processing unit (GPU) status, driver status, or runtime status.</span></span> <span data-ttu-id="2d648-106">若要瞭解不同查詢類型之間的差異，您需要瞭解查詢狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-106">To understand the difference between the different query types, you need to understand the query states.</span></span> <span data-ttu-id="2d648-107">下列狀態轉換圖說明每個查詢狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-107">The following state transition diagram explains each of the query states.</span></span>

![顯示查詢狀態之間轉換的圖表](images/queries.png)

<span data-ttu-id="2d648-109">下圖顯示三種狀態，每個都是由圓形所定義。</span><span class="sxs-lookup"><span data-stu-id="2d648-109">The diagram shows three states, each defined by circles.</span></span> <span data-ttu-id="2d648-110">每一條實線都是導致狀態轉換的應用程式驅動事件。</span><span class="sxs-lookup"><span data-stu-id="2d648-110">Each of the solid lines are application-driven events that cause a state transition.</span></span> <span data-ttu-id="2d648-111">虛線是資源驅動事件，會將查詢從發出的狀態切換至已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-111">The dashed line is a resource-driven event that switches a query from the issued state to the signaled state.</span></span> <span data-ttu-id="2d648-112">這些狀態各有不同的用途：</span><span class="sxs-lookup"><span data-stu-id="2d648-112">Each of these states has a different purpose:</span></span>

-   <span data-ttu-id="2d648-113">信號狀態就像是閒置狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-113">The signaled state is like an idle state.</span></span> <span data-ttu-id="2d648-114">已產生查詢物件，並正在等候應用程式發出查詢。</span><span class="sxs-lookup"><span data-stu-id="2d648-114">The query object has been generated and is waiting for the application to issue the query.</span></span> <span data-ttu-id="2d648-115">當查詢完成並轉換回已發出信號的狀態之後，就可以取出查詢的答案。</span><span class="sxs-lookup"><span data-stu-id="2d648-115">Once a query has completed and transitioned back to the signaled state, the answer to the query can be retrieved.</span></span>
-   <span data-ttu-id="2d648-116">建築物狀態就像是查詢的臨時區域。</span><span class="sxs-lookup"><span data-stu-id="2d648-116">The building state is like a staging area for a query.</span></span> <span data-ttu-id="2d648-117">從大樓狀態中， (藉由呼叫 [**D3DISSUE \_ BEGIN**](d3dissue-begin.md)) 來發出查詢，但尚未轉換成已發行的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-117">From the building state, a query has been issued (by calling [**D3DISSUE\_BEGIN**](d3dissue-begin.md)) but has not yet transitioned to the issued state.</span></span> <span data-ttu-id="2d648-118">當應用程式透過呼叫 [**D3DISSUE \_ end**](d3dissue-end.md)) 發出查詢結束 (時，查詢會轉換成已發出的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-118">When an application issues a query end (by calling [**D3DISSUE\_END**](d3dissue-end.md)), the query transitions to the issued state.</span></span>
-   <span data-ttu-id="2d648-119">「已發出」狀態表示所查詢的資源具有查詢的控制權。</span><span class="sxs-lookup"><span data-stu-id="2d648-119">The issued state means that the resource being queried has control of the query.</span></span> <span data-ttu-id="2d648-120">一旦資源完成其工作，資源就會將狀態機器轉換成已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-120">Once the resource finishes its work, the resource transitions the state machine to the signaled state.</span></span> <span data-ttu-id="2d648-121">在「已發出」狀態期間，應用程式必須輪詢以偵測轉換為已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-121">During the issued state, the application must poll to detect the transition to the signaled state.</span></span> <span data-ttu-id="2d648-122">一旦轉換至已發出信號的 [**狀態，則**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 會透過應用程式) 引數傳回查詢結果 (。</span><span class="sxs-lookup"><span data-stu-id="2d648-122">Once the transition to the signaled state occurs, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns the query result (through an argument) to the application.</span></span>

<span data-ttu-id="2d648-123">下表列出可用的查詢類型。</span><span class="sxs-lookup"><span data-stu-id="2d648-123">The following table lists the available query types.</span></span>



| <span data-ttu-id="2d648-124">查詢類型</span><span class="sxs-lookup"><span data-stu-id="2d648-124">Query Type</span></span>        | <span data-ttu-id="2d648-125">問題事件</span><span class="sxs-lookup"><span data-stu-id="2d648-125">Issue Event</span></span>                                                                      | <span data-ttu-id="2d648-126">有其的緩衝區</span><span class="sxs-lookup"><span data-stu-id="2d648-126">GetData buffer</span></span>                                                              | <span data-ttu-id="2d648-127">執行階段</span><span class="sxs-lookup"><span data-stu-id="2d648-127">Runtime</span></span>      | <span data-ttu-id="2d648-128">查詢的隱含開頭</span><span class="sxs-lookup"><span data-stu-id="2d648-128">Implicit beginning of query</span></span>                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| <span data-ttu-id="2d648-129">BANDWIDTHTIMINGS</span><span class="sxs-lookup"><span data-stu-id="2d648-129">BANDWIDTHTIMINGS</span></span>  | <span data-ttu-id="2d648-130">[**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2d648-130">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="2d648-131">**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="2d648-131">**D3DDEVINFO\_D3D9BANDWIDTHTIMINGS**</span></span>](d3ddevinfo-d3d9bandwidthtimings.md) | <span data-ttu-id="2d648-132">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-132">Retail/Debug</span></span> | <span data-ttu-id="2d648-133">N/A</span><span class="sxs-lookup"><span data-stu-id="2d648-133">N/A</span></span>                                              |
| <span data-ttu-id="2d648-134">CACHEUTILIZATION</span><span class="sxs-lookup"><span data-stu-id="2d648-134">CACHEUTILIZATION</span></span>  | <span data-ttu-id="2d648-135">[**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2d648-135">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="2d648-136">**D3DDEVINFO \_ D3D9CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="2d648-136">**D3DDEVINFO\_D3D9CACHEUTILIZATION**</span></span>](d3ddevinfo-d3d9cacheutilization.md) | <span data-ttu-id="2d648-137">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-137">Retail/Debug</span></span> | <span data-ttu-id="2d648-138">N/A</span><span class="sxs-lookup"><span data-stu-id="2d648-138">N/A</span></span>                                              |
| <span data-ttu-id="2d648-139">事件</span><span class="sxs-lookup"><span data-stu-id="2d648-139">EVENT</span></span>             | [<span data-ttu-id="2d648-140">**D3DISSUE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="2d648-140">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="2d648-141">BOOL</span><span class="sxs-lookup"><span data-stu-id="2d648-141">BOOL</span></span>                                                                        | <span data-ttu-id="2d648-142">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-142">Retail/Debug</span></span> | [<span data-ttu-id="2d648-143">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="2d648-143">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="2d648-144">INTERFACETIMINGS</span><span class="sxs-lookup"><span data-stu-id="2d648-144">INTERFACETIMINGS</span></span>  | <span data-ttu-id="2d648-145">[**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2d648-145">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="2d648-146">**D3DDEVINFO \_ D3D9INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="2d648-146">**D3DDEVINFO\_D3D9INTERFACETIMINGS**</span></span>](d3ddevinfo-d3d9interfacetimings.md) | <span data-ttu-id="2d648-147">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-147">Retail/Debug</span></span> | <span data-ttu-id="2d648-148">N/A</span><span class="sxs-lookup"><span data-stu-id="2d648-148">N/A</span></span>                                              |
| <span data-ttu-id="2d648-149">閉塞</span><span class="sxs-lookup"><span data-stu-id="2d648-149">OCCLUSION</span></span>         | <span data-ttu-id="2d648-150">[**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2d648-150">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="2d648-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="2d648-151">DWORD</span></span>                                                                       | <span data-ttu-id="2d648-152">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-152">Retail/Debug</span></span> | <span data-ttu-id="2d648-153">N/A</span><span class="sxs-lookup"><span data-stu-id="2d648-153">N/A</span></span>                                              |
| <span data-ttu-id="2d648-154">PIPELINETIMINGS</span><span class="sxs-lookup"><span data-stu-id="2d648-154">PIPELINETIMINGS</span></span>   | <span data-ttu-id="2d648-155">[**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2d648-155">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="2d648-156">**D3DDEVINFO \_ D3D9PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="2d648-156">**D3DDEVINFO\_D3D9PIPELINETIMINGS**</span></span>](d3ddevinfo-d3d9pipelinetimings.md)   | <span data-ttu-id="2d648-157">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-157">Retail/Debug</span></span> | <span data-ttu-id="2d648-158">N/A</span><span class="sxs-lookup"><span data-stu-id="2d648-158">N/A</span></span>                                              |
| <span data-ttu-id="2d648-159">RESOURCEMANAGER</span><span class="sxs-lookup"><span data-stu-id="2d648-159">RESOURCEMANAGER</span></span>   | [<span data-ttu-id="2d648-160">**D3DISSUE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="2d648-160">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="2d648-161">**D3DDEVINFO \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="2d648-161">**D3DDEVINFO\_ResourceManager**</span></span>](d3ddevinfo-resourcemanager.md)           | <span data-ttu-id="2d648-162">僅限 Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-162">Debug only</span></span>   | [<span data-ttu-id="2d648-163">**目前**</span><span class="sxs-lookup"><span data-stu-id="2d648-163">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="2d648-164">timestamp</span><span class="sxs-lookup"><span data-stu-id="2d648-164">TIMESTAMP</span></span>         | [<span data-ttu-id="2d648-165">**D3DISSUE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="2d648-165">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="2d648-166">UINT64</span><span class="sxs-lookup"><span data-stu-id="2d648-166">UINT64</span></span>                                                                      | <span data-ttu-id="2d648-167">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-167">Retail/Debug</span></span> | <span data-ttu-id="2d648-168">N/A</span><span class="sxs-lookup"><span data-stu-id="2d648-168">N/A</span></span>                                              |
| <span data-ttu-id="2d648-169">TIMESTAMPDISJOINT</span><span class="sxs-lookup"><span data-stu-id="2d648-169">TIMESTAMPDISJOINT</span></span> | <span data-ttu-id="2d648-170">[**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2d648-170">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="2d648-171">BOOL</span><span class="sxs-lookup"><span data-stu-id="2d648-171">BOOL</span></span>                                                                        | <span data-ttu-id="2d648-172">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-172">Retail/Debug</span></span> | <span data-ttu-id="2d648-173">N/A</span><span class="sxs-lookup"><span data-stu-id="2d648-173">N/A</span></span>                                              |
| <span data-ttu-id="2d648-174">TIMESTAMPFREQ</span><span class="sxs-lookup"><span data-stu-id="2d648-174">TIMESTAMPFREQ</span></span>     | [<span data-ttu-id="2d648-175">**D3DISSUE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="2d648-175">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="2d648-176">UINT64</span><span class="sxs-lookup"><span data-stu-id="2d648-176">UINT64</span></span>                                                                      | <span data-ttu-id="2d648-177">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-177">Retail/Debug</span></span> | <span data-ttu-id="2d648-178">N/A</span><span class="sxs-lookup"><span data-stu-id="2d648-178">N/A</span></span>                                              |
| <span data-ttu-id="2d648-179">VCACHE</span><span class="sxs-lookup"><span data-stu-id="2d648-179">VCACHE</span></span>            | [<span data-ttu-id="2d648-180">**D3DISSUE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="2d648-180">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="2d648-181">**D3DDEVINFO \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="2d648-181">**D3DDEVINFO\_VCACHE**</span></span>](d3ddevinfo-vcache.md)                             | <span data-ttu-id="2d648-182">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-182">Retail/Debug</span></span> | [<span data-ttu-id="2d648-183">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="2d648-183">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="2d648-184">VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="2d648-184">VERTEXSTATS</span></span>       | [<span data-ttu-id="2d648-185">**D3DISSUE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="2d648-185">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="2d648-186">**D3DDEVINFO \_ D3DVERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="2d648-186">**D3DDEVINFO\_D3DVERTEXSTATS**</span></span>](d3ddevinfo-d3dvertexstats.md)             | <span data-ttu-id="2d648-187">僅限 Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-187">Debug only</span></span>   | [<span data-ttu-id="2d648-188">**目前**</span><span class="sxs-lookup"><span data-stu-id="2d648-188">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="2d648-189">VERTEXTIMINGS</span><span class="sxs-lookup"><span data-stu-id="2d648-189">VERTEXTIMINGS</span></span>     | <span data-ttu-id="2d648-190">[**D3DISSUE \_BEGIN**](d3dissue-begin.md)， [ **D3DISSUE \_ END**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="2d648-190">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="2d648-191">**D3DDEVINFO \_ D3D9STAGETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="2d648-191">**D3DDEVINFO\_D3D9STAGETIMINGS**</span></span>](d3ddevinfo-d3d9stagetimings.md)         | <span data-ttu-id="2d648-192">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="2d648-192">Retail/Debug</span></span> | <span data-ttu-id="2d648-193">N/A</span><span class="sxs-lookup"><span data-stu-id="2d648-193">N/A</span></span>                                              |



 

<span data-ttu-id="2d648-194">有些查詢需要 begin 和 end 事件，有些則只需要 end 事件。</span><span class="sxs-lookup"><span data-stu-id="2d648-194">Some of the queries require a begin and end event, while others only require an end event.</span></span> <span data-ttu-id="2d648-195">當另一個隱含事件發生時，只需要結束事件的查詢就會開始 (此) 表中列出。</span><span class="sxs-lookup"><span data-stu-id="2d648-195">The queries that only require an end event begin when another implicit event occurs (which is listed in the table).</span></span> <span data-ttu-id="2d648-196">所有查詢都會傳回答案，但答案一律 **為 TRUE** 的事件查詢除外。</span><span class="sxs-lookup"><span data-stu-id="2d648-196">All queries return an answer, except the event query whose answer is always **TRUE**.</span></span> <span data-ttu-id="2d648-197">應用程式會使用查詢的狀態或有 [**可能的傳回碼。**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)</span><span class="sxs-lookup"><span data-stu-id="2d648-197">An application uses either the state of the query or the return code of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>

## <a name="create-a-query"></a><span data-ttu-id="2d648-198">建立查詢</span><span class="sxs-lookup"><span data-stu-id="2d648-198">Create a Query</span></span>

<span data-ttu-id="2d648-199">在您建立查詢之前，您可以藉由呼叫 [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) 與 **Null** 指標（如下所示）來檢查執行時間是否支援查詢：</span><span class="sxs-lookup"><span data-stu-id="2d648-199">Before you create a query, you can check to see if the runtime supports queries by calling [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) with a **NULL** pointer like this:</span></span>


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



<span data-ttu-id="2d648-200">如果可以建立查詢，這個方法會傳回成功的程式碼;否則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2d648-200">This method returns a success code if a query can be created; otherwise it returns an error code.</span></span> <span data-ttu-id="2d648-201">[**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)成功之後，您就可以建立如下的查詢物件：</span><span class="sxs-lookup"><span data-stu-id="2d648-201">Once [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) succeeds, you can create a query object like this:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



<span data-ttu-id="2d648-202">如果此呼叫成功，則會建立查詢物件。</span><span class="sxs-lookup"><span data-stu-id="2d648-202">If this call succeeds, a query object is created.</span></span> <span data-ttu-id="2d648-203">此查詢基本上是閒置的信號狀態 (有未初始化的回應) 等候發出。</span><span class="sxs-lookup"><span data-stu-id="2d648-203">The query is essentially idle in the signaled state (with an uninitialized answer) waiting to be issued.</span></span> <span data-ttu-id="2d648-204">當您完成查詢時，請將它當作任何其他介面來釋放。</span><span class="sxs-lookup"><span data-stu-id="2d648-204">When you are finished with the query, release it like any other interface.</span></span>

## <a name="issue-a-query"></a><span data-ttu-id="2d648-205">發出查詢</span><span class="sxs-lookup"><span data-stu-id="2d648-205">Issue a Query</span></span>

<span data-ttu-id="2d648-206">應用程式會藉由發出查詢來變更查詢狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-206">An application changes a query state by issuing a query.</span></span> <span data-ttu-id="2d648-207">以下是發出查詢的範例：</span><span class="sxs-lookup"><span data-stu-id="2d648-207">Here is an example of issuing a query:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



<span data-ttu-id="2d648-208">發出信號狀態的查詢會在發出時轉換如下：</span><span class="sxs-lookup"><span data-stu-id="2d648-208">A query in the signaled state will transition like this when issued:</span></span>



| <span data-ttu-id="2d648-209">問題類型</span><span class="sxs-lookup"><span data-stu-id="2d648-209">Issue Type</span></span>                                | <span data-ttu-id="2d648-210">查詢會轉換至。</span><span class="sxs-lookup"><span data-stu-id="2d648-210">Query Transitions to the .</span></span> <span data-ttu-id="2d648-211">.</span><span class="sxs-lookup"><span data-stu-id="2d648-211">.</span></span> <span data-ttu-id="2d648-212">.</span><span class="sxs-lookup"><span data-stu-id="2d648-212">.</span></span> |
|-------------------------------------------|--------------------------------|
| [<span data-ttu-id="2d648-213">**D3DISSUE \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="2d648-213">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="2d648-214">建立狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-214">Building state.</span></span>                |
| [<span data-ttu-id="2d648-215">**D3DISSUE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="2d648-215">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="2d648-216">已發行狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-216">Issued state.</span></span>                  |



 

<span data-ttu-id="2d648-217">發出時，建立狀態的查詢會如下所示轉換：</span><span class="sxs-lookup"><span data-stu-id="2d648-217">A query in the building state will transition like this when issued:</span></span>



| <span data-ttu-id="2d648-218">問題類型</span><span class="sxs-lookup"><span data-stu-id="2d648-218">Issue Type</span></span>                                | <span data-ttu-id="2d648-219">查詢會轉換至。</span><span class="sxs-lookup"><span data-stu-id="2d648-219">Query Transitions to the .</span></span> <span data-ttu-id="2d648-220">.</span><span class="sxs-lookup"><span data-stu-id="2d648-220">.</span></span> <span data-ttu-id="2d648-221">.</span><span class="sxs-lookup"><span data-stu-id="2d648-221">.</span></span>                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="2d648-222">**D3DISSUE \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="2d648-222">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="2d648-223"> (沒有任何轉換，則會維持在大樓狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-223">(No transition, stays in the building state.</span></span> <span data-ttu-id="2d648-224">重新開機查詢括弧。 ) </span><span class="sxs-lookup"><span data-stu-id="2d648-224">Restarts the query bracket.)</span></span> |
| [<span data-ttu-id="2d648-225">**D3DISSUE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="2d648-225">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="2d648-226">已發行狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-226">Issued state.</span></span>                                                             |



 

<span data-ttu-id="2d648-227">發出時，發出狀態的查詢會如下所示轉換：</span><span class="sxs-lookup"><span data-stu-id="2d648-227">A query in the issued state will transition like this when issued:</span></span>



| <span data-ttu-id="2d648-228">問題類型</span><span class="sxs-lookup"><span data-stu-id="2d648-228">Issue Type</span></span>                                | <span data-ttu-id="2d648-229">查詢會轉換至。</span><span class="sxs-lookup"><span data-stu-id="2d648-229">Query Transitions to the .</span></span> <span data-ttu-id="2d648-230">.</span><span class="sxs-lookup"><span data-stu-id="2d648-230">.</span></span> <span data-ttu-id="2d648-231">.</span><span class="sxs-lookup"><span data-stu-id="2d648-231">.</span></span>                    |
|-------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="2d648-232">**D3DISSUE \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="2d648-232">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="2d648-233">建立狀態並重新啟動查詢括弧。</span><span class="sxs-lookup"><span data-stu-id="2d648-233">Building state and restarts the query bracket.</span></span>    |
| [<span data-ttu-id="2d648-234">**D3DISSUE \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="2d648-234">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="2d648-235">放棄常設查詢之後發出的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-235">Issued state after abandoning the existing query.</span></span> |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a><span data-ttu-id="2d648-236">檢查查詢狀態並取得查詢的答案</span><span class="sxs-lookup"><span data-stu-id="2d648-236">Check the Query State and Get the Answer to the Query</span></span>

<span data-ttu-id="2d648-237">[](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)有兩個專案：</span><span class="sxs-lookup"><span data-stu-id="2d648-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) does two things:</span></span>

1.  <span data-ttu-id="2d648-238">傳回傳回碼中的查詢狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-238">Returns the query state in the return code.</span></span>
2.  <span data-ttu-id="2d648-239">傳回 *.pdata* 中的查詢答案。</span><span class="sxs-lookup"><span data-stu-id="2d648-239">Returns the answer to the query in *pData*.</span></span>

<span data-ttu-id="2d648-240">從三個查詢狀態中的每一個，以下是有 [**數量的傳回**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 碼：</span><span class="sxs-lookup"><span data-stu-id="2d648-240">From each of the three query states, here are the [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) return codes:</span></span>



| <span data-ttu-id="2d648-241">查詢狀態</span><span class="sxs-lookup"><span data-stu-id="2d648-241">Query State</span></span> | <span data-ttu-id="2d648-242">有其傳回碼</span><span class="sxs-lookup"><span data-stu-id="2d648-242">GetData return code</span></span> |
|-------------|---------------------|
| <span data-ttu-id="2d648-243">暗示</span><span class="sxs-lookup"><span data-stu-id="2d648-243">Signaled</span></span>    | <span data-ttu-id="2d648-244">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="2d648-244">S\_OK</span></span>               |
| <span data-ttu-id="2d648-245">建置</span><span class="sxs-lookup"><span data-stu-id="2d648-245">Building</span></span>    | <span data-ttu-id="2d648-246">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2d648-246">Error code</span></span>          |
| <span data-ttu-id="2d648-247">已發出</span><span class="sxs-lookup"><span data-stu-id="2d648-247">Issued</span></span>      | <span data-ttu-id="2d648-248">S \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="2d648-248">S\_FALSE</span></span>            |



 

<span data-ttu-id="2d648-249">例如，當查詢處於「已發行」 [**狀態，而**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 查詢的答案無法使用時，[操作] 會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="2d648-249">For example, when a query is in the issued state and the answer to the query is not available, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns S\_FALSE.</span></span> <span data-ttu-id="2d648-250">當資源完成其工作，且應用程式已發出查詢結束時，資源會將查詢轉換為已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-250">When the resource finishes its work and the application has issued a query end, the resource transitions the query to the signaled state.</span></span> <span data-ttu-id="2d648-251">從信號的狀態中 **，「** 操作」 \_ 會傳回「確定」，表示查詢的答案也會在 *.pdata* 中傳回。</span><span class="sxs-lookup"><span data-stu-id="2d648-251">From the signaled state, **GetData** returns S\_OK which means that the answer to the query is also returned in *pData*.</span></span> <span data-ttu-id="2d648-252">例如，以下是傳回轉譯順序中所繪製之圖元數目的事件順序：</span><span class="sxs-lookup"><span data-stu-id="2d648-252">For instance, here is the sequence of events to return the number of pixels drawn in a render sequence:</span></span>

-   <span data-ttu-id="2d648-253">建立查詢。</span><span class="sxs-lookup"><span data-stu-id="2d648-253">Create the query.</span></span>
-   <span data-ttu-id="2d648-254">發出開始事件。</span><span class="sxs-lookup"><span data-stu-id="2d648-254">Issue a begin event.</span></span>
-   <span data-ttu-id="2d648-255">繪製一些東西。</span><span class="sxs-lookup"><span data-stu-id="2d648-255">Draw something.</span></span>
-   <span data-ttu-id="2d648-256">發出結束事件。</span><span class="sxs-lookup"><span data-stu-id="2d648-256">Issue an end event.</span></span>

<span data-ttu-id="2d648-257">以下是對應的程式碼序列：</span><span class="sxs-lookup"><span data-stu-id="2d648-257">The following is the corresponding sequence of code:</span></span>


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="2d648-258">這幾行程式碼會執行幾項作業：</span><span class="sxs-lookup"><span data-stu-id="2d648-258">These lines of code do several things:</span></span>

-   <span data-ttu-id="2d648-259">呼叫 [**，**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 以傳回繪製的圖元數。</span><span class="sxs-lookup"><span data-stu-id="2d648-259">Call [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to return the number of pixels drawn.</span></span>
-   <span data-ttu-id="2d648-260">指定 [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md) ，讓資源能夠將查詢轉換為已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-260">Specify [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md) to enable the resource to transition the query to the signaled state.</span></span>
-   <span data-ttu-id="2d648-261">藉 [**由從迴圈**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 呼叫 [已建立] 來輪詢查詢資源。</span><span class="sxs-lookup"><span data-stu-id="2d648-261">Poll the query resource by calling [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) from a loop.</span></span> <span data-ttu-id="2d648-262">**只要操作** 單位 \_ 傳回 FALSE，這表示資源尚未傳回答案。</span><span class="sxs-lookup"><span data-stu-id="2d648-262">As long as **GetData** returns S\_FALSE, this means the resource has not returned the answer yet.</span></span>

<span data-ttu-id="2d648-263">[確定 [**] 的傳回值基本上會**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 告知您該查詢的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-263">The return value of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) essentially tells you in what state the query is.</span></span> <span data-ttu-id="2d648-264">可能的值為 \_ [確定]、[ \_ FALSE] 和 [錯誤]。</span><span class="sxs-lookup"><span data-stu-id="2d648-264">Possible values are S\_OK, S\_FALSE, and an error.</span></span> <span data-ttu-id="2d648-265">請勿在處於建立狀態的 **查詢上呼叫** [操作]。</span><span class="sxs-lookup"><span data-stu-id="2d648-265">Do not call **GetData** on a query that is in the building state.</span></span>

-   <span data-ttu-id="2d648-266">S \_ OK 表示資源 (GPU 或驅動程式，或執行時間) 已完成。</span><span class="sxs-lookup"><span data-stu-id="2d648-266">S\_OK means the resource (GPU or driver, or runtime) is finished.</span></span> <span data-ttu-id="2d648-267">此查詢會返回信號狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-267">The query is returning to the signaled state.</span></span> <span data-ttu-id="2d648-268">如果有任何) 是由 [**操作者傳回，就**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)會 (答案。</span><span class="sxs-lookup"><span data-stu-id="2d648-268">The answer (if any) is being returned by [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>
-   <span data-ttu-id="2d648-269">\_FALSE 表示資源 (GPU 或驅動程式，或執行時間) 無法傳回答案。</span><span class="sxs-lookup"><span data-stu-id="2d648-269">S\_FALSE means the resource (GPU or driver, or runtime) cannot return an answer yet.</span></span> <span data-ttu-id="2d648-270">這可能是因為 GPU 未完成或尚未看過工作。</span><span class="sxs-lookup"><span data-stu-id="2d648-270">This could be because the GPU is not finished or has not seen the work yet.</span></span>
-   <span data-ttu-id="2d648-271">錯誤表示查詢產生了無法復原的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2d648-271">An error means that the query has generated an error from which it cannot recover.</span></span> <span data-ttu-id="2d648-272">如果裝置在查詢期間遺失，就可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="2d648-272">This could be the case if the device is lost during a query.</span></span> <span data-ttu-id="2d648-273">一旦查詢產生的錯誤 (不是 \_ FALSE) ，就必須重新建立查詢，這會從已發出信號的狀態重新開機查詢順序。</span><span class="sxs-lookup"><span data-stu-id="2d648-273">Once a query has generated an error (other than S\_FALSE), the query must be recreated which will restart the query sequence from the signaled state.</span></span>

<span data-ttu-id="2d648-274">除了指定 [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md)（這會提供最新的資訊）之外，您還可以提供零，如果查詢處於「已發行」狀態，這會是較輕量的檢查。</span><span class="sxs-lookup"><span data-stu-id="2d648-274">Instead of specifying [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md), which provides more up-to-date information, you could supply zero which is a more light-weight check if the query is in the issued state.</span></span> <span data-ttu-id="2d648-275">提供零 [**會導致無法**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 排清命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2d648-275">Supplying zero will cause [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to not flush the command buffer.</span></span> <span data-ttu-id="2d648-276">基於這個理由，請務必小心避免 infinate 迴圈 **(如需** 詳細資料，請參閱 [) ]。</span><span class="sxs-lookup"><span data-stu-id="2d648-276">For this reason, care must be taken to avoid infinate loops (see **GetData** for details).</span></span> <span data-ttu-id="2d648-277">由於執行時間會在命令緩衝區中排入佇列，所以 D3DGETDATA 排清是將命令緩衝區排到驅動程式 (的機制，因此也是 GPU; 請參閱 [ (direct3d 9) ) 中正確分析 DIRECT3D API 呼叫](accurately-profiling-direct3d-api-calls.md)。 **\_**</span><span class="sxs-lookup"><span data-stu-id="2d648-277">Since the runtime queues up work in the command buffer, **D3DGETDATA\_FLUSH** is a mechanism for flushing the command buffer to the driver (and hence the GPU; see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="2d648-278">在命令緩衝區排清期間，查詢可能會轉換成已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="2d648-278">During the command buffer flush, a query may transition to the signaled state.</span></span>

## <a name="example-an-event-query"></a><span data-ttu-id="2d648-279">範例：事件查詢</span><span class="sxs-lookup"><span data-stu-id="2d648-279">Example: An Event Query</span></span>

<span data-ttu-id="2d648-280">事件查詢不支援 begin 事件。</span><span class="sxs-lookup"><span data-stu-id="2d648-280">An event query does not support a begin event.</span></span>

-   <span data-ttu-id="2d648-281">建立查詢。</span><span class="sxs-lookup"><span data-stu-id="2d648-281">Create the query.</span></span>
-   <span data-ttu-id="2d648-282">發出結束事件。</span><span class="sxs-lookup"><span data-stu-id="2d648-282">Issue an end event.</span></span>
-   <span data-ttu-id="2d648-283">輪詢直到 GPU 閒置為止。</span><span class="sxs-lookup"><span data-stu-id="2d648-283">Poll until the GPU is idle.</span></span>
-   <span data-ttu-id="2d648-284">發出結束事件。</span><span class="sxs-lookup"><span data-stu-id="2d648-284">Issue an end event.</span></span>


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="2d648-285">這是事件查詢用來分析應用程式開發介面 (API) 呼叫的命令順序 (請參閱 [ (direct3d 9) ) 中正確分析 DIRECT3D API 呼叫 ](accurately-profiling-direct3d-api-calls.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d648-285">This is the sequence of commands an event query uses to profile application programming interface (API) calls (see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="2d648-286">此順序會使用標記來協助控制命令緩衝區中的工作量。</span><span class="sxs-lookup"><span data-stu-id="2d648-286">This sequence uses markers to help control the amount of work in the command buffer.</span></span>

<span data-ttu-id="2d648-287">請注意，應用程式應該特別注意與清除命令緩衝區相關聯的大型成本，因為這會導致作業系統切換至核心模式，因此會造成相當大的效能影響。</span><span class="sxs-lookup"><span data-stu-id="2d648-287">Note that applications should pay special attention to the large cost associated with flushing the command buffer because this causes the operating system to switch into kernel mode, thus incurring a sizeable performance penalty.</span></span> <span data-ttu-id="2d648-288">應用程式也應該注意，藉由等候查詢完成來浪費 CPU 週期。</span><span class="sxs-lookup"><span data-stu-id="2d648-288">Applications should also be aware of wasting CPU cycles by waiting for queries to complete.</span></span>

<span data-ttu-id="2d648-289">查詢是在轉譯期間用來提升效能的優化。</span><span class="sxs-lookup"><span data-stu-id="2d648-289">Queries are an optimization to be used during rendering to increase performance.</span></span> <span data-ttu-id="2d648-290">因此，花時間等候查詢完成並不會有説明。</span><span class="sxs-lookup"><span data-stu-id="2d648-290">Therefore, it is not beneficial to spend time waiting for a query to finish.</span></span> <span data-ttu-id="2d648-291">如果發出查詢，而且應用程式在檢查這些結果時尚未準備好這些結果，則優化的嘗試不會成功，且轉譯應正常地繼續進行。</span><span class="sxs-lookup"><span data-stu-id="2d648-291">If a query is issued and if the results are not yet ready by the time the application checks for them, the attempt at optimizing did not succeed and rendering should continue as normal.</span></span>

<span data-ttu-id="2d648-292">此範例的典型範例是在遮蔽的剔除期間。</span><span class="sxs-lookup"><span data-stu-id="2d648-292">The classic example of this is during Occlusion Culling.</span></span> <span data-ttu-id="2d648-293">使用查詢的應用程式不會使用上述 **while** 迴圈，而是會執行遮蔽的剔除，以查看查詢是否在需要結果時完成。</span><span class="sxs-lookup"><span data-stu-id="2d648-293">Instead of the **while** loop above, an application using queries can implement occlusion culling to check to see if a query had finished by the time it needs the result.</span></span> <span data-ttu-id="2d648-294">如果查詢尚未完成，請在最糟的情況下繼續 (，) 就像是針對進行測試的物件不是 pixels occluded 一樣 (也就是可見) 並加以呈現。</span><span class="sxs-lookup"><span data-stu-id="2d648-294">If the query has not finished, continue (as a worst-case scenario) as if the object being tested against is not occluded (i.e. it is visible) and render it.</span></span> <span data-ttu-id="2d648-295">程式碼看起來會如下所示。</span><span class="sxs-lookup"><span data-stu-id="2d648-295">The code would look similar to the following.</span></span>


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a><span data-ttu-id="2d648-296">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d648-296">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d648-297">Advanced 主題</span><span class="sxs-lookup"><span data-stu-id="2d648-297">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
