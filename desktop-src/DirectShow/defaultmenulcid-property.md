---
description: DVDAdm. DefaultMenuLCID 屬性會設定或抓取使用者為功能表指定之預設 LCID 的登錄設定。
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: DefaultMenuLCID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109617"
---
# <a name="defaultmenulcid-property"></a><span data-ttu-id="eebe4-103">DefaultMenuLCID 屬性</span><span class="sxs-lookup"><span data-stu-id="eebe4-103">DefaultMenuLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="eebe4-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="eebe4-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="eebe4-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="eebe4-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="eebe4-106">`DVDAdm.DefaultMenuLCID`屬性會設定或抓取使用者為功能表指定之預設 LCID 的登錄設定。</span><span class="sxs-lookup"><span data-stu-id="eebe4-106">The `DVDAdm.DefaultMenuLCID` property sets or retrieves the registry setting for the user-specified default LCID for menus.</span></span>

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a><span data-ttu-id="eebe4-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="eebe4-107">Return Value</span></span>

<span data-ttu-id="eebe4-108">傳回整數值，代表儲存在 DVD 應用程式之登錄設定中的 LCID。</span><span class="sxs-lookup"><span data-stu-id="eebe4-108">Returns an Integer value representing the LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="eebe4-109">此值與在 DVD 上撰寫的預設功能表語言不一定相同。</span><span class="sxs-lookup"><span data-stu-id="eebe4-109">This value is not necessarily the same as the default menu language as authored on the DVD.</span></span> <span data-ttu-id="eebe4-110">如需有效的 Lcid 範圍，請參閱 Platform SDK 中的 Win32 檔。</span><span class="sxs-lookup"><span data-stu-id="eebe4-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="eebe4-111">備註</span><span class="sxs-lookup"><span data-stu-id="eebe4-111">Remarks</span></span>

<span data-ttu-id="eebe4-112">此屬性是讀取/寫入，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="eebe4-112">This property is read/write with no default value.</span></span> <span data-ttu-id="eebe4-113">如果未指定預設的功能表 LCID，MSDVDAdm 物件會使用標示為光碟上預設功能表語言的語言。</span><span class="sxs-lookup"><span data-stu-id="eebe4-113">If no default menu LCID is specified, the MSDVDAdm object will use the language that is marked as the default menu language on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="eebe4-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eebe4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eebe4-115">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="eebe4-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



