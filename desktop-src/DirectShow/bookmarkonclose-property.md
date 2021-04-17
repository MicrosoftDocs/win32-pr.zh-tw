---
description: DVDAdm BookmarkOnClose 屬性會設定或抓取值，告知 MSDVDAdm 物件是否要在使用者關閉應用程式時，自動儲存目前位置和設定的書簽。
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: BookmarkOnClose 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfbbfe194a496dba3568b7dfa4d75b97d4ed57c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317747"
---
# <a name="bookmarkonclose-property"></a><span data-ttu-id="86685-103">BookmarkOnClose 屬性</span><span class="sxs-lookup"><span data-stu-id="86685-103">BookmarkOnClose Property</span></span>

> [!Note]  
> <span data-ttu-id="86685-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="86685-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="86685-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="86685-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="86685-106">`DVDAdm.BookmarkOnClose`屬性會設定或抓取值，告知 MSDVDAdm 物件是否要在使用者關閉應用程式時，自動儲存目前位置和設定的書簽。</span><span class="sxs-lookup"><span data-stu-id="86685-106">The `DVDAdm.BookmarkOnClose` property sets or retrieves a value that tells the MSDVDAdm object whether to automatically save a bookmark of the current location and settings when the user closes the application.</span></span>

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a><span data-ttu-id="86685-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="86685-107">Return Value</span></span>

<span data-ttu-id="86685-108">傳回布林值，如果為 true，表示 MSDVDAdm 控制項將會儲存所有 DVD 設定的書簽，包括光碟上的位置、家長監護，以及當使用者關閉 DVD 播放機應用程式時的家長監護/區域。</span><span class="sxs-lookup"><span data-stu-id="86685-108">Returns a Boolean value, which if true, indicates that the MSDVDAdm control will save a bookmark of all DVD settings, including position on disc, parental level, and parental country/region when the user closes the DVD player application.</span></span>

## <a name="remarks"></a><span data-ttu-id="86685-109">備註</span><span class="sxs-lookup"><span data-stu-id="86685-109">Remarks</span></span>

<span data-ttu-id="86685-110">此屬性是讀取/寫入，預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="86685-110">This property is read/write with a default value of true.</span></span>

## <a name="see-also"></a><span data-ttu-id="86685-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86685-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86685-112">**BookmarkOnStop**</span><span class="sxs-lookup"><span data-stu-id="86685-112">**BookmarkOnStop**</span></span>](bookmarkonstop-property.md)
</dt> <dt>

[<span data-ttu-id="86685-113">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="86685-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



