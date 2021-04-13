---
description: DVDAdm. DefaultSubpictureLCID 屬性會針對使用者指定的子圖片資料流程預設 LCID 設定或抓取登錄設定。
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: DefaultSubpictureLCID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510357"
---
# <a name="defaultsubpicturelcid-property"></a><span data-ttu-id="1a1c7-103">DefaultSubpictureLCID 屬性</span><span class="sxs-lookup"><span data-stu-id="1a1c7-103">DefaultSubpictureLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="1a1c7-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="1a1c7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1a1c7-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="1a1c7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1a1c7-106">屬性會針對 `DVDAdm.DefaultSubpictureLCID` 使用者指定的子圖片資料流程預設 LCID 設定或抓取登錄設定。</span><span class="sxs-lookup"><span data-stu-id="1a1c7-106">The `DVDAdm.DefaultSubpictureLCID` property sets or retrieves the registry setting for the user-specified default LCID for the subpicture stream.</span></span>

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a><span data-ttu-id="1a1c7-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a1c7-107">Return Value</span></span>

<span data-ttu-id="1a1c7-108">傳回整數值，代表使用者指定的預設子圖片 LCID （儲存在 DVD 應用程式的登錄設定中）。</span><span class="sxs-lookup"><span data-stu-id="1a1c7-108">Returns an Integer value representing the user-specified default subpicture LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="1a1c7-109">此值不一定與 DVD 上所撰寫的預設子圖片資料流程相同。</span><span class="sxs-lookup"><span data-stu-id="1a1c7-109">This value is not necessarily the same as the default subpicture stream as authored on the DVD.</span></span> <span data-ttu-id="1a1c7-110">如需有效的 Lcid 範圍，請參閱 Platform SDK 中的 Win32 檔。</span><span class="sxs-lookup"><span data-stu-id="1a1c7-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a1c7-111">備註</span><span class="sxs-lookup"><span data-stu-id="1a1c7-111">Remarks</span></span>

<span data-ttu-id="1a1c7-112">此屬性是讀取/寫入，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="1a1c7-112">This property is read/write with no default value.</span></span> <span data-ttu-id="1a1c7-113">如果未指定預設子圖片 LCID，MSDVDAdm 物件將會播放標示為光碟上預設資料流程的子圖片串流。</span><span class="sxs-lookup"><span data-stu-id="1a1c7-113">If no default subpicture LCID is specified, the MSDVDAdm object will play the subpicture stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a1c7-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a1c7-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a1c7-115">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="1a1c7-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



