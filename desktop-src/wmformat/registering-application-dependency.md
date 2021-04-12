---
title: " (Windows Media Format 11 SDK) 註冊應用程式相依性"
description: 註冊應用程式相依性
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK，註冊應用程式相依性
- 註冊應用程式相依性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024402"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="b2635-105"> (Windows Media Format 11 SDK) 註冊應用程式相依性</span><span class="sxs-lookup"><span data-stu-id="b2635-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="b2635-106">使用 Windows Media 格式 SDK 或 Windows Media Player SDK 所提供之 Api 的應用程式，會根據這些技術的執行時間元件而定。</span><span class="sxs-lookup"><span data-stu-id="b2635-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="b2635-107">您可以在應用程式設定中註冊應用程式，使其相依于這些元件。</span><span class="sxs-lookup"><span data-stu-id="b2635-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="b2635-108">當您註冊應用程式時，您可以選擇兩個相依性層級的其中一個：封鎖或相依。</span><span class="sxs-lookup"><span data-stu-id="b2635-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="b2635-109">當一個或多個應用程式在其中一個執行時間元件的封鎖相依性註冊時，元件將會被封鎖而無法回復至先前的版本。</span><span class="sxs-lookup"><span data-stu-id="b2635-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="b2635-110">未註冊為封鎖的相依應用程式，則不會封鎖復原。</span><span class="sxs-lookup"><span data-stu-id="b2635-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="b2635-111">相反地，在執行復原之前，系統會提示使用者輸入訊息，指出應用程式相依于元件。</span><span class="sxs-lookup"><span data-stu-id="b2635-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="b2635-112">若要註冊您的應用程式，您必須在登錄中設定用來識別應用程式的值。</span><span class="sxs-lookup"><span data-stu-id="b2635-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="b2635-113">要設定的登錄值取決於您的應用程式相依的元件。</span><span class="sxs-lookup"><span data-stu-id="b2635-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="b2635-114">您也可以為每個相依性設定兩個額外的值，以提供應用程式的額外資訊。</span><span class="sxs-lookup"><span data-stu-id="b2635-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="b2635-115">下列登錄值會用來註冊 Windows Media Format SDK runtime 的相依性：</span><span class="sxs-lookup"><span data-stu-id="b2635-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="b2635-116">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *REF \_ TYPE* \\ App，"*app*"，"*應用程式 \_ 字串*"</span><span class="sxs-lookup"><span data-stu-id="b2635-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="b2635-117">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *REF \_ TYPE* \\ 描述元，"*APP*"，"*REF \_ 描述* 元"</span><span class="sxs-lookup"><span data-stu-id="b2635-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="b2635-118">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *REF \_ TYPE* \\ Version，"*APP*"，"*WMF \_ Version*"</span><span class="sxs-lookup"><span data-stu-id="b2635-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="b2635-119">下列登錄值會用來註冊 Windows Media Player SDK 執行時間的相依性：</span><span class="sxs-lookup"><span data-stu-id="b2635-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="b2635-120">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ *REF \_ TYPE* \\ App，"*app*"，"*應用程式 \_ 字串*"</span><span class="sxs-lookup"><span data-stu-id="b2635-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="b2635-121">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ *REF \_ TYPE* \\ 描述元，"*APP*"，"*REF \_ 描述* 元"</span><span class="sxs-lookup"><span data-stu-id="b2635-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="b2635-122">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ *REF \_ TYPE* \\ Version，"*APP*"，"*WMP \_ version*"</span><span class="sxs-lookup"><span data-stu-id="b2635-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="b2635-123">下列變數會用於上述的登錄值：</span><span class="sxs-lookup"><span data-stu-id="b2635-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="b2635-124">*REF \_ 類型*</span><span class="sxs-lookup"><span data-stu-id="b2635-124">*REF\_TYPE*</span></span>

<span data-ttu-id="b2635-125">取代為封鎖相依性的 BlockingRefCounts，或針對非封鎖相依性使用 DependentRefCounts 取代。</span><span class="sxs-lookup"><span data-stu-id="b2635-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="b2635-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="b2635-126">*APP*</span></span>

<span data-ttu-id="b2635-127">應用程式的名稱或簡短描述項。</span><span class="sxs-lookup"><span data-stu-id="b2635-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="b2635-128">此字串不會用於使用者顯示的訊息。</span><span class="sxs-lookup"><span data-stu-id="b2635-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="b2635-129">此值是與每個執行時間元件相關聯的三個登錄值所使用的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2635-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="b2635-130">*應用程式 \_ 字串*</span><span class="sxs-lookup"><span data-stu-id="b2635-130">*APP\_STRING*</span></span>

<span data-ttu-id="b2635-131">應用程式的描述項。</span><span class="sxs-lookup"><span data-stu-id="b2635-131">Descriptor of your application.</span></span> <span data-ttu-id="b2635-132">這個字串可用於顯示給使用者的訊息。</span><span class="sxs-lookup"><span data-stu-id="b2635-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="b2635-133">*參考 \_ 描述元*</span><span class="sxs-lookup"><span data-stu-id="b2635-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="b2635-134">應用程式如何使用元件的描述。</span><span class="sxs-lookup"><span data-stu-id="b2635-134">Description of how your application uses the component.</span></span> <span data-ttu-id="b2635-135">此值最多可包含256個字元。</span><span class="sxs-lookup"><span data-stu-id="b2635-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="b2635-136">*WMP \_ 版本*</span><span class="sxs-lookup"><span data-stu-id="b2635-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="b2635-137">應用程式所需的 Windows Media Player 版本。</span><span class="sxs-lookup"><span data-stu-id="b2635-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="b2635-138">*WMF \_ 版本*</span><span class="sxs-lookup"><span data-stu-id="b2635-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="b2635-139">應用程式所需的 Windows Media 格式 SDK 版本。</span><span class="sxs-lookup"><span data-stu-id="b2635-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="b2635-140">下列三個範例登錄值示範如何設定應用程式的值：</span><span class="sxs-lookup"><span data-stu-id="b2635-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="b2635-141">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ App，"SouthridgeVideo"，"Southridge 影片播放程式"</span><span class="sxs-lookup"><span data-stu-id="b2635-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="b2635-142">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ 描述項，"SouthridgeVideo"，"Southridge Video Player 使用 Windows Media Format SDK 來播放影片檔案。"</span><span class="sxs-lookup"><span data-stu-id="b2635-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="b2635-143">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ Version，"SouthridgeVideo"，"9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="b2635-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2635-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2635-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2635-145">**專案考慮**</span><span class="sxs-lookup"><span data-stu-id="b2635-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




