---
description: IUpdateSearcher 介面會定義下列方法。
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: IUpdateSearcher 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462cbd371546743bab836ed1cdc2479e30f13612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991750"
---
# <a name="iupdatesearcher-methods"></a><span data-ttu-id="5ec8e-103">IUpdateSearcher 方法</span><span class="sxs-lookup"><span data-stu-id="5ec8e-103">IUpdateSearcher Methods</span></span>

<span data-ttu-id="5ec8e-104">[**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)介面會定義下列方法。</span><span class="sxs-lookup"><span data-stu-id="5ec8e-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following methods.</span></span>



| <span data-ttu-id="5ec8e-105">方法</span><span class="sxs-lookup"><span data-stu-id="5ec8e-105">Method</span></span>                                                              | <span data-ttu-id="5ec8e-106">描述</span><span class="sxs-lookup"><span data-stu-id="5ec8e-106">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ec8e-107">**BeginSearch**</span><span class="sxs-lookup"><span data-stu-id="5ec8e-107">**BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)                   | <span data-ttu-id="5ec8e-108">開始執行更新的非同步搜尋。</span><span class="sxs-lookup"><span data-stu-id="5ec8e-108">Begins execution of an asynchronous search for updates.</span></span> <span data-ttu-id="5ec8e-109">搜尋會使用目前設定的搜尋選項。</span><span class="sxs-lookup"><span data-stu-id="5ec8e-109">The search uses the search options that are currently configured.</span></span> |
| [<span data-ttu-id="5ec8e-110">**EndSearch**</span><span class="sxs-lookup"><span data-stu-id="5ec8e-110">**EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)                       | <span data-ttu-id="5ec8e-111">完成更新的非同步搜尋。</span><span class="sxs-lookup"><span data-stu-id="5ec8e-111">Completes an asynchronous search for updates.</span></span>                                                                             |
| [<span data-ttu-id="5ec8e-112">**EscapeString**</span><span class="sxs-lookup"><span data-stu-id="5ec8e-112">**EscapeString**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-escapestring)                 | <span data-ttu-id="5ec8e-113">將字串轉換成可在搜尋準則字串中當做常值使用的字串。</span><span class="sxs-lookup"><span data-stu-id="5ec8e-113">Converts a string into a string that can be used as a literal value in a search criteria string.</span></span>                          |
| [<span data-ttu-id="5ec8e-114">**GetTotalHistoryCount**</span><span class="sxs-lookup"><span data-stu-id="5ec8e-114">**GetTotalHistoryCount**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount) | <span data-ttu-id="5ec8e-115">傳回電腦上更新事件的數目。</span><span class="sxs-lookup"><span data-stu-id="5ec8e-115">Returns the number of update events on the computer.</span></span>                                                                      |
| [<span data-ttu-id="5ec8e-116">**QueryHistory**</span><span class="sxs-lookup"><span data-stu-id="5ec8e-116">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-queryhistory)                | <span data-ttu-id="5ec8e-117">以同步方式查詢更新事件歷程記錄的電腦。</span><span class="sxs-lookup"><span data-stu-id="5ec8e-117">Synchronously queries the computer for the history of update events.</span></span>                                                      |
| [<span data-ttu-id="5ec8e-118">**搜尋**</span><span class="sxs-lookup"><span data-stu-id="5ec8e-118">**Search**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search)                             | <span data-ttu-id="5ec8e-119">執行更新的同步搜尋。</span><span class="sxs-lookup"><span data-stu-id="5ec8e-119">Performs a synchronous search for updates.</span></span> <span data-ttu-id="5ec8e-120">搜尋會使用目前設定的搜尋選項。</span><span class="sxs-lookup"><span data-stu-id="5ec8e-120">The search uses the search options that are currently configured.</span></span>              |



 

 

 



