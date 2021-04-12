---
description: MSDVDAdm 物件
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: MSDVDAdm 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193d5e46837c576c61b8bf1704ec967c1b6fc246
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108484"
---
# <a name="msdvdadm-object"></a><span data-ttu-id="ca741-103">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="ca741-103">MSDVDAdm Object</span></span>

> [!Note]  
> <span data-ttu-id="ca741-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="ca741-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ca741-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ca741-105">It may be altered or unavailable in subsequent versions.</span></span>

 

> [!Note]  
> <span data-ttu-id="ca741-106">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="ca741-106">This API is deprecated.</span></span> <span data-ttu-id="ca741-107">如需有關在 DirectShow 播放和流覽 DVD 的詳細資訊，請參閱 [Dvd 應用程式](dvd-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="ca741-107">For information about DVD playback and navigation in DirectShow, see [DVD Applications](dvd-applications.md).</span></span>

 

<span data-ttu-id="ca741-108">`MSDVDAdm`"Administration" 物件的方法和屬性可讓腳本應用程式在 Microsoft® Windows® registry 中修改其預設設定。</span><span class="sxs-lookup"><span data-stu-id="ca741-108">The methods and properties of the `MSDVDAdm` "administration" object enable a scripting application to modify its default settings in the Microsoft® Windows® registry.</span></span> <span data-ttu-id="ca741-109">登錄是所有 Windows 系統上的資料庫，應用程式可以在這些系統上儲存本身的相關資訊，以便在初始化時或在執行時間時使用。</span><span class="sxs-lookup"><span data-stu-id="ca741-109">The registry is a database on all Windows systems where applications can store information about themselves to be used on initialization or during run time.</span></span>

<span data-ttu-id="ca741-110">大部分的方法和屬性都不會設定或抓取 [MSWebDVD](mswebdvd-object.md) 物件本身中的目前值。</span><span class="sxs-lookup"><span data-stu-id="ca741-110">Most of these methods and properties do not set or retrieve the current values in the [MSWebDVD](mswebdvd-object.md) object itself.</span></span> <span data-ttu-id="ca741-111">例如，這表示當您呼叫 **GetParentalLevel** 時，傳回的值不是目前儲存在物件中的父層級。</span><span class="sxs-lookup"><span data-stu-id="ca741-111">This means, for example, that when you call **GetParentalLevel** the returned value is not the current parental level stored in the object.</span></span> <span data-ttu-id="ca741-112">相反地，它是儲存在登錄中的預設家長儲存層級。</span><span class="sxs-lookup"><span data-stu-id="ca741-112">Rather, it is the default parental level stored in the registry.</span></span> <span data-ttu-id="ca741-113">若要取得目前的父層級，請呼叫 **MSWebDVD** 方法 [**GetPlayerParentalLevel**](getplayerparentallevel-method.md)。</span><span class="sxs-lookup"><span data-stu-id="ca741-113">To get the current parental level, call the **MSWebDVD** method [**GetPlayerParentalLevel**](getplayerparentallevel-method.md).</span></span> <span data-ttu-id="ca741-114">呼叫 [**SaveParentalLevel**](saveparentallevel-method.md) 只會將新的預設家長存取層級寫入登錄;您仍然需要呼叫 **MSWebDVD** 方法 [**SelectParentalLevel**](selectparentallevel-method.md) ，讓變更立即生效于 **MSWebDVD** 物件中。</span><span class="sxs-lookup"><span data-stu-id="ca741-114">Calling [**SaveParentalLevel**](saveparentallevel-method.md) simply writes a new default parental access level to the registry; you still need to call the **MSWebDVD** method [**SelectParentalLevel**](selectparentallevel-method.md) to make the change take effect immediately in the **MSWebDVD** object.</span></span> <span data-ttu-id="ca741-115">預設的地區設定識別碼 (LCID) 方法的運作方式類似。</span><span class="sxs-lookup"><span data-stu-id="ca741-115">The default locale identifier (LCID) methods work in a similar way.</span></span>

<span data-ttu-id="ca741-116">另一方面， [**BookmarkOnStop**](bookmarkonstop-property.md) 和 [**BookmarkOnClose**](bookmarkonclose-property.md) 方法會立即生效，因為 **MSWebDVD** 物件會在使用者停止播放或關閉應用程式時，而不是在初始化期間檢查這些設定。</span><span class="sxs-lookup"><span data-stu-id="ca741-116">On the other hand, the [**BookmarkOnStop**](bookmarkonstop-property.md) and [**BookmarkOnClose**](bookmarkonclose-property.md) methods take effect immediately because the **MSWebDVD** object checks these settings just before the user stops playback or closes the application, rather than during initialization.</span></span>

<span data-ttu-id="ca741-117">您可以 `MSDVDAdm` 透過 **MSWebDVD** 的 **DVDAdm** 屬性存取物件。</span><span class="sxs-lookup"><span data-stu-id="ca741-117">You access the `MSDVDAdm` object through the **DVDAdm** property of **MSWebDVD**.</span></span> <span data-ttu-id="ca741-118">比方說，如果 **MSWebDVD** 物件名為 "DVD"，請呼叫 **ChangePassword** ，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="ca741-118">So, for example, if the **MSWebDVD** object is named "DVD," call **ChangePassword** as shown in the following code example.</span></span>


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



<span data-ttu-id="ca741-119">**方法和屬性**</span><span class="sxs-lookup"><span data-stu-id="ca741-119">**Methods and Properties**</span></span>

<span data-ttu-id="ca741-120">下表列出 MSDVDAdm 物件方法和屬性所公開的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="ca741-120">The following table lists the methods and properties exposed by the MSDVDAdm object methods and properties.</span></span>



| <span data-ttu-id="ca741-121">方法</span><span class="sxs-lookup"><span data-stu-id="ca741-121">Method</span></span>                                                          | <span data-ttu-id="ca741-122">描述</span><span class="sxs-lookup"><span data-stu-id="ca741-122">Description</span></span>                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca741-123">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="ca741-123">**ChangePassword**</span></span>](changepassword-method.md)                 | <span data-ttu-id="ca741-124">在登錄中儲存新的應用程式密碼。</span><span class="sxs-lookup"><span data-stu-id="ca741-124">Saves a new application password in the registry.</span></span>                                                                                                                                |
| [<span data-ttu-id="ca741-125">**SaveParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="ca741-125">**SaveParentalLevel**</span></span>](saveparentallevel-method.md)           | <span data-ttu-id="ca741-126">將新的預設家長監護儲存至登錄。</span><span class="sxs-lookup"><span data-stu-id="ca741-126">Saves a new default parental level to the registry.</span></span>                                                                                                                              |
| [<span data-ttu-id="ca741-127">**SaveParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="ca741-127">**SaveParentalCountry**</span></span>](saveparentalcountry-method.md)       | <span data-ttu-id="ca741-128">將應用程式的新家長/區域儲存至登錄。</span><span class="sxs-lookup"><span data-stu-id="ca741-128">Saves the application's new parental country/region to the registry.</span></span>                                                                                                             |
| [<span data-ttu-id="ca741-129">**ConfirmPassword**</span><span class="sxs-lookup"><span data-stu-id="ca741-129">**ConfirmPassword**</span></span>](confirmpassword-method.md)               | <span data-ttu-id="ca741-130">測試指定的密碼是否符合先前儲存的密碼。</span><span class="sxs-lookup"><span data-stu-id="ca741-130">Tests whether the specified password matches the previously saved password.</span></span>                                                                                                      |
| [<span data-ttu-id="ca741-131">**GetParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="ca741-131">**GetParentalLevel**</span></span>](getparentallevel-method.md)             | <span data-ttu-id="ca741-132">抓取上次儲存至登錄的父層級。</span><span class="sxs-lookup"><span data-stu-id="ca741-132">Retrieves the parental level that was last saved to the registry.</span></span>                                                                                                                |
| [<span data-ttu-id="ca741-133">**GetParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="ca741-133">**GetParentalCountry**</span></span>](getparentalcountry-method.md)         | <span data-ttu-id="ca741-134">抓取上次儲存至登錄的家長監護/區域。</span><span class="sxs-lookup"><span data-stu-id="ca741-134">Retrieves the parental country/region that was last saved to the registry.</span></span>                                                                                                       |
| [<span data-ttu-id="ca741-135">**RestoreScreenSaver**</span><span class="sxs-lookup"><span data-stu-id="ca741-135">**RestoreScreenSaver**</span></span>](restorescreensaver-method.md)         | <span data-ttu-id="ca741-136">還原系統螢幕保護裝置設定。</span><span class="sxs-lookup"><span data-stu-id="ca741-136">Restores the system screen saver settings.</span></span>                                                                                                                                       |
| <span data-ttu-id="ca741-137">屬性</span><span class="sxs-lookup"><span data-stu-id="ca741-137">Property</span></span>                                                        | <span data-ttu-id="ca741-138">描述</span><span class="sxs-lookup"><span data-stu-id="ca741-138">Description</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="ca741-139">**DisableScreenSaver**</span><span class="sxs-lookup"><span data-stu-id="ca741-139">**DisableScreenSaver**</span></span>](disablescreensaver-property.md)       | <span data-ttu-id="ca741-140">開啟或關閉系統螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="ca741-140">Turns the system screen saver on or off.</span></span>                                                                                                                                         |
| [<span data-ttu-id="ca741-141">**DefaultAudioLCID**</span><span class="sxs-lookup"><span data-stu-id="ca741-141">**DefaultAudioLCID**</span></span>](defaultaudiolcid-property.md)           | <span data-ttu-id="ca741-142">為音訊資料流程設定或抓取使用者指定之預設 LCID 的登錄設定。</span><span class="sxs-lookup"><span data-stu-id="ca741-142">Sets or retrieves the registry setting for the user-specified default LCID for the audio stream.</span></span>                                                                                 |
| [<span data-ttu-id="ca741-143">**DefaultSubpictureLCID**</span><span class="sxs-lookup"><span data-stu-id="ca741-143">**DefaultSubpictureLCID**</span></span>](defaultsubpicturelcid-property.md) | <span data-ttu-id="ca741-144">針對使用者指定的子圖片資料流程預設 LCID 設定或抓取登錄設定。</span><span class="sxs-lookup"><span data-stu-id="ca741-144">Sets or retrieves the registry setting for the user-specified default LCID for the subpicture stream.</span></span>                                                                            |
| [<span data-ttu-id="ca741-145">**DefaultMenuLCID**</span><span class="sxs-lookup"><span data-stu-id="ca741-145">**DefaultMenuLCID**</span></span>](defaultmenulcid-property.md)             | <span data-ttu-id="ca741-146">設定或抓取使用者為功能表指定之預設 LCID 的登錄設定。</span><span class="sxs-lookup"><span data-stu-id="ca741-146">Sets or retrieves the registry setting for the user-specified default LCID for menus.</span></span>                                                                                            |
| [<span data-ttu-id="ca741-147">**BookmarkOnStop**</span><span class="sxs-lookup"><span data-stu-id="ca741-147">**BookmarkOnStop**</span></span>](bookmarkonstop-property.md)               | <span data-ttu-id="ca741-148">設定或抓取值，告知 MSDVDAdm 物件是否要在使用者按一下 [ **停止** ] 按鈕時，自動儲存目前位置和設定的書簽。</span><span class="sxs-lookup"><span data-stu-id="ca741-148">Sets or retrieves a value that tells the MSDVDAdm object whether to automatically save a bookmark of the current location and settings when the user clicks the **Stop** button.</span></span> |
| [<span data-ttu-id="ca741-149">**BookmarkOnClose**</span><span class="sxs-lookup"><span data-stu-id="ca741-149">**BookmarkOnClose**</span></span>](bookmarkonclose-property.md)             | <span data-ttu-id="ca741-150">設定或抓取值，告知 MSDVDAdm 物件是否要在使用者關閉應用程式時，自動儲存目前位置和設定的書簽。</span><span class="sxs-lookup"><span data-stu-id="ca741-150">Sets or retrieves a value that tells the MSDVDAdm object whether to automatically save a bookmark of the current location and settings when the user closes the application.</span></span>     |



 

 

 



