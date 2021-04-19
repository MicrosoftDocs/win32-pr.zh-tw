---
description: 如果沒有任何效能成本，應用程式可能會產生一些有趣的查詢。
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: " (Direct3D 9) 的非同步通知"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972772"
---
# <a name="asynchronous-notification-direct3d-9"></a><span data-ttu-id="c7a9b-103"> (Direct3D 9) 的非同步通知</span><span class="sxs-lookup"><span data-stu-id="c7a9b-103">Asynchronous Notification (Direct3D 9)</span></span>

<span data-ttu-id="c7a9b-104">如果沒有任何效能成本，應用程式可能會產生一些有趣的查詢。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-104">There are number of interesting queries on a driver that an application can make if there is no performance cost.</span></span> <span data-ttu-id="c7a9b-105">在 Direct3D 7 和 Direct3D 8 中，同步查詢機制 GetInfo，適用于統計資料，但未加入任何效能關鍵查詢。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-105">In Direct3D 7 and Direct3D 8, a synchronous query mechanism, GetInfo, worked well for things like statistics, but no performance-critical queries were added.</span></span> <span data-ttu-id="c7a9b-106">另外還有其他專案 (，像是本質上是非同步) 。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-106">There are other things (like fences) that are inherently asynchronous.</span></span> <span data-ttu-id="c7a9b-107">這是一個簡單的 API，可進行同步和非同步查詢。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-107">This is a simple API to make both synchronous and asynchronous queries.</span></span> <span data-ttu-id="c7a9b-108">GetInfo 將在 Direct3D 9 中淘汰。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-108">GetInfo will be retired in Direct3D 9.</span></span>

