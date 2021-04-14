---
title: WM/WMCollectionGroupID
description: WM/WMCollectionGroupID 屬性包含可識別集合群組的 GUID。
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- WM/WMCollectionGroupID windows Media 格式
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652007933669db4ed7977474858c7089ca0d577f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373144"
---
# <a name="wmwmcollectiongroupid"></a><span data-ttu-id="1d139-104">WM/WMCollectionGroupID</span><span class="sxs-lookup"><span data-stu-id="1d139-104">WM/WMCollectionGroupID</span></span>

<span data-ttu-id="1d139-105">**WM/WMCollectionGroupID** 屬性包含可識別集合群組的 GUID。</span><span class="sxs-lookup"><span data-stu-id="1d139-105">The **WM/WMCollectionGroupID** attribute contains a GUID identifying the collection group.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1d139-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="1d139-106">Global Constant</span></span>

<span data-ttu-id="1d139-107">g \_ wszWMWMCollectionGroupID</span><span class="sxs-lookup"><span data-stu-id="1d139-107">g\_wszWMWMCollectionGroupID</span></span>

## <a name="data-type"></a><span data-ttu-id="1d139-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="1d139-108">Data Type</span></span>

<span data-ttu-id="1d139-109">**WMT \_ 類型 \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="1d139-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="1d139-110">備註</span><span class="sxs-lookup"><span data-stu-id="1d139-110">Remarks</span></span>

<span data-ttu-id="1d139-111">使用三個值（ **wm/WMCollectionGroupID**、 **WM/WMCollectionID** 和 **WM/WMContentID**），以 Windows Media 技術來識別內容。</span><span class="sxs-lookup"><span data-stu-id="1d139-111">Content is identified by Windows Media technologies by using three values: **WM/WMCollectionGroupID**, **WM/WMCollectionID**, and **WM/WMContentID**.</span></span> <span data-ttu-id="1d139-112">這些值會識別內容、其所屬的集合，以及集合所屬的群組。</span><span class="sxs-lookup"><span data-stu-id="1d139-112">These values identify the content, the collection to which it belongs, and the group to which the collection belongs.</span></span> <span data-ttu-id="1d139-113">當抓取內容的中繼資料時，會 Windows Media Player 填入上述三個值。</span><span class="sxs-lookup"><span data-stu-id="1d139-113">All three of these values are populated by Windows Media Player when metadata for the content is retrieved.</span></span> <span data-ttu-id="1d139-114">您可以讓您的應用程式記錄這些值，並使用它們來識別內容，但如果有的話，您就不應該變更它們。</span><span class="sxs-lookup"><span data-stu-id="1d139-114">You can have your application record these values and use them to identify content, but you should not change them if they are present.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d139-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d139-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d139-116">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="1d139-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




