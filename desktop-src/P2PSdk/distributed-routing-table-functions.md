---
description: 分散式路由表 (DRT) API 會利用下列功能。
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: 分散式路由表函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977918"
---
# <a name="distributed-routing-table-functions"></a><span data-ttu-id="a9d64-103">分散式路由表函數</span><span class="sxs-lookup"><span data-stu-id="a9d64-103">Distributed Routing Table Functions</span></span>

<span data-ttu-id="a9d64-104">分散式路由表 (DRT) API 會利用下列功能。</span><span class="sxs-lookup"><span data-stu-id="a9d64-104">The Distributed Routing Table (DRT) API utilizes the following functions.</span></span>

## <a name="lifetime-management-functions"></a><span data-ttu-id="a9d64-105">存留期管理函數</span><span class="sxs-lookup"><span data-stu-id="a9d64-105">Lifetime Management Functions</span></span>



| <span data-ttu-id="a9d64-106">函式</span><span class="sxs-lookup"><span data-stu-id="a9d64-106">Function</span></span>                                           | <span data-ttu-id="a9d64-107">描述</span><span class="sxs-lookup"><span data-stu-id="a9d64-107">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9d64-108">**DrtOpen**</span><span class="sxs-lookup"><span data-stu-id="a9d64-108">**DrtOpen**</span></span>](/windows/desktop/api/drt/nf-drt-drtopen)                         | <span data-ttu-id="a9d64-109">使用 [**DRT \_ 設定**](/windows/desktop/api/drt/ns-drt-drt_settings) 結構所指定的準則建立本機的 DRT 實例。</span><span class="sxs-lookup"><span data-stu-id="a9d64-109">Creates a local DRT instance using criteria specified by the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>  |
| [<span data-ttu-id="a9d64-110">**DrtClose**</span><span class="sxs-lookup"><span data-stu-id="a9d64-110">**DrtClose**</span></span>](/windows/desktop/api/drt/nf-drt-drtclose)                       | <span data-ttu-id="a9d64-111">關閉並移除 DRT 的本機實例。</span><span class="sxs-lookup"><span data-stu-id="a9d64-111">Closes and removes the local instance of the DRT.</span></span>                                                              |
| [<span data-ttu-id="a9d64-112">**DrtGetEventData**</span><span class="sxs-lookup"><span data-stu-id="a9d64-112">**DrtGetEventData**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | <span data-ttu-id="a9d64-113">抓取與訊號事件相關聯的事件資料。</span><span class="sxs-lookup"><span data-stu-id="a9d64-113">Retrieves event data associated with a signaled event.</span></span>                                                         |
| [<span data-ttu-id="a9d64-114">**DrtGetEventDataSize**</span><span class="sxs-lookup"><span data-stu-id="a9d64-114">**DrtGetEventDataSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | <span data-ttu-id="a9d64-115">傳回與訊號事件相關聯之 [**DRT \_ 事件 \_ 資料**](/windows/desktop/api/drt/ns-drt-drt_event_data) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="a9d64-115">Returns the size of the [**DRT\_EVENT\_DATA**](/windows/desktop/api/drt/ns-drt-drt_event_data) structure associated with a signaled event.</span></span> |



 

## <a name="module-management-functions"></a><span data-ttu-id="a9d64-116">模組管理函式</span><span class="sxs-lookup"><span data-stu-id="a9d64-116">Module Management Functions</span></span>



| <span data-ttu-id="a9d64-117">函式</span><span class="sxs-lookup"><span data-stu-id="a9d64-117">Function</span></span>                                                                           | <span data-ttu-id="a9d64-118">描述</span><span class="sxs-lookup"><span data-stu-id="a9d64-118">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9d64-119">**DrtCreatePnrpBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="a9d64-119">**DrtCreatePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | <span data-ttu-id="a9d64-120">根據 PNRP 通訊協定建立啟動程式解析程式。</span><span class="sxs-lookup"><span data-stu-id="a9d64-120">Creates a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="a9d64-121">**DrtDeletePnrpBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="a9d64-121">**DrtDeletePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | <span data-ttu-id="a9d64-122">根據 PNRP 通訊協定刪除啟動程式解析程式。</span><span class="sxs-lookup"><span data-stu-id="a9d64-122">Deletes a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="a9d64-123">**DrtCreateDnsBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="a9d64-123">**DrtCreateDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | <span data-ttu-id="a9d64-124">建立啟動載入器提供者，此提供者會依名稱連接已知的主機。</span><span class="sxs-lookup"><span data-stu-id="a9d64-124">Creates a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="a9d64-125">**DrtDeleteDnsBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="a9d64-125">**DrtDeleteDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | <span data-ttu-id="a9d64-126">刪除啟動載入器提供者，此提供者會依名稱連接已知的主機。</span><span class="sxs-lookup"><span data-stu-id="a9d64-126">Deletes a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="a9d64-127">**DrtCreateIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="a9d64-127">**DrtCreateIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | <span data-ttu-id="a9d64-128">建立以 IPv6 UDP 通訊協定為基礎的傳輸。</span><span class="sxs-lookup"><span data-stu-id="a9d64-128">Creates a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="a9d64-129">**DrtDeleteIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="a9d64-129">**DrtDeleteIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | <span data-ttu-id="a9d64-130">刪除以 IPv6 UDP 通訊協定為基礎的傳輸。</span><span class="sxs-lookup"><span data-stu-id="a9d64-130">Deletes a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="a9d64-131">**DrtCreateDerivedKeySecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="a9d64-131">**DrtCreateDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | <span data-ttu-id="a9d64-132">建立適用于 DRT 的衍生金鑰安全性提供者。</span><span class="sxs-lookup"><span data-stu-id="a9d64-132">Creates a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="a9d64-133">**DrtCreateDerivedKey**</span><span class="sxs-lookup"><span data-stu-id="a9d64-133">**DrtCreateDerivedKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | <span data-ttu-id="a9d64-134">建立當 DRT 使用衍生金鑰安全性提供者時，可供 [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) 使用的金鑰。</span><span class="sxs-lookup"><span data-stu-id="a9d64-134">Creates a key that can be utilized by [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) when the DRT is using a derived key security provider.</span></span> |
| [<span data-ttu-id="a9d64-135">**DrtDeleteDerivedKeySecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="a9d64-135">**DrtDeleteDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | <span data-ttu-id="a9d64-136">刪除適用于 DRT 的衍生金鑰安全性提供者。</span><span class="sxs-lookup"><span data-stu-id="a9d64-136">Deletes a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="a9d64-137">**DrtCreateNullSecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="a9d64-137">**DrtCreateNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | <span data-ttu-id="a9d64-138">建立 null 安全性提供者。</span><span class="sxs-lookup"><span data-stu-id="a9d64-138">Creates a null security provider.</span></span> <span data-ttu-id="a9d64-139">此安全性提供者不需要節點來驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="a9d64-139">This security provider does not require nodes to authenticate keys.</span></span>                                 |
| [<span data-ttu-id="a9d64-140">**DrtDeleteNullSecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="a9d64-140">**DrtDeleteNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | <span data-ttu-id="a9d64-141">刪除 null 安全性提供者。</span><span class="sxs-lookup"><span data-stu-id="a9d64-141">Deletes a null security provider.</span></span>                                                                                                     |



 

## <a name="registration-functions"></a><span data-ttu-id="a9d64-142">註冊函式</span><span class="sxs-lookup"><span data-stu-id="a9d64-142">Registration Functions</span></span>



| <span data-ttu-id="a9d64-143">函式</span><span class="sxs-lookup"><span data-stu-id="a9d64-143">Function</span></span>                                     | <span data-ttu-id="a9d64-144">描述</span><span class="sxs-lookup"><span data-stu-id="a9d64-144">Description</span></span>                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="a9d64-145">**DrtRegisterKey**</span><span class="sxs-lookup"><span data-stu-id="a9d64-145">**DrtRegisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | <span data-ttu-id="a9d64-146">在 DRT 中註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="a9d64-146">Registers a key in the DRT.</span></span>                                    |
| [<span data-ttu-id="a9d64-147">**DrtUpdateKey**</span><span class="sxs-lookup"><span data-stu-id="a9d64-147">**DrtUpdateKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | <span data-ttu-id="a9d64-148">更新與已註冊金鑰相關聯的應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="a9d64-148">Updates the application data associated with a registered key.</span></span> |
| [<span data-ttu-id="a9d64-149">**DrtUnregisterKey**</span><span class="sxs-lookup"><span data-stu-id="a9d64-149">**DrtUnregisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | <span data-ttu-id="a9d64-150">從 DRT 取消註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="a9d64-150">Deregisters a key from the DRT.</span></span>                                |



 

## <a name="search-functions"></a><span data-ttu-id="a9d64-151">搜尋函數</span><span class="sxs-lookup"><span data-stu-id="a9d64-151">Search Functions</span></span>



| <span data-ttu-id="a9d64-152">函式</span><span class="sxs-lookup"><span data-stu-id="a9d64-152">Function</span></span>                                                 | <span data-ttu-id="a9d64-153">描述</span><span class="sxs-lookup"><span data-stu-id="a9d64-153">Description</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9d64-154">**DrtStartSearch**</span><span class="sxs-lookup"><span data-stu-id="a9d64-154">**DrtStartSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | <span data-ttu-id="a9d64-155">使用在 [**drt \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info) 結構中指定的準則，在 drt 中搜尋金鑰。</span><span class="sxs-lookup"><span data-stu-id="a9d64-155">Searches the DRT for a key using criteria specified in the [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span>                                                                                                      |
| [<span data-ttu-id="a9d64-156">**DrtContinueSearch**</span><span class="sxs-lookup"><span data-stu-id="a9d64-156">**DrtContinueSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | <span data-ttu-id="a9d64-157">繼續在 \_ \_ \_ drt 中搜尋金鑰的 drt 搜尋傳回路徑。</span><span class="sxs-lookup"><span data-stu-id="a9d64-157">Continues a DRT\_SEARCH\_RETURN\_PATH search for a key in the DRT.</span></span> <span data-ttu-id="a9d64-158">只有在相關聯的 [**DRT \_ 搜尋 \_ 資訊**](/windows/desktop/api/drt/ns-drt-drt_search_info)結構中將 **FIterative** 旗標設為 **TRUE** 時，才會使用此函數。</span><span class="sxs-lookup"><span data-stu-id="a9d64-158">This function is used only when the **fIterative** flag is set to **TRUE** in the associated [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span> |
| [<span data-ttu-id="a9d64-159">**DrtGetSearchResult**</span><span class="sxs-lookup"><span data-stu-id="a9d64-159">**DrtGetSearchResult**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | <span data-ttu-id="a9d64-160">抓取 (s) 的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="a9d64-160">Retrieves the search result(s).</span></span>                                                                                                                                                                                         |
| [<span data-ttu-id="a9d64-161">**DrtGetSearchResultSize**</span><span class="sxs-lookup"><span data-stu-id="a9d64-161">**DrtGetSearchResultSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | <span data-ttu-id="a9d64-162">傳回下一個可用搜尋結果的大小。</span><span class="sxs-lookup"><span data-stu-id="a9d64-162">Returns the size of the next available search result.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="a9d64-163">**DrtGetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="a9d64-163">**DrtGetSearchPath**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | <span data-ttu-id="a9d64-164">傳回在搜尋作業期間連接的節點清單。</span><span class="sxs-lookup"><span data-stu-id="a9d64-164">Returns a list of nodes contacted during the search operation.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="a9d64-165">**DrtGetSearchPathSize**</span><span class="sxs-lookup"><span data-stu-id="a9d64-165">**DrtGetSearchPathSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | <span data-ttu-id="a9d64-166">傳回搜尋路徑的大小，這表示搜尋作業中使用的節點數目。</span><span class="sxs-lookup"><span data-stu-id="a9d64-166">Returns the size of the search path, which represents the number of nodes utilized in the search operation.</span></span>                                                                                                             |
| [<span data-ttu-id="a9d64-167">**DrtEndSearch**</span><span class="sxs-lookup"><span data-stu-id="a9d64-167">**DrtEndSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | <span data-ttu-id="a9d64-168">取消搜尋在 DRT 中的金鑰，如此一來，透過 [**DRT \_ 搜尋 \_ 結果**](/windows/desktop/api/drt/ns-drt-drt_search_result) 傳回結果的結果就會停止。</span><span class="sxs-lookup"><span data-stu-id="a9d64-168">Cancels a search for a key in a DRT, and as a result, the return of results via [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) is stopped.</span></span> <span data-ttu-id="a9d64-169">您可以在發出搜尋之後的任何時間點呼叫此 API。</span><span class="sxs-lookup"><span data-stu-id="a9d64-169">This API can be called at any point after a search is issued.</span></span>              |



 

## <a name="instance-name-functions"></a><span data-ttu-id="a9d64-170">實例名稱函數</span><span class="sxs-lookup"><span data-stu-id="a9d64-170">Instance Name Functions</span></span>



| <span data-ttu-id="a9d64-171">函式</span><span class="sxs-lookup"><span data-stu-id="a9d64-171">Function</span></span>                                                 | <span data-ttu-id="a9d64-172">描述</span><span class="sxs-lookup"><span data-stu-id="a9d64-172">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="a9d64-173">**DrtGetInstanceName**</span><span class="sxs-lookup"><span data-stu-id="a9d64-173">**DrtGetInstanceName**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | <span data-ttu-id="a9d64-174">取得與 DRT 實例相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9d64-174">Gets the name associated with a DRT instance.</span></span>                    |
| [<span data-ttu-id="a9d64-175">**DrtGetInstanceNameSize**</span><span class="sxs-lookup"><span data-stu-id="a9d64-175">**DrtGetInstanceNameSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | <span data-ttu-id="a9d64-176">傳回分散式路由表實例名稱的大小。</span><span class="sxs-lookup"><span data-stu-id="a9d64-176">Returns the size of the Distributed Routing Table instance name.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a9d64-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9d64-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9d64-178">分散式路由表列舉</span><span class="sxs-lookup"><span data-stu-id="a9d64-178">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="a9d64-179">分散式路由表結構</span><span class="sxs-lookup"><span data-stu-id="a9d64-179">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="a9d64-180">分散式路由資料表 API 參考</span><span class="sxs-lookup"><span data-stu-id="a9d64-180">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



