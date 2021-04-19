---
title: 內容容器
description: 內容容器
ms.assetid: bed0293b-4765-4d1b-861c-f0c0a064df5f
keywords:
- Windows Media Player 線上商店、內容容器
- 線上商店、內容容器
- 輸入1個線上商店、內容容器
- Windows Media Player 線上商店、IWMPContentContainer 介面
- 線上商店、IWMPContentContainer 介面
- 輸入1個線上商店、IWMPContentContainer 介面
- Windows Media Player 內容容器
- Windows Media Player，IWMPContentContainer 介面
- 內容容器
- IWMPContentContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801816c3e26920f3d0869190fc1101d6017a524e
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "106969093"
---
# <a name="content-containers"></a><span data-ttu-id="29875-113">內容容器</span><span class="sxs-lookup"><span data-stu-id="29875-113">Content Containers</span></span>

<span data-ttu-id="29875-114">Windows Media Player 使用內容容器來代表訂用帳戶下載或購買交易中的數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="29875-114">Windows Media Player uses content containers to represent digital media content in a subscription download or purchase transaction.</span></span> <span data-ttu-id="29875-115">內容容器會以 **IWMPContentContainer** 介面表示。</span><span class="sxs-lookup"><span data-stu-id="29875-115">A content container is represented by the **IWMPContentContainer** interface.</span></span> <span data-ttu-id="29875-116">內容容器可能包含相關內容的清單，例如專輯或一組不相關的內容專案或 *追蹤*。</span><span class="sxs-lookup"><span data-stu-id="29875-116">A content container might contain a list of related content, such as an album, or a set of unrelated content items, or *tracks*.</span></span> <span data-ttu-id="29875-117">您可以使用 **IWMPContentContainer** 介面來列舉內容容器的追蹤，以及取得每個曲目的價格。您也可以取出內容容器本身的相關資訊，例如容器識別碼、容器中的內容類型，以及容器中的曲目總價格 (這可能與個別曲目的價格總和不同，就像是專輯購買) 一樣。</span><span class="sxs-lookup"><span data-stu-id="29875-117">You can use the **IWMPContentContainer** interface to enumerate the tracks of the content container and retrieve the price of each track. You can also retrieve information about the content container itself, such as the container ID, the type of content in the container, and the total price for the tracks in the container (which might differ from the sum of the prices of the individual tracks, as in the case of an album purchase).</span></span>

<span data-ttu-id="29875-118">為了提供將多個內容容器封裝成單一物件的機制，Windows Media Player 支援 **IWMPContentContainerList** 介面。</span><span class="sxs-lookup"><span data-stu-id="29875-118">To provide a mechanism for packaging multiple content containers into a single object, Windows Media Player supports the **IWMPContentContainerList** interface.</span></span> <span data-ttu-id="29875-119">**IWMPContentContainerList** 提供列舉和取出清單中內容容器的方法。</span><span class="sxs-lookup"><span data-stu-id="29875-119">**IWMPContentContainerList** provides methods to enumerate and retrieve the content containers in the list.</span></span> <span data-ttu-id="29875-120">若要探索內容容器清單是否代表購買或訂閱下載，請呼叫 [IWMPContentContainerList：： GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) 來取得 [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) 值。</span><span class="sxs-lookup"><span data-stu-id="29875-120">To discover whether the content container list represents a purchase or a subscription download, call [IWMPContentContainerList::GetTransactionType](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentcontainerlist-gettransactiontype) to retrieve a [WMPTransactionType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptransactiontype) value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29875-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="29875-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29875-122">**關於類型1線上商店**</span><span class="sxs-lookup"><span data-stu-id="29875-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="29875-123">**IWMPContentContainer 介面**</span><span class="sxs-lookup"><span data-stu-id="29875-123">**IWMPContentContainer Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)
</dt> <dt>

[<span data-ttu-id="29875-124">**IWMPContentContainerList 介面**</span><span class="sxs-lookup"><span data-stu-id="29875-124">**IWMPContentContainerList Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)
</dt> </dl>

 

 




