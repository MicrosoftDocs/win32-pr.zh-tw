---
title: 回呼同步處理
description: 回呼同步處理
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106978586"
---
# <a name="callback-synchronization"></a><span data-ttu-id="51014-103">回呼同步處理</span><span class="sxs-lookup"><span data-stu-id="51014-103">Callback Synchronization</span></span>

<span data-ttu-id="51014-104">非同步 [WININET API](/windows/desktop/WinInet/portal) (用於最常見的通訊協定) 讓回呼機制和呼叫應用程式的同步處理成為用戶端的練習。</span><span class="sxs-lookup"><span data-stu-id="51014-104">The asynchronous [WinInet API](/windows/desktop/WinInet/portal) (used for the most common protocols) leaves the synchronization of the callback mechanism and the calling application as an exercise for the client.</span></span> <span data-ttu-id="51014-105">這是故意的，因為它允許最大程度的彈性。</span><span class="sxs-lookup"><span data-stu-id="51014-105">This is intentional because it allows the greatest degree of flexibility.</span></span> <span data-ttu-id="51014-106">預設的通訊協定和 URL 的標記執行會執行這種同步處理，並保證單一執行緒和執行緒應用程式永遠不需要處理無限制執行緒的爭用。</span><span class="sxs-lookup"><span data-stu-id="51014-106">The default protocols and the URL moniker implementation perform this synchronization and guarantee that single-threaded and apartment-threaded applications never have to deal with free-thread-style contention.</span></span> <span data-ttu-id="51014-107">也就是說，用戶端的 [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) 和 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) 介面只會在其適當的執行緒上呼叫。</span><span class="sxs-lookup"><span data-stu-id="51014-107">That is, the client's [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) and [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) interfaces are called only on their proper threads.</span></span> <span data-ttu-id="51014-108">這項功能對於 URL mMoniker 的使用者而言是透明的，只要呼叫 [**IMoniker：： BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) 和 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) 的每個執行緒都有訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="51014-108">This feature is transparent to the user of the URL mMoniker as long each thread that calls [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) and [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) has a message queue.</span></span>

<span data-ttu-id="51014-109">非同步「標記」規格需要更精確地控制下載的優先順序與管理，而不是 WinSock 或 WinInet 所允許的。</span><span class="sxs-lookup"><span data-stu-id="51014-109">The asynchronous moniker specification requires more precise control over the prioritization and management of downloads than is allowed for by either WinSock or WinInet.</span></span> <span data-ttu-id="51014-110">因此，URL 標記會針對任何指定的呼叫端執行緒管理所有下載，並使用 (作為其同步處理的一部分，) 以 [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) 規格為基礎的優先順序配置。</span><span class="sxs-lookup"><span data-stu-id="51014-110">Accordingly, a URL moniker manages all the downloads for any given caller's thread, using (as part of its synchronization) a priority scheme based on the [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) specification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51014-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="51014-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51014-112">URL 的名字</span><span class="sxs-lookup"><span data-stu-id="51014-112">URL Monikers</span></span>](url-monikers.md)
</dt> </dl>

 

 