---
description: SaveBookmark 方法會儲存目前的光碟位置和 MSWebDVD 物件的狀態，讓使用者可以在稍後返回相同的位置。
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: 'SaveBookmark 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999194"
---
# <a name="savebookmark-method"></a><span data-ttu-id="abebf-103">SaveBookmark 方法</span><span class="sxs-lookup"><span data-stu-id="abebf-103">SaveBookmark Method</span></span>

> [!Note]  
> <span data-ttu-id="abebf-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="abebf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="abebf-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="abebf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="abebf-106">`SaveBookmark`方法會儲存目前的光碟位置和 **MSWebDVD** 物件的狀態，讓使用者可以在稍後返回相同的位置。</span><span class="sxs-lookup"><span data-stu-id="abebf-106">The `SaveBookmark` method saves the current disc position and state of the **MSWebDVD** object so the user can return to the same place later.</span></span>

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a><span data-ttu-id="abebf-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="abebf-107">Return Value</span></span>

<span data-ttu-id="abebf-108">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="abebf-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="abebf-109">備註</span><span class="sxs-lookup"><span data-stu-id="abebf-109">Remarks</span></span>

<span data-ttu-id="abebf-110">書簽是 DVD 導覽器目前狀態的快照。</span><span class="sxs-lookup"><span data-stu-id="abebf-110">A bookmark is a snapshot of the DVD Navigator's current state.</span></span> <span data-ttu-id="abebf-111">這包括在光碟上播放的位置，以及選取的音訊和 subpictures 串流等資訊。</span><span class="sxs-lookup"><span data-stu-id="abebf-111">This includes information such as where it is playing on the disc, and which audio and subpictures streams are selected.</span></span> <span data-ttu-id="abebf-112">藉由儲存書簽，使用者就可以關閉應用程式、關閉電腦，然後稍後再返回，以繼續在離開的地方繼續觀看光碟，並與之前一樣的設定。</span><span class="sxs-lookup"><span data-stu-id="abebf-112">By saving a bookmark, the user can close the application, shut down the computer, and come back later to continue viewing the disc right where he or she left off, with all settings just as they were before.</span></span> <span data-ttu-id="abebf-113">在任何指定的時間都只能儲存一個書簽。</span><span class="sxs-lookup"><span data-stu-id="abebf-113">Only one bookmark can be saved at any given time.</span></span> <span data-ttu-id="abebf-114">當您呼叫時 `SaveBookmark` ，會覆寫舊的書簽。</span><span class="sxs-lookup"><span data-stu-id="abebf-114">When you call `SaveBookmark`, the old bookmark is overwritten.</span></span>

## <a name="requirements"></a><span data-ttu-id="abebf-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="abebf-115">Requirements</span></span>



| <span data-ttu-id="abebf-116">需求</span><span class="sxs-lookup"><span data-stu-id="abebf-116">Requirement</span></span> | <span data-ttu-id="abebf-117">值</span><span class="sxs-lookup"><span data-stu-id="abebf-117">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="abebf-118">標頭</span><span class="sxs-lookup"><span data-stu-id="abebf-118">Header</span></span><br/> | <dl> <span data-ttu-id="abebf-119"><dt>區段。h</dt></span><span class="sxs-lookup"><span data-stu-id="abebf-119"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abebf-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abebf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abebf-121">**RestoreBookmark**</span><span class="sxs-lookup"><span data-stu-id="abebf-121">**RestoreBookmark**</span></span>](restorebookmark-method.md)
</dt> </dl>

 

 




