---
description: DVDAdm. BookmarkOnStop 屬性會設定或抓取值，告知 MSWebDVD 物件是否要在使用者按一下 [停止] 按鈕時，自動儲存目前位置和設定的書簽。
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: BookmarkOnStop 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109537"
---
# <a name="bookmarkonstop-property"></a><span data-ttu-id="7f99a-103">BookmarkOnStop 屬性</span><span class="sxs-lookup"><span data-stu-id="7f99a-103">BookmarkOnStop Property</span></span>

<span data-ttu-id="7f99a-104">`DVDAdm.BookmarkOnStop`屬性會設定或抓取值，告知 MSWebDVD 物件是否要在使用者按一下 [**停止**] 按鈕時，自動儲存目前位置和設定的書簽。</span><span class="sxs-lookup"><span data-stu-id="7f99a-104">The `DVDAdm.BookmarkOnStop` property sets or retrieves a value that tells the MSWebDVD object whether to automatically save a bookmark of the current location and settings when the user clicks the **Stop** button.</span></span>

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a><span data-ttu-id="7f99a-105">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f99a-105">Return Value</span></span>

<span data-ttu-id="7f99a-106">傳回布林值，指出 MSDVDAdm 物件是否會儲存所有 DVD 設定的書簽，包括光碟上的位置、家長監護層和家長監護/區域。</span><span class="sxs-lookup"><span data-stu-id="7f99a-106">Returns a Boolean value indicating whether the MSDVDAdm object will save a bookmark of all DVD settings including position on disc, parental level and parental country/region.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f99a-107">備註</span><span class="sxs-lookup"><span data-stu-id="7f99a-107">Remarks</span></span>

<span data-ttu-id="7f99a-108">這個屬性是讀取/寫入，預設值是 false。</span><span class="sxs-lookup"><span data-stu-id="7f99a-108">This property is read/write with a default value of false.</span></span>

<span data-ttu-id="7f99a-109">書簽只對特定電腦有效。</span><span class="sxs-lookup"><span data-stu-id="7f99a-109">Bookmarks are valid only for a particular machine.</span></span> <span data-ttu-id="7f99a-110">使用者無法儲存書簽，然後將它傳送給其他人，以便在不同的電腦上讀取。</span><span class="sxs-lookup"><span data-stu-id="7f99a-110">A user cannot save a bookmark and then send it to someone else to read on a different machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f99a-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f99a-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f99a-112">**BookmarkOnClose**</span><span class="sxs-lookup"><span data-stu-id="7f99a-112">**BookmarkOnClose**</span></span>](bookmarkonclose-property.md)
</dt> <dt>

[<span data-ttu-id="7f99a-113">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="7f99a-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



