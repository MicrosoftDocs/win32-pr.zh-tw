---
title: Windows Media Player SDK) 註冊應用程式相依性 (
description: 瞭解如何向 Windows Media Player SDK 所提供之 Api 的執行時間元件註冊您的應用程式。
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player，應用程式相依性登錄設定
- Windows Media Player，相依性登錄設定
- Windows Media Player，登錄
- 登錄，應用程式相依性設定
- 登錄，相依性設定
- 登錄，Windows Media Player 的設定
- 相依性登錄設定
- 應用程式相依性登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b1692c6a4e1a8274472bbe9d718721c1ab4f1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407361"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="2b0d5-111">Windows Media Player SDK) 註冊應用程式相依性 (</span><span class="sxs-lookup"><span data-stu-id="2b0d5-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="2b0d5-112">使用 Windows Media Player SDK 或 Windows Media 格式 SDK 所提供之 Api 的應用程式，會根據這些技術的執行時間元件而定。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="2b0d5-113">您可以在應用程式設定中註冊應用程式，使其相依于這些元件。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="2b0d5-114">當您註冊應用程式時，您可以選擇兩個相依性層級的其中一個：封鎖或相依。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="2b0d5-115">當一個或多個應用程式在其中一個執行時間元件的封鎖相依性註冊時，元件將會遭到封鎖而無法回復為先前的版本。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="2b0d5-116">未註冊為封鎖的相依應用程式不會封鎖復原。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="2b0d5-117">相反地，在執行復原之前，使用者會看到一則訊息，指出應用程式相依于元件。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="2b0d5-118">若要註冊您的應用程式，您必須在登錄中設定用來識別應用程式的值。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="2b0d5-119">要設定的登錄值取決於您的應用程式相依的元件。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="2b0d5-120">您也可以為每個相依性設定兩個額外的值，以提供應用程式的額外資訊。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="2b0d5-121">下列登錄值會用來註冊 Windows Media Player SDK 執行時間的相依性：</span><span class="sxs-lookup"><span data-stu-id="2b0d5-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="2b0d5-122">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ *REF \_ TYPE* \\ App，"*app*"，"*應用程式 \_ 字串*"</span><span class="sxs-lookup"><span data-stu-id="2b0d5-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="2b0d5-123">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ *REF \_ TYPE* \\ 描述元，"*APP*"，"*REF \_ 描述* 元"</span><span class="sxs-lookup"><span data-stu-id="2b0d5-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="2b0d5-124">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ *REF \_ TYPE* \\ Version，"*APP*"，"*WMP \_ version*"</span><span class="sxs-lookup"><span data-stu-id="2b0d5-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="2b0d5-125">下列登錄值會用來註冊 Windows Media Format SDK runtime 的相依性：</span><span class="sxs-lookup"><span data-stu-id="2b0d5-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="2b0d5-126">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *REF \_ TYPE* \\ App，"*app*"，"*應用程式 \_ 字串*"</span><span class="sxs-lookup"><span data-stu-id="2b0d5-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="2b0d5-127">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *REF \_ TYPE* \\ 描述元，"*APP*"，"*REF \_ 描述* 元"</span><span class="sxs-lookup"><span data-stu-id="2b0d5-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="2b0d5-128">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *REF \_ TYPE* \\ Version，"*APP*"，"*WMF \_ Version*"</span><span class="sxs-lookup"><span data-stu-id="2b0d5-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="2b0d5-129">下列變數會用於上述的登錄值：</span><span class="sxs-lookup"><span data-stu-id="2b0d5-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="2b0d5-130">*REF \_ 類型*</span><span class="sxs-lookup"><span data-stu-id="2b0d5-130">*REF\_TYPE*</span></span>

<span data-ttu-id="2b0d5-131">取代為封鎖相依性的 BlockingRefCounts，或針對非封鎖相依性使用 DependentRefCounts 取代。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="2b0d5-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="2b0d5-132">*APP*</span></span>

<span data-ttu-id="2b0d5-133">應用程式的名稱或簡短描述項。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="2b0d5-134">此字串不會用於使用者顯示的訊息。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="2b0d5-135">此值是與每個執行時間元件相關聯的三個登錄值所使用的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="2b0d5-136">*應用程式 \_ 字串*</span><span class="sxs-lookup"><span data-stu-id="2b0d5-136">*APP\_STRING*</span></span>

<span data-ttu-id="2b0d5-137">應用程式的描述項。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-137">Descriptor of your application.</span></span> <span data-ttu-id="2b0d5-138">這個字串可用於顯示給使用者的訊息。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="2b0d5-139">*參考 \_ 描述元*</span><span class="sxs-lookup"><span data-stu-id="2b0d5-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="2b0d5-140">應用程式如何使用元件的描述。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-140">Description of how your application uses the component.</span></span> <span data-ttu-id="2b0d5-141">此值最多可包含256個字元。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="2b0d5-142">*WMP \_ 版本*</span><span class="sxs-lookup"><span data-stu-id="2b0d5-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="2b0d5-143">應用程式所需的 Windows Media Player 版本。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="2b0d5-144">如果未指定任何版本，則會假設預設值為9.0.0.0。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="2b0d5-145">*WMF \_ 版本*</span><span class="sxs-lookup"><span data-stu-id="2b0d5-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="2b0d5-146">應用程式所需的 Windows Media 格式 SDK 版本。</span><span class="sxs-lookup"><span data-stu-id="2b0d5-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="2b0d5-147">下列三個範例登錄值示範如何設定應用程式的值：</span><span class="sxs-lookup"><span data-stu-id="2b0d5-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="2b0d5-148">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ App，"SouthridgeVideo"，"Southridge 影片播放程式"</span><span class="sxs-lookup"><span data-stu-id="2b0d5-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="2b0d5-149">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ 描述項，"SouthridgeVideo"，"Southridge Video Player 使用 Windows Media Format SDK 來播放影片檔案。"</span><span class="sxs-lookup"><span data-stu-id="2b0d5-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="2b0d5-150">HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Version，"SouthridgeVideo"，"9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="2b0d5-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b0d5-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b0d5-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b0d5-152">**登錄設定**</span><span class="sxs-lookup"><span data-stu-id="2b0d5-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




