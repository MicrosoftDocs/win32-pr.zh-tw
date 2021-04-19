---
title: Profiles
description: Profiles
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows Media Format SDK，設定檔
- Advanced Systems Format (ASF) ，設定檔
- ASF (Advanced Systems Format) ，設定檔
- Windows Media 格式 SDK、prx 檔案
- Advanced Systems Format (ASF) prx 檔案
- ASF (Advanced Systems Format) ，prx files
- Windows Media Format SDK，設定檔編輯器
- Advanced Systems Format (ASF) ，設定檔編輯器
- ASF (Advanced 系統格式) ，設定檔編輯器
- prx 檔案
- prx 檔案
- 設定檔編輯器
- Windows Media Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de244445a7c1301c7a14ef273b81ac9fd9cbfb62
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106991097"
---
# <a name="profiles"></a><span data-ttu-id="fd16d-116">Profiles</span><span class="sxs-lookup"><span data-stu-id="fd16d-116">Profiles</span></span>

<span data-ttu-id="fd16d-117">設定檔是描述 ASF 檔案設定的資料集合。</span><span class="sxs-lookup"><span data-stu-id="fd16d-117">A profile is a collection of data that describes the configuration of an ASF file.</span></span> <span data-ttu-id="fd16d-118">設定檔至少必須包含單一資料流程的設定。</span><span class="sxs-lookup"><span data-stu-id="fd16d-118">At a minimum, a profile must contain configuration settings for a single stream.</span></span>