<span data-ttu-id="c7a9b-109">使用 [**IDirect3DDevice9：： CreateQuery**](/windows/desktop/api)建立查詢。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-109">Create a query using [**IDirect3DDevice9::CreateQuery**](/windows/desktop/api).</span></span> <span data-ttu-id="c7a9b-110">這個方法會採用 D3DQUERYTYPE，它會定義要進行何種類型的查詢，並將指標傳回至 [**IDirect3DQuery9**](/windows/desktop/api) 物件。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-110">This method takes a D3DQUERYTYPE, which defines what kind of query to make and returns a pointer to an [**IDirect3DQuery9**](/windows/desktop/api) object.</span></span> <span data-ttu-id="c7a9b-111">如果查詢類型不受支援，則呼叫會傳回錯誤 D3DERR \_ NOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-111">If the query type is not supported, the call returns an error D3DERR\_NOTAVAILABLE.</span></span> <span data-ttu-id="c7a9b-112">使用查詢物件時，應用程式會使用 [**IDirect3DQuery9：： Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)將查詢提交至執行時間，並使用 [**IDirect3DQuery9：：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)來輪詢查詢狀態。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-112">Using the query object, the application submits the query to the runtime using [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue), and polls the query status using [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="c7a9b-113">如果有可用的查詢結果， \_ 則會傳回 s OK，否則會 \_ 傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-113">If the query result is available, S\_OK is returned; otherwise, S\_FALSE is returned.</span></span> <span data-ttu-id="c7a9b-114">應用程式預期會針對查詢結果傳遞適當大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-114">The application is expected to pass an appropriately sized buffer for the query results.</span></span>

<span data-ttu-id="c7a9b-115">應用程式有一個選項，可讓執行時間使用 D3DGETDATA \_ flush With [**IDirect3DQuery9：：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)來強制將查詢排清至驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-115">The application has an option to force the runtime to flush the query down to the driver by using D3DGETDATA\_FLUSH with [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="c7a9b-116">它會造成清除，強制驅動程式查看查詢。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-116">It causes a flush, forcing the driver to see the query.</span></span> <span data-ttu-id="c7a9b-117">在此情況下， \_ 如果裝置遺失，則會傳回 D3DERR DEVICELOST。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-117">In this case, D3DERR\_DEVICELOST is returned if the device becomes lost.</span></span>

<span data-ttu-id="c7a9b-118">當裝置遺失時，所有查詢都會遺失，應用程式必須重新建立。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-118">All queries are lost when the device is lost, the application has to re-create them.</span></span> <span data-ttu-id="c7a9b-119">如果裝置不支援查詢，且 pQueryID 為 **Null**，則查詢建立將會失敗，並出現 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-119">If the device does not support the query and the pQueryID is **NULL**, the query creation will fail with D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="c7a9b-120">下表摘要說明每個查詢類型的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="c7a9b-120">The following table summaries important information about each query type.</span></span>



| <span data-ttu-id="c7a9b-121">QuertyType</span><span class="sxs-lookup"><span data-stu-id="c7a9b-121">QuertyType</span></span>                    | <span data-ttu-id="c7a9b-122">有效的問題旗標</span><span class="sxs-lookup"><span data-stu-id="c7a9b-122">Valid issue flag</span></span>              | <span data-ttu-id="c7a9b-123">有其的緩衝區</span><span class="sxs-lookup"><span data-stu-id="c7a9b-123">GetData buffer</span></span>              | <span data-ttu-id="c7a9b-124">執行階段</span><span class="sxs-lookup"><span data-stu-id="c7a9b-124">Runtime</span></span>      | <span data-ttu-id="c7a9b-125">查詢的隱含開頭</span><span class="sxs-lookup"><span data-stu-id="c7a9b-125">Implicit beginning of query</span></span> |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| <span data-ttu-id="c7a9b-126">D3DQUERYTYPE \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="c7a9b-126">D3DQUERYTYPE\_VCACHE</span></span>          | <span data-ttu-id="c7a9b-127">D3DISSUE \_ 結束</span><span class="sxs-lookup"><span data-stu-id="c7a9b-127">D3DISSUE\_END</span></span>                 | <span data-ttu-id="c7a9b-128">D3DDEVINFO \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="c7a9b-128">D3DDEVINFO\_VCACHE</span></span>          | <span data-ttu-id="c7a9b-129">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="c7a9b-129">Retail/Debug</span></span> | <span data-ttu-id="c7a9b-130">CreateDevice</span><span class="sxs-lookup"><span data-stu-id="c7a9b-130">CreateDevice</span></span>                |
| <span data-ttu-id="c7a9b-131">D3DQUERYTYPE \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="c7a9b-131">D3DQUERYTYPE\_ResourceManager</span></span> | <span data-ttu-id="c7a9b-132">D3DISSUE \_ 結束</span><span class="sxs-lookup"><span data-stu-id="c7a9b-132">D3DISSUE\_END</span></span>                 | <span data-ttu-id="c7a9b-133">D3DDEVINFO \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="c7a9b-133">D3DDEVINFO\_ResourceManager</span></span> | <span data-ttu-id="c7a9b-134">僅限 Debug</span><span class="sxs-lookup"><span data-stu-id="c7a9b-134">Debug only</span></span>   | <span data-ttu-id="c7a9b-135">存在</span><span class="sxs-lookup"><span data-stu-id="c7a9b-135">Present</span></span>                     |
| <span data-ttu-id="c7a9b-136">D3DQUERYTYPE \_ VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="c7a9b-136">D3DQUERYTYPE\_VERTEXSTATS</span></span>     | <span data-ttu-id="c7a9b-137">D3DISSUE \_ 結束</span><span class="sxs-lookup"><span data-stu-id="c7a9b-137">D3DISSUE\_END</span></span>                 | <span data-ttu-id="c7a9b-138">D3DDEVINFO \_ D3DVERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="c7a9b-138">D3DDEVINFO\_D3DVERTEXSTATS</span></span>  | <span data-ttu-id="c7a9b-139">僅限 Debug</span><span class="sxs-lookup"><span data-stu-id="c7a9b-139">Debug only</span></span>   | <span data-ttu-id="c7a9b-140">存在</span><span class="sxs-lookup"><span data-stu-id="c7a9b-140">Present</span></span>                     |
| <span data-ttu-id="c7a9b-141">D3DQUERYTYPE \_ 事件</span><span class="sxs-lookup"><span data-stu-id="c7a9b-141">D3DQUERYTYPE\_EVENT</span></span>           | <span data-ttu-id="c7a9b-142">D3DISSUE \_ 結束</span><span class="sxs-lookup"><span data-stu-id="c7a9b-142">D3DISSUE\_END</span></span>                 | <span data-ttu-id="c7a9b-143">BOOL</span><span class="sxs-lookup"><span data-stu-id="c7a9b-143">BOOL</span></span>                        | <span data-ttu-id="c7a9b-144">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="c7a9b-144">Retail/Debug</span></span> | <span data-ttu-id="c7a9b-145">CreateDevice</span><span class="sxs-lookup"><span data-stu-id="c7a9b-145">CreateDevice</span></span>                |
| <span data-ttu-id="c7a9b-146">D3DQUERYTYPE \_ 遮蔽</span><span class="sxs-lookup"><span data-stu-id="c7a9b-146">D3DQUERYTYPE\_OCCLUSION</span></span>       | <span data-ttu-id="c7a9b-147">D3DISSUE \_ BEGIN，D3DISSUE \_ END</span><span class="sxs-lookup"><span data-stu-id="c7a9b-147">D3DISSUE\_BEGIN,D3DISSUE\_END</span></span> | <span data-ttu-id="c7a9b-148">DWORD</span><span class="sxs-lookup"><span data-stu-id="c7a9b-148">DWORD</span></span>                       | <span data-ttu-id="c7a9b-149">零售/Debug</span><span class="sxs-lookup"><span data-stu-id="c7a9b-149">Retail/Debug</span></span> | <span data-ttu-id="c7a9b-150">N/A</span><span class="sxs-lookup"><span data-stu-id="c7a9b-150">N/A</span></span>                         |



 

<span data-ttu-id="c7a9b-151">[**IDirect3DQuery9：： Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)的旗標欄位：</span><span class="sxs-lookup"><span data-stu-id="c7a9b-151">Flags field for [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span></span>


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



<span data-ttu-id="c7a9b-152">[**IDirect3DQuery9：：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)的旗標欄位：</span><span class="sxs-lookup"><span data-stu-id="c7a9b-152">Flags field for [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span></span>


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a><span data-ttu-id="c7a9b-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7a9b-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7a9b-154">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="c7a9b-154">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
