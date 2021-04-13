---
description: IUpdateSearcher 介面會定義下列屬性。
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: IUpdateSearcher 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/11/2021
ms.locfileid: "104322583"
---
# <a name="iupdatesearcher-properties"></a><span data-ttu-id="48636-103">IUpdateSearcher 屬性</span><span class="sxs-lookup"><span data-stu-id="48636-103">IUpdateSearcher Properties</span></span>

<span data-ttu-id="48636-104">[**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="48636-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following properties.</span></span>



| <span data-ttu-id="48636-105">屬性</span><span class="sxs-lookup"><span data-stu-id="48636-105">Property</span></span>                                                                                           | <span data-ttu-id="48636-106">描述</span><span class="sxs-lookup"><span data-stu-id="48636-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48636-107">**CanAutomaticallyUpgradeService**</span><span class="sxs-lookup"><span data-stu-id="48636-107">**CanAutomaticallyUpgradeService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | <span data-ttu-id="48636-108">取得和設定布林值，這個值會指出未來對 [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) 和 [**搜尋**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) 方法的呼叫是否會導致自動升級為 WINDOWS UPDATE 代理程式 (WUA) 。</span><span class="sxs-lookup"><span data-stu-id="48636-108">Gets and sets a Boolean value that indicates whether future calls to the [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) and [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) methods result in an automatic upgrade to Windows Update Agent (WUA).</span></span> |
| [<span data-ttu-id="48636-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="48636-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | <span data-ttu-id="48636-110">識別目前的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="48636-110">Identifies the current client application.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="48636-111">**IncludePotentiallySupersededUpdates**</span><span class="sxs-lookup"><span data-stu-id="48636-111">**IncludePotentiallySupersededUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | <span data-ttu-id="48636-112">取得和設定布林值，這個值會指出搜尋結果是否包含在搜尋結果中由其他更新所取代的更新。</span><span class="sxs-lookup"><span data-stu-id="48636-112">Gets and sets a Boolean value that indicates whether the search results include updates that are superseded by other updates in the search results.</span></span>                                                                                          |
| [<span data-ttu-id="48636-113">**線上**</span><span class="sxs-lookup"><span data-stu-id="48636-113">**Online**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | <span data-ttu-id="48636-114">取得和設定布林值，指出 [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) 是否上線以搜尋更新。</span><span class="sxs-lookup"><span data-stu-id="48636-114">Gets and sets a Boolean value that indicates whether the [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) goes online to search for updates.</span></span>                                                                                                        |
| [<span data-ttu-id="48636-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="48636-115">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | <span data-ttu-id="48636-116">取得和設定網站，以搜尋要搜尋的網站不是 Windows Update 網站。</span><span class="sxs-lookup"><span data-stu-id="48636-116">Gets and sets a site to search when the site to search is not a Windows Update site.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="48636-117">**Serverselection.sqlpolicy**</span><span class="sxs-lookup"><span data-stu-id="48636-117">**ServerSelection**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | <span data-ttu-id="48636-118">取得和設定 [**serverselection.sqlpolicy**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) 值，指出要搜尋更新的伺服器。</span><span class="sxs-lookup"><span data-stu-id="48636-118">Gets and sets a [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) value that indicates the server to search for updates.</span></span>                                                                                                                            |




 

 

 