<span data-ttu-id="fd16d-119">設定檔中的資料流程資訊包含資料流程的位元速率、緩衝區視窗和媒體屬性。</span><span class="sxs-lookup"><span data-stu-id="fd16d-119">The stream information in a profile contains the bit rate, buffer window, and media properties for the stream.</span></span> <span data-ttu-id="fd16d-120">音訊和影片的串流資訊會完全描述檔案中的媒體設定方式，包括在使用任何) 來壓縮資料時 (的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="fd16d-120">The stream information for audio and video describes exactly how the media is configured in the file, including which codec (if any) will be used to compress the data.</span></span>

<span data-ttu-id="fd16d-121">設定檔也包含各種 ASF 檔案功能的相關資訊，這些功能將用於以它建立的檔案。</span><span class="sxs-lookup"><span data-stu-id="fd16d-121">A profile also contains information about the various ASF file features that will be used in files created with it.</span></span> <span data-ttu-id="fd16d-122">這些包括 [互斥](mutual-exclusion.md)、 [串流優先順序](stream-prioritization.md)、 [頻寬共用](bandwidth-sharing.md)和 [資料單位延伸](data-unit-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="fd16d-122">These include [Mutual Exclusion](mutual-exclusion.md), [Stream Prioritization](stream-prioritization.md), [Bandwidth Sharing](bandwidth-sharing.md), and [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="fd16d-123">舊版 Windows Media Format SDK 提供預先設定的系統設定檔，可用來建立一般類型的檔案，或稍微改變以符合您應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="fd16d-123">Previous versions of the Windows Media Format SDK provided preconfigured system profiles, which could be used to create common types of files, or altered slightly to suit the needs of your application.</span></span> <span data-ttu-id="fd16d-124">Windows Media 9 系列編解碼器不支援系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="fd16d-124">System profiles are not supported for the Windows Media 9 Series codecs.</span></span> <span data-ttu-id="fd16d-125">這是因為「一般」檔案類型的數目隨著新功能的增加而以指數方式成長。</span><span class="sxs-lookup"><span data-stu-id="fd16d-125">This is because the number of "common" types of files has grown exponentially with the addition of new features.</span></span> <span data-ttu-id="fd16d-126">預期幾乎每個內容建立者都需要超越系統設定檔所提供的簡單解決方案。</span><span class="sxs-lookup"><span data-stu-id="fd16d-126">It is expected that virtually every content creator has needs that go beyond the simple solutions provided by system profiles.</span></span> <span data-ttu-id="fd16d-127">您仍然可以使用舊的系統設定檔作為起點。</span><span class="sxs-lookup"><span data-stu-id="fd16d-127">You can still use the old system profiles as a starting place.</span></span> <span data-ttu-id="fd16d-128">如需詳細資訊，請參閱 [使用系統設定檔](using-system-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="fd16d-128">For more information, see [Using System Profiles](using-system-profiles.md).</span></span>

<span data-ttu-id="fd16d-129">您必須為寫入器提供每個檔案的設定檔。</span><span class="sxs-lookup"><span data-stu-id="fd16d-129">You must supply the writer with a profile for every file you write.</span></span> <span data-ttu-id="fd16d-130">您可以藉由呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)來指定要搭配寫入器使用的設定檔。</span><span class="sxs-lookup"><span data-stu-id="fd16d-130">You can specify a profile to use with the writer by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span>

<span data-ttu-id="fd16d-131">設定檔資料有數種不同的形式，可供 Windows Media 格式 SDK 使用。</span><span class="sxs-lookup"><span data-stu-id="fd16d-131">Profile data exists in several different forms that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="fd16d-132">您也可以透過數種方式來存取設定檔資訊。</span><span class="sxs-lookup"><span data-stu-id="fd16d-132">Profile information can also be accessed in several ways.</span></span> <span data-ttu-id="fd16d-133">這可能會對設定檔及其使用方式造成混淆。</span><span class="sxs-lookup"><span data-stu-id="fd16d-133">This can lead to confusion about what a profile is and how it is used.</span></span>

<span data-ttu-id="fd16d-134">下圖顯示如何在 SDK 中使用設定檔資料。</span><span class="sxs-lookup"><span data-stu-id="fd16d-134">The following diagram shows how profile data is used in the SDK.</span></span>

![顯示設定檔資訊流程的圖表。](images/formatsdk01.png)

<span data-ttu-id="fd16d-136">設定檔資料採用三種不同的形式：包含在應用程式中的設定檔物件內的資料、在磁片上的 XML 檔案，以及 ASF 檔案標頭中的資料。</span><span class="sxs-lookup"><span data-stu-id="fd16d-136">Profile data takes three different forms: data contained within a profile object in an application, an XML file on disk, and data in the header of an ASF file.</span></span> <span data-ttu-id="fd16d-137">這兩種形式的資料會顯示為圖表中的陰影矩形。</span><span class="sxs-lookup"><span data-stu-id="fd16d-137">Each of these forms of data is shown as a shaded rectangle in the diagram.</span></span>

## <a name="data-in-a-profile-object"></a><span data-ttu-id="fd16d-138">設定檔物件中的資料</span><span class="sxs-lookup"><span data-stu-id="fd16d-138">Data in a Profile Object</span></span>

<span data-ttu-id="fd16d-139">當您編輯設定檔時，您會使用設定檔物件，該物件會封裝所有的設定檔資料。</span><span class="sxs-lookup"><span data-stu-id="fd16d-139">When you are editing a profile, you use a profile object, which encapsulates all of the profile data.</span></span> <span data-ttu-id="fd16d-140">您可以使用 [配置檔案管理員] 物件來建立空白的設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="fd16d-140">You can create an empty profile object by using the profile manager object.</span></span> <span data-ttu-id="fd16d-141">您也可以使用配置檔案管理員物件，將現有的設定檔資料載入至設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="fd16d-141">You can also use the profile manager object to load existing profile data into a profile object.</span></span>

<span data-ttu-id="fd16d-142">大部分的設定檔資料都必須透過使用代表設定檔個別部分的物件來新增和操作。</span><span class="sxs-lookup"><span data-stu-id="fd16d-142">Most profile data must be added and manipulated through the use of objects representing individual parts of the profile.</span></span> <span data-ttu-id="fd16d-143">這些包括串流設定物件、相互排除物件、頻寬共用物件，以及資料流程優先順序物件。</span><span class="sxs-lookup"><span data-stu-id="fd16d-143">These include stream configuration objects, mutual exclusion objects, bandwidth sharing objects, and a stream prioritization object.</span></span> <span data-ttu-id="fd16d-144">您可以使用設定檔物件中的方法來建立每個物件類型。</span><span class="sxs-lookup"><span data-stu-id="fd16d-144">Each of these object types can be created using methods in the profile object.</span></span> <span data-ttu-id="fd16d-145">除非您使用設定檔物件中的方法，以包含來自其他物件的更新資料，否則對這些物件進行變更並不會影響設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="fd16d-145">Making changes to these objects does not affect the profile object until you use a method in the profile object to include the updated data from the other object.</span></span>

## <a name="data-in-an-xml-file"></a><span data-ttu-id="fd16d-146">XML 檔案中的資料</span><span class="sxs-lookup"><span data-stu-id="fd16d-146">Data in an XML File</span></span>

<span data-ttu-id="fd16d-147">設定檔資料會以 XML 檔案的形式儲存在磁片上，其副檔名為 prx。</span><span class="sxs-lookup"><span data-stu-id="fd16d-147">Profile data is stored on disk in the form of an XML file with the .prx file name extension.</span></span> <span data-ttu-id="fd16d-148">Windows Media Format SDK 隨附的設定檔集合，稱為系統設定檔，其中涵蓋最常見的 ASF 檔類型。</span><span class="sxs-lookup"><span data-stu-id="fd16d-148">Included with the Windows Media Format SDK is a collection of profiles called system profiles that cover the most common types of ASF files.</span></span> <span data-ttu-id="fd16d-149">系統設定檔會儲存在名為 WMSysPr9. prx 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="fd16d-149">System profiles are stored in a file named WMSysPr9.prx.</span></span> <span data-ttu-id="fd16d-150"> (請注意，此檔案實際上不包含 Windows Media 9 系列的系統設定檔，因為系統設定檔的概念已不再使用 ) 。當您儲存自己的自訂設定檔時，必須將它們儲存到您自己的檔案中。</span><span class="sxs-lookup"><span data-stu-id="fd16d-150">(Note that this file actually contains no system profiles for Windows Media 9 Series because the concept of system profiles is no longer used.) When you save your own custom profiles, you must save them to your own files.</span></span>

<span data-ttu-id="fd16d-151">您可以使用 [配置檔案管理員] 物件，將設定檔物件的資料儲存至 XML 文字字串。</span><span class="sxs-lookup"><span data-stu-id="fd16d-151">You can use the profile manager object to save the data from a profile object to a string of XML text.</span></span> <span data-ttu-id="fd16d-152">然後，您可以使用任何您想要的檔案 i/o 功能，將字串儲存到磁片上的檔案中。</span><span class="sxs-lookup"><span data-stu-id="fd16d-152">You can then use whatever file I/O functions you like to save the string to a file on disk.</span></span>

## <a name="data-in-the-header-of-an-asf-file"></a><span data-ttu-id="fd16d-153">ASF 檔案標頭中的資料</span><span class="sxs-lookup"><span data-stu-id="fd16d-153">Data in the Header of an ASF File</span></span>

<span data-ttu-id="fd16d-154">寫入器會取得設定檔中的資訊，並使用它來建立資料流程，以進入 ASF 檔案的資料區段。</span><span class="sxs-lookup"><span data-stu-id="fd16d-154">The writer takes the information from the profile and uses it to create the streams that go into the data section of the ASF file.</span></span> <span data-ttu-id="fd16d-155">寫入檔案時，大量的設定檔資料會儲存在檔案的標頭區段中。</span><span class="sxs-lookup"><span data-stu-id="fd16d-155">The bulk of the profile data is stored in the header section of the file when a file is written.</span></span> <span data-ttu-id="fd16d-156">在播放時，[讀取器] 物件 (或同步讀取器物件) 可以存取檔案標頭中的資訊。</span><span class="sxs-lookup"><span data-stu-id="fd16d-156">At playback, the reader object (or the synchronous reader object) can access the information in the header of the file.</span></span> <span data-ttu-id="fd16d-157">在此情況下，讀取物件會建立設定檔物件，並在其中填入標頭中的資料。</span><span class="sxs-lookup"><span data-stu-id="fd16d-157">In this case, the reading object creates a profile object and populates it with the data from the header.</span></span>

<span data-ttu-id="fd16d-158">當您使用讀取器 (或同步讀取器) 來存取設定檔資料時，可以變更設定檔資訊，但無法在讀取器中將這些變更套用至檔案。</span><span class="sxs-lookup"><span data-stu-id="fd16d-158">When you access the profile data by using the reader (or synchronous reader), you can make changes to the profile information, but there is no way to apply those changes to the file in the reader.</span></span> <span data-ttu-id="fd16d-159">您可以將讀取器檔案中的設定檔資訊套用至寫入器中的設定檔，以建立新檔案，其設定與讀取器中的檔案相同。</span><span class="sxs-lookup"><span data-stu-id="fd16d-159">You can apply the profile information from a file in a reader to a profile in a writer to create a new file with the same settings as the file in the reader.</span></span> <span data-ttu-id="fd16d-160">在此情況下，您對設定檔中的設定檔資訊進行的任何變更，都會反映在寫入器所註冊的設定檔資訊中。</span><span class="sxs-lookup"><span data-stu-id="fd16d-160">In this case, any changes you make to the profile information prior to setting the profile in the writer will be reflected in the profile information registered by the writer.</span></span>

## <a name="using-profile-editor"></a><span data-ttu-id="fd16d-161">使用設定檔編輯器</span><span class="sxs-lookup"><span data-stu-id="fd16d-161">Using Profile Editor</span></span>

<span data-ttu-id="fd16d-162">除了使用 Windows Media Format SDK 建立設定檔之外，您還可以使用 [設定檔編輯器]，這是 Windows Media 編碼器隨附的公用程式。</span><span class="sxs-lookup"><span data-stu-id="fd16d-162">Rather than creating profiles by using the Windows Media Format SDK, you can use Profile Editor, a utility that is included with Windows Media Encoder.</span></span> <span data-ttu-id="fd16d-163">在您的編碼應用程式中，使用 **IWMProfileManager：： LoadProfileByData** 方法載入儲存的設定檔。</span><span class="sxs-lookup"><span data-stu-id="fd16d-163">In your encoding application, use the **IWMProfileManager::LoadProfileByData** method to load the saved profile.</span></span> <span data-ttu-id="fd16d-164">在某些情況下，例如，如果您使用永遠不會動態修改的有限設定檔數目，使用設定檔編輯器來建立您的設定檔可能會更方便。</span><span class="sxs-lookup"><span data-stu-id="fd16d-164">In some scenarios, for example if you use a limited number of profiles that are never modified dynamically, it might be more convenient to use the Profile Editor to create your profiles.</span></span>

<span data-ttu-id="fd16d-165">但是，如果您使用設定檔編輯器，建議您不要使用 [影片大小：與影片輸入相同] 設定。</span><span class="sxs-lookup"><span data-stu-id="fd16d-165">However, if you do use Profile Editor, it is recommended that you do not use the "Video Size: Same As Video Input" setting.</span></span> <span data-ttu-id="fd16d-166">核取此核取方塊時，[設定檔編輯器] 會建立一個設定檔，其中的影片輸出高度和寬度設定為零。</span><span class="sxs-lookup"><span data-stu-id="fd16d-166">When this check box is checked, Profile Editor will create a profile with the video output height and width set to zero.</span></span> <span data-ttu-id="fd16d-167">當 Windows Media 編碼器遇到這些設定檔時，會設定正確的值以符合其影片輸入。</span><span class="sxs-lookup"><span data-stu-id="fd16d-167">When Windows Media Encoder encounters these profiles, it sets the correct values to match its video input.</span></span> <span data-ttu-id="fd16d-168">不過，Windows Media 格式 SDK 中的寫入器不會自動執行這項作業，因此您必須確保應用程式在設定檔沒有任何情況下，設定影片框架大小。</span><span class="sxs-lookup"><span data-stu-id="fd16d-168">However, the Writer in the Windows Media Format SDK does not do so automatically, so you must ensure that your application sets the video frame size in cases where the profile has none.</span></span>

<span data-ttu-id="fd16d-169">**注意** 部分串流設定專案不會儲存在設定檔中。</span><span class="sxs-lookup"><span data-stu-id="fd16d-169">**Note** Some stream configuration items are not stored in the profile.</span></span> <span data-ttu-id="fd16d-170">設定檔中的資料會描述已完成之 ASF 檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="fd16d-170">The data in the profile describes the format of the finished ASF file.</span></span> <span data-ttu-id="fd16d-171">寫入器物件用來設定編解碼器的輸入媒體屬性和其他設定資料，不會儲存在設定檔中。</span><span class="sxs-lookup"><span data-stu-id="fd16d-171">Input media properties and other configuration data used by the writer object to configure the codecs are not saved in the profile.</span></span> <span data-ttu-id="fd16d-172">這包括使用 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) 方法設定的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="fd16d-172">This includes all properties set by using the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd16d-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd16d-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd16d-174">**頻寬共用物件**</span><span class="sxs-lookup"><span data-stu-id="fd16d-174">**Bandwidth Sharing Object**</span></span>](bandwidth-sharing-object.md)
</dt> <dt>

[<span data-ttu-id="fd16d-175">**概念**</span><span class="sxs-lookup"><span data-stu-id="fd16d-175">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="fd16d-176">**IWMProfile 介面**</span><span class="sxs-lookup"><span data-stu-id="fd16d-176">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="fd16d-177">**IWMProfileManager 介面**</span><span class="sxs-lookup"><span data-stu-id="fd16d-177">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="fd16d-178">**相互排除物件**</span><span class="sxs-lookup"><span data-stu-id="fd16d-178">**Mutual Exclusion Object**</span></span>](mutual-exclusion-object.md)
</dt> <dt>

[<span data-ttu-id="fd16d-179">**設定檔管理員物件**</span><span class="sxs-lookup"><span data-stu-id="fd16d-179">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="fd16d-180">**串流設定物件**</span><span class="sxs-lookup"><span data-stu-id="fd16d-180">**Stream Configuration Object**</span></span>](stream-configuration-object.md)
</dt> <dt>

[<span data-ttu-id="fd16d-181">**串流優先順序物件**</span><span class="sxs-lookup"><span data-stu-id="fd16d-181">**Stream Prioritization Object**</span></span>](stream-prioritization-object.md)
</dt> <dt>

[<span data-ttu-id="fd16d-182">**使用設定檔**</span><span class="sxs-lookup"><span data-stu-id="fd16d-182">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




