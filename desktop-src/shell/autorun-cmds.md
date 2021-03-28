---
description: 本主題是可在自動播放 .inf 檔案中使用之專案的參考。 專案是由索引鍵和值所組成。
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: 自動播放 .inf 專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191186"
---
# <a name="autoruninf-entries"></a><span data-ttu-id="adfd6-104">自動播放 .inf 專案</span><span class="sxs-lookup"><span data-stu-id="adfd6-104">Autorun.inf Entries</span></span>

<span data-ttu-id="adfd6-105">本主題是可在自動播放 .inf 檔案中使用之專案的參考。</span><span class="sxs-lookup"><span data-stu-id="adfd6-105">This topic is a reference for the entries that can be used in an Autorun.inf file.</span></span> <span data-ttu-id="adfd6-106">專案是由索引鍵和值所組成。</span><span class="sxs-lookup"><span data-stu-id="adfd6-106">An entry consists of a key and a value.</span></span>

-   <span data-ttu-id="adfd6-107">[\[自動運行機 \] 碼](#autorun-keys)</span><span class="sxs-lookup"><span data-stu-id="adfd6-107">[\[AutoRun\] Keys](#autorun-keys)</span></span>
    -   [<span data-ttu-id="adfd6-108">action</span><span class="sxs-lookup"><span data-stu-id="adfd6-108">action</span></span>](#parameters)
    -   [<span data-ttu-id="adfd6-109">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="adfd6-109">CustomEvent</span></span>](#customevent)
    -   [<span data-ttu-id="adfd6-110">圖示</span><span class="sxs-lookup"><span data-stu-id="adfd6-110">icon</span></span>](#parameters)
    -   [<span data-ttu-id="adfd6-111">label</span><span class="sxs-lookup"><span data-stu-id="adfd6-111">label</span></span>](#parameters)
    -   [<span data-ttu-id="adfd6-112">open</span><span class="sxs-lookup"><span data-stu-id="adfd6-112">open</span></span>](#parameters)
    -   [<span data-ttu-id="adfd6-113">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="adfd6-113">UseAutoPlay</span></span>](#parameters)
    -   [<span data-ttu-id="adfd6-114">shellexecute</span><span class="sxs-lookup"><span data-stu-id="adfd6-114">shellexecute</span></span>](#shellexecute)
    -   [<span data-ttu-id="adfd6-115">殼</span><span class="sxs-lookup"><span data-stu-id="adfd6-115">shell</span></span>](#autoruninf-entries)
    -   [<span data-ttu-id="adfd6-116">shell \\ 動詞</span><span class="sxs-lookup"><span data-stu-id="adfd6-116">shell\\verb</span></span>](#shellverb)
-   <span data-ttu-id="adfd6-117">[\[內容 \] 金鑰](#content-keys)</span><span class="sxs-lookup"><span data-stu-id="adfd6-117">[\[Content\] Keys](#content-keys)</span></span>
-   <span data-ttu-id="adfd6-118">[\[ExclusiveContentPaths 索引 \] 鍵](#exclusivecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="adfd6-118">[\[ExclusiveContentPaths\] Keys](#exclusivecontentpaths-keys)</span></span>
-   <span data-ttu-id="adfd6-119">[\[IgnoreContentPaths 索引 \] 鍵](#ignorecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="adfd6-119">[\[IgnoreContentPaths\] Keys](#ignorecontentpaths-keys)</span></span>
-   <span data-ttu-id="adfd6-120">[\[DeviceInstall 索引 \] 鍵](#deviceinstall-keys)</span><span class="sxs-lookup"><span data-stu-id="adfd6-120">[\[DeviceInstall\] Keys](#deviceinstall-keys)</span></span>
    -   [<span data-ttu-id="adfd6-121">DriverPath</span><span class="sxs-lookup"><span data-stu-id="adfd6-121">DriverPath</span></span>](#driverpath)

## <a name="autorun-keys"></a><span data-ttu-id="adfd6-122">\[自動運行機 \] 碼</span><span class="sxs-lookup"><span data-stu-id="adfd6-122">\[AutoRun\] Keys</span></span>

-   [<span data-ttu-id="adfd6-123">action</span><span class="sxs-lookup"><span data-stu-id="adfd6-123">action</span></span>](#parameters)
-   [<span data-ttu-id="adfd6-124">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="adfd6-124">CustomEvent</span></span>](#customevent)
-   [<span data-ttu-id="adfd6-125">圖示</span><span class="sxs-lookup"><span data-stu-id="adfd6-125">icon</span></span>](#parameters)
-   [<span data-ttu-id="adfd6-126">label</span><span class="sxs-lookup"><span data-stu-id="adfd6-126">label</span></span>](#parameters)
-   [<span data-ttu-id="adfd6-127">open</span><span class="sxs-lookup"><span data-stu-id="adfd6-127">open</span></span>](#parameters)
-   [<span data-ttu-id="adfd6-128">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="adfd6-128">UseAutoPlay</span></span>](#parameters)
-   [<span data-ttu-id="adfd6-129">shellexecute</span><span class="sxs-lookup"><span data-stu-id="adfd6-129">shellexecute</span></span>](#shellexecute)
-   [<span data-ttu-id="adfd6-130">殼</span><span class="sxs-lookup"><span data-stu-id="adfd6-130">shell</span></span>](#autoruninf-entries)
-   [<span data-ttu-id="adfd6-131">shell \\ 動詞</span><span class="sxs-lookup"><span data-stu-id="adfd6-131">shell\\verb</span></span>](#shellverb)

### <a name="action"></a><span data-ttu-id="adfd6-132">動作</span><span class="sxs-lookup"><span data-stu-id="adfd6-132">action</span></span>

<span data-ttu-id="adfd6-133">**動作** 專案會指定處理常式的 [自動播放] 對話方塊中所使用的文字，此處理程式代表媒體的 [自動執行] .inf 檔案中的 [open](#parameters)或 [shellexecute](#shellexecute)專案所指定的程式。</span><span class="sxs-lookup"><span data-stu-id="adfd6-133">The **action** entry specifies the text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span> <span data-ttu-id="adfd6-134">值可以是文字或以二進位格式儲存的資源。</span><span class="sxs-lookup"><span data-stu-id="adfd6-134">The value can be expressed as either text or as a resource stored in a binary.</span></span>


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a><span data-ttu-id="adfd6-135">參數</span><span class="sxs-lookup"><span data-stu-id="adfd6-135">Parameters</span></span>

-   <span data-ttu-id="adfd6-136">*ActionText*</span><span class="sxs-lookup"><span data-stu-id="adfd6-136">*ActionText*</span></span>

    <span data-ttu-id="adfd6-137">處理常式的 [自動播放] 對話方塊中所使用的文字，表示媒體的 [自動播放] 檔案中的 [open](#parameters) 或 [shellexecute](#shellexecute) 專案所指定的程式。</span><span class="sxs-lookup"><span data-stu-id="adfd6-137">Text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span>

-   <span data-ttu-id="adfd6-138">*filepath*</span><span class="sxs-lookup"><span data-stu-id="adfd6-138">*filepath*</span></span>

    <span data-ttu-id="adfd6-139">字串，其中包含目錄的完整路徑，該目錄包含包含字串的二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="adfd6-139">A string that contains the fully qualified path of the directory that contains the binary file containing the string.</span></span> <span data-ttu-id="adfd6-140">如果未指定路徑，則檔案必須位於磁片磁碟機的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="adfd6-140">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="adfd6-141">*filename*</span><span class="sxs-lookup"><span data-stu-id="adfd6-141">*filename*</span></span>

    <span data-ttu-id="adfd6-142">包含二進位檔案名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="adfd6-142">A string that contains the binary file's name.</span></span>

-   <span data-ttu-id="adfd6-143">*Id*</span><span class="sxs-lookup"><span data-stu-id="adfd6-143">*resourceID*</span></span>

    <span data-ttu-id="adfd6-144">二進位檔案中的字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="adfd6-144">The ID of the string within the binary file.</span></span>

### <a name="remarks"></a><span data-ttu-id="adfd6-145">備註</span><span class="sxs-lookup"><span data-stu-id="adfd6-145">Remarks</span></span>

<span data-ttu-id="adfd6-146">**動作** 金鑰僅適用于 Windows XP Service Pack 2 (SP2) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="adfd6-146">The **action** key is only used in Windows XP Service Pack 2 (SP2) or later.</span></span> <span data-ttu-id="adfd6-147">只有磁片磁碟機的磁片磁碟機卸載式 \_ 和磁片磁碟機 \_ 固定支援。</span><span class="sxs-lookup"><span data-stu-id="adfd6-147">It is only supported for drives of type DRIVE\_REMOVABLE and DRIVE\_FIXED.</span></span> <span data-ttu-id="adfd6-148">在卸載磁片磁碟機的情況下 \_ ，需要 **動作** 金鑰。</span><span class="sxs-lookup"><span data-stu-id="adfd6-148">In the case of DRIVE\_REMOVABLE, the **action** key is required.</span></span> <span data-ttu-id="adfd6-149">音訊 CD 或電影 DVD 的執行中 .inf 檔案中的 **動作** 命令會被忽略，而這些媒體會在 Windows XP Service Pack 1 (SP1) 和更早版本中繼續運作。</span><span class="sxs-lookup"><span data-stu-id="adfd6-149">An **action** command in the Autorun.inf file of an audio CD or movie DVD is ignored, and these media continue to behave as in Windows XP Service Pack 1 (SP1) and earlier.</span></span>

<span data-ttu-id="adfd6-150">在 [自動播放] 對話方塊中顯示的字串，是藉由將 **動作** 專案中指定的文字與提供者的硬式編碼文字（由 Shell 所提供）結合在一起。</span><span class="sxs-lookup"><span data-stu-id="adfd6-150">The string displayed in the Autoplay dialog is constructed by combining the text specified in the **action** entry with hard-coded text naming the provider, provided by the Shell.</span></span> <span data-ttu-id="adfd6-151">圖示旁邊會顯示 [圖示](#parameters) 。</span><span class="sxs-lookup"><span data-stu-id="adfd6-151">The [icon](#parameters) is displayed next to it.</span></span> <span data-ttu-id="adfd6-152">此專案一律會顯示為 [自動播放] 對話方塊中的第一個選項，而且預設為選取。</span><span class="sxs-lookup"><span data-stu-id="adfd6-152">This entry always appears as the first option in the Autoplay dialog and is selected by default.</span></span> <span data-ttu-id="adfd6-153">如果使用者接受選項，則會啟動媒體的自動運行時檔案中的 [open](#parameters) 或 [shellexecute](#shellexecute) 專案所指定的應用程式。</span><span class="sxs-lookup"><span data-stu-id="adfd6-153">If the user accepts the option, the application specified by the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file is launched.</span></span> <span data-ttu-id="adfd6-154">在此情況下，[ **永遠執行選取的動作** ] 選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="adfd6-154">The **Always do the selected action** option is not available in this situation.</span></span>

<span data-ttu-id="adfd6-155">[動作](#parameters)和[圖示](#parameters)按鍵會定義使用者在 [自動播放] 對話方塊中看到的應用程式標記法。</span><span class="sxs-lookup"><span data-stu-id="adfd6-155">The [action](#parameters) and [icon](#parameters) keys together define the representation of the application that is seen by the end user in the Autoplay dialog.</span></span> <span data-ttu-id="adfd6-156">它們應該以使用者可以輕鬆識別的方式來撰寫。</span><span class="sxs-lookup"><span data-stu-id="adfd6-156">They should be composed in such a way that users can easily identify them.</span></span> <span data-ttu-id="adfd6-157">他們應該會指出要執行的應用程式、建立該應用程式的公司，以及任何相關聯的商標。</span><span class="sxs-lookup"><span data-stu-id="adfd6-157">They should indicate the application to be run, the company that created it, and any associated branding.</span></span>

<span data-ttu-id="adfd6-158">為了回溯相容性，對於磁片磁碟機類型的裝置而言， **動作** 專案是選擇性的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="adfd6-158">For backward compatibility, the **action** entry is optional for devices of type DRIVE\_FIXED.</span></span> <span data-ttu-id="adfd6-159">針對此類型，如果執行 .inf 檔案中沒有 **動作** 專案，則會在 [自動播放] 對話方塊中使用預設專案。</span><span class="sxs-lookup"><span data-stu-id="adfd6-159">For this type, a default entry is used in the Autoplay dialog if no **action** entry is present in the Autorun.inf file.</span></span>

<span data-ttu-id="adfd6-160">「 磁片磁碟機卸載」類型的裝置必須 \_ 要有動作專案，直到現在沒有支援 .inf 的支援。</span><span class="sxs-lookup"><span data-stu-id="adfd6-160">The **action** entry is mandatory for devices of type DRIVE\_REMOVABLE, which until now did not have Autorun.inf support.</span></span> <span data-ttu-id="adfd6-161">如果沒有 **動作** 專案存在，則會顯示 [自動播放] 對話方塊，但沒有任何選項可啟動其他內容。</span><span class="sxs-lookup"><span data-stu-id="adfd6-161">If no **action** entry is present, the Autoplay dialog is displayed but with no option to launch the additional content.</span></span>

### <a name="customevent"></a><span data-ttu-id="adfd6-162">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="adfd6-162">CustomEvent</span></span>

<span data-ttu-id="adfd6-163">**CustomEvent** 專案會指定自訂的自動播放內容事件。</span><span class="sxs-lookup"><span data-stu-id="adfd6-163">The **CustomEvent** entry specifies a custom AutoPlay content event.</span></span>


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a><span data-ttu-id="adfd6-164">參數</span><span class="sxs-lookup"><span data-stu-id="adfd6-164">Parameters</span></span>

-   <span data-ttu-id="adfd6-165">*CustomEventName*</span><span class="sxs-lookup"><span data-stu-id="adfd6-165">*CustomEventName*</span></span>

    <span data-ttu-id="adfd6-166">包含自動播放內容事件名稱的文字字串。</span><span class="sxs-lookup"><span data-stu-id="adfd6-166">A text string containing the name of the AutoPlay content event.</span></span> <span data-ttu-id="adfd6-167">名稱不得超過100個英數位元。</span><span class="sxs-lookup"><span data-stu-id="adfd6-167">The name must be no more than 100 alphanumeric characters.</span></span>

### <a name="remarks"></a><span data-ttu-id="adfd6-168">備註</span><span class="sxs-lookup"><span data-stu-id="adfd6-168">Remarks</span></span>

<span data-ttu-id="adfd6-169">您可以在磁片區的 [自動播放] 檔案中包含自訂事件名稱。</span><span class="sxs-lookup"><span data-stu-id="adfd6-169">You can include a custom event name in the Autorun.inf file of a volume.</span></span> <span data-ttu-id="adfd6-170">當自動播放提示使用者將應用程式用於磁片區時，它只會顯示已針對指定的自訂事件名稱註冊的應用程式。</span><span class="sxs-lookup"><span data-stu-id="adfd6-170">When AutoPlay prompts the user for an application to use with the volume, it displays only applications that have registered for the specified custom event name.</span></span> <span data-ttu-id="adfd6-171">如需如何將應用程式註冊為自訂自動播放內容事件之處理常式的詳細資訊，請參閱 [使用自動播放自動啟動](/previous-versions/windows/apps/hh452731(v=win.10)) 或 [如何註冊事件處理常式](how-to-register-an-event-handler.md)。</span><span class="sxs-lookup"><span data-stu-id="adfd6-171">For information on how you can register an application as a handler for your custom AutoPlay content event, see [Auto-launching with AutoPlay](/previous-versions/windows/apps/hh452731(v=win.10)) or [How to Register an Event Handler](how-to-register-an-event-handler.md).</span></span>

<span data-ttu-id="adfd6-172">下列範例會將 "MyContentOnArrival" 值指定為新的自動播放內容事件。</span><span class="sxs-lookup"><span data-stu-id="adfd6-172">The following example specifies the value "MyContentOnArrival" as a new AutoPlay content event.</span></span>


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a><span data-ttu-id="adfd6-173">icon</span><span class="sxs-lookup"><span data-stu-id="adfd6-173">icon</span></span>

<span data-ttu-id="adfd6-174">**圖示** 專案會指定代表 Windows 使用者介面中啟用自動啟用磁片磁碟機的圖示。</span><span class="sxs-lookup"><span data-stu-id="adfd6-174">The **icon** entry specifies an icon which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
icon=iconfilename[,index]
```



### <a name="parameters"></a><span data-ttu-id="adfd6-175">參數</span><span class="sxs-lookup"><span data-stu-id="adfd6-175">Parameters</span></span>

-   <span data-ttu-id="adfd6-176">*iconfilename*</span><span class="sxs-lookup"><span data-stu-id="adfd6-176">*iconfilename*</span></span>

    <span data-ttu-id="adfd6-177">包含圖示資訊之 .ico、.bmp、.exe 或 .dll 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="adfd6-177">Name of an .ico, .bmp, .exe, or .dll file containing the icon information.</span></span> <span data-ttu-id="adfd6-178">如果檔案包含一個以上的圖示，您也必須指定圖示的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="adfd6-178">If a file contains more than one icon, you must also specify zero-based index of the icon.</span></span>

### <a name="remarks"></a><span data-ttu-id="adfd6-179">備註</span><span class="sxs-lookup"><span data-stu-id="adfd6-179">Remarks</span></span>

<span data-ttu-id="adfd6-180">圖示（連同標籤）表示 Windows 使用者介面中啟用自動啟動的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="adfd6-180">The icon, together with the label, represents the AutoRun-enabled drive in the Windows user interface.</span></span> <span data-ttu-id="adfd6-181">例如，在 Windows 檔案總管中，磁片磁碟機是以這個圖示而非標準磁片磁碟機圖示來表示。</span><span class="sxs-lookup"><span data-stu-id="adfd6-181">For instance, in Windows Explorer, the drive is represented by this icon instead of the standard drive icon.</span></span> <span data-ttu-id="adfd6-182">圖示的檔案必須與 [open](#parameters) 命令所指定的檔案位於相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="adfd6-182">The icon's file must be in the same directory as the file specified by the [open](#parameters) command.</span></span>

<span data-ttu-id="adfd6-183">下列範例會指定 MyProg.exe 檔中的第二個圖示。</span><span class="sxs-lookup"><span data-stu-id="adfd6-183">The following example specifies the second icon in the MyProg.exe file.</span></span>


```
icon=MyProg.exe,1
```



### <a name="label"></a><span data-ttu-id="adfd6-184">label</span><span class="sxs-lookup"><span data-stu-id="adfd6-184">label</span></span>

<span data-ttu-id="adfd6-185">**標籤** 專案會指定文字標籤，表示 Windows 使用者介面中啟用自動啟用的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="adfd6-185">The **label** entry specifies a text label which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
label=LabelText
```



### <a name="parameters"></a><span data-ttu-id="adfd6-186">參數</span><span class="sxs-lookup"><span data-stu-id="adfd6-186">Parameters</span></span>

-   <span data-ttu-id="adfd6-187">*LabelText*</span><span class="sxs-lookup"><span data-stu-id="adfd6-187">*LabelText*</span></span>

    <span data-ttu-id="adfd6-188">包含標籤的文字字串。</span><span class="sxs-lookup"><span data-stu-id="adfd6-188">A text string containing the label.</span></span> <span data-ttu-id="adfd6-189">它可以包含空格，而且不能超過32個字元。</span><span class="sxs-lookup"><span data-stu-id="adfd6-189">It can contain spaces and should be no longer than 32 characters.</span></span>

> [!Note]  
> <span data-ttu-id="adfd6-190">您可以在 **LabelText** 參數中放入超過32個字元的值，而且不會收到任何錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="adfd6-190">It is possible to put a value in the **LabelText** parameter which exceeds 32 characters and receive no error message.</span></span> <span data-ttu-id="adfd6-191">不過，系統只會顯示前32個字元。</span><span class="sxs-lookup"><span data-stu-id="adfd6-191">However, the system only displays the first 32 characters.</span></span> <span data-ttu-id="adfd6-192">第32之後的任何字元都會被截斷且不會顯示。</span><span class="sxs-lookup"><span data-stu-id="adfd6-192">Any characters after the 32nd are truncated and not displayed.</span></span> <span data-ttu-id="adfd6-193">例如，如果 **LabelText** 如下所示：標籤 = 「此 CD 設計為終極音樂 cd」。</span><span class="sxs-lookup"><span data-stu-id="adfd6-193">For example, if the **LabelText** is as follows: label="This CD is designed to be the ultimate music CD."</span></span> <span data-ttu-id="adfd6-194">將會顯示下列「此 CD 設計成 ul」。</span><span class="sxs-lookup"><span data-stu-id="adfd6-194">the following will be displayed, "This CD is designed to be the ul".</span></span>

 

### <a name="remarks"></a><span data-ttu-id="adfd6-195">備註</span><span class="sxs-lookup"><span data-stu-id="adfd6-195">Remarks</span></span>

<span data-ttu-id="adfd6-196">標籤連同圖示，代表 Windows 使用者介面中啟用自動啟動的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="adfd6-196">The label, together with an icon, represents the AutoRun-enabled drive in the Windows user interface.</span></span>

<span data-ttu-id="adfd6-197">下列範例會將「我的磁片磁碟機標籤」值指定為磁片磁碟機的標籤。</span><span class="sxs-lookup"><span data-stu-id="adfd6-197">The following example specifies the value "My Drive Label" as the drive's label.</span></span>


```
label=My Drive Label
```



### <a name="open"></a><span data-ttu-id="adfd6-198">開啟</span><span class="sxs-lookup"><span data-stu-id="adfd6-198">open</span></span>

<span data-ttu-id="adfd6-199">**開啟** 專案指定當使用者將光碟片插入磁片磁碟機時，自動啟動的應用程式路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="adfd6-199">The **open** entry specifies the path and file name of the application that AutoRun launches when a user inserts a disc in the drive.</span></span>


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a><span data-ttu-id="adfd6-200">參數</span><span class="sxs-lookup"><span data-stu-id="adfd6-200">Parameters</span></span>

-   <span data-ttu-id="adfd6-201">*exefile*</span><span class="sxs-lookup"><span data-stu-id="adfd6-201">*exefile*</span></span>

    <span data-ttu-id="adfd6-202">插入光碟時執行之可執行檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="adfd6-202">Fully qualified path of an executable file that runs when the CD is inserted.</span></span> <span data-ttu-id="adfd6-203">如果只指定檔案名，它必須位於磁片磁碟機的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="adfd6-203">If only a file name is specified, it must be in drive's root directory.</span></span> <span data-ttu-id="adfd6-204">若要在子目錄中找出檔案，您必須指定路徑。</span><span class="sxs-lookup"><span data-stu-id="adfd6-204">To locate the file in a subdirectory, you must specify a path.</span></span> <span data-ttu-id="adfd6-205">您也可以加入一或多個命令列參數，以傳遞至啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="adfd6-205">You can also include one or more command-line parameters to pass to the startup application.</span></span>

### <a name="useautoplay"></a><span data-ttu-id="adfd6-206">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="adfd6-206">UseAutoPlay</span></span>

<span data-ttu-id="adfd6-207">在 Windows XP 上， **UseAutoPlay** 專案指定應該使用自動播放，而不是自動播放。</span><span class="sxs-lookup"><span data-stu-id="adfd6-207">On Windows XP, the **UseAutoPlay** entry specifies that AutoPlay should be used instead of AutoRun.</span></span>

<span data-ttu-id="adfd6-208">在 Windows Vista （含）以後版本中，此專案會使用 [ **開啟** ] 或 [ **shellexecute** 專案]) ，從 [自動播放] 對話方塊中隱藏，導致任何針對自動執行 (指定的動作。</span><span class="sxs-lookup"><span data-stu-id="adfd6-208">On Windows Vista and later, this entry causes any actions specified for AutoRun (by using either the **open** or **shellexecute** entries) to be suppressed from the AutoPlay dialog.</span></span> <span data-ttu-id="adfd6-209">此專案對 Windows XP 之前的 Windows 版本沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="adfd6-209">This entry has no effect on versions of Windows earlier than Windows XP.</span></span>

<span data-ttu-id="adfd6-210">在 Windows 8 和更新版本上，指定值0將會停用此裝置的自動播放。</span><span class="sxs-lookup"><span data-stu-id="adfd6-210">On Windows 8 and later, specifying a value of 0 will disable autoplay for this device.</span></span>

### <a name="parameters"></a><span data-ttu-id="adfd6-211">參數</span><span class="sxs-lookup"><span data-stu-id="adfd6-211">Parameters</span></span>

<span data-ttu-id="adfd6-212">若要使用此選項，請將 **UseAutoPlay** 的專案新增至執行 .inf 檔案，並將專案設定為等於1。</span><span class="sxs-lookup"><span data-stu-id="adfd6-212">To use this option, add an entry for **UseAutoPlay** to the Autorun.inf file and set the entry equal to 1.</span></span> <span data-ttu-id="adfd6-213">在 Windows 8 之前的 Windows 版本上，不支援其他的值。</span><span class="sxs-lookup"><span data-stu-id="adfd6-213">No other value is supported on versions of Windows earlier than Windows 8.</span></span>

<span data-ttu-id="adfd6-214">在 Windows 8 和更新版本上，指定0的值以停用此裝置的自動播放。</span><span class="sxs-lookup"><span data-stu-id="adfd6-214">On Windows 8 and later, specify a value of 0 to disable autoplay for this device.</span></span>


```
UseAutoPlay=1
```



### <a name="remarks"></a><span data-ttu-id="adfd6-215">備註</span><span class="sxs-lookup"><span data-stu-id="adfd6-215">Remarks</span></span>

<span data-ttu-id="adfd6-216">目前， **UseAutoPlay** 僅適用于 Windows XP 或更新版本，且僅適用于 [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) 判斷為 **磁片磁碟機 \_ 光碟** 磁片磁碟機的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="adfd6-216">Currently, **UseAutoPlay** is applicable only on Windows XP or later and only on a drive that [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determines to be of type **DRIVE\_CDROM**.</span></span>

<span data-ttu-id="adfd6-217">使用 **UseAutoPlay** 時，windows XP 上的 **open** 或 **shellexecute** 專案所指定的任何動作都會被忽略，並在 Windows Vista 上的 [自動播放] 對話方塊中省略。</span><span class="sxs-lookup"><span data-stu-id="adfd6-217">When **UseAutoPlay** is used, any action specified by the **open** or **shellexecute** entries in Autorun.inf is ignored on Windows XP and omitted from the AutoPlay dialog on Windows Vista.</span></span>

<span data-ttu-id="adfd6-218">自動執行通常用來自動執行或載入插入的媒體上所含的某個內容，而 [自動播放] 則會顯示一個對話方塊，其中包含可能採取的相關動作清單，並可讓使用者選擇要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="adfd6-218">AutoRun is typically used to automatically run or load something contained on the inserted media, whereas AutoPlay presents a dialog that includes a list of relevant actions that may be taken and enables the user to choose which action to take.</span></span> <span data-ttu-id="adfd6-219">如需有關自動安裝和自動播放之間差異的詳細資訊，請參閱 [建立啟用自動啟動的 Cd-rom 應用程式](autoplay.md) ，並分別 [使用和設定自動播放](autoplay2k-using.md)。</span><span class="sxs-lookup"><span data-stu-id="adfd6-219">For more information about the difference between AutoRun and AutoPlay, see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md) and [Using and Configuring AutoPlay](autoplay2k-using.md), respectively.</span></span>

### <a name="usage-example"></a><span data-ttu-id="adfd6-220">使用範例</span><span class="sxs-lookup"><span data-stu-id="adfd6-220">Usage Example</span></span>

<span data-ttu-id="adfd6-221">CD 包含三個檔案：自動執行 .inf、Readme.txt 和 .wma。</span><span class="sxs-lookup"><span data-stu-id="adfd6-221">A CD contains three files: Autorun.inf, Readme.txt, and Music.wma.</span></span> <span data-ttu-id="adfd6-222">視使用中的 Windows 版本和在 [自動執行] 中指定的選項而定，在插入光碟時，可以透過自動執行或自動播放來處理 CD (假設已為 CD 插入) 的磁片磁碟機啟用 [自動播放/自動播放]。</span><span class="sxs-lookup"><span data-stu-id="adfd6-222">Depending on the version of Windows in use and options specified in Autorun.inf, the CD may be handled by either AutoRun or AutoPlay when it is inserted (assuming AutoRun/AutoPlay is enabled for the drive into which the CD is inserted).</span></span>

<span data-ttu-id="adfd6-223">首先，請考慮具有下列內容的執行中 .inf 檔案，請注意未指定 **UseAutoPlay = 1** ：</span><span class="sxs-lookup"><span data-stu-id="adfd6-223">First, consider an Autorun.inf file with the following contents, noting that **UseAutoPlay=1** is not specified:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
```



<span data-ttu-id="adfd6-224">插入此 CD 時，Shell 所採取的動作取決於使用中的 Windows 版本：</span><span class="sxs-lookup"><span data-stu-id="adfd6-224">The action taken by the Shell when this CD is inserted depends on the version of Windows in use:</span></span>

-   <span data-ttu-id="adfd6-225">在 Windows XP 或更早版本上，此 CD 會在插入時由自動播放處理。</span><span class="sxs-lookup"><span data-stu-id="adfd6-225">On Windows XP or earlier, this CD is handled by AutoRun when it is inserted.</span></span> <span data-ttu-id="adfd6-226">在此情況下，會讀取 **shellexecute** 專案，而且 Shell 會叫用與 .txt 檔案相關聯的檔案處理常式;這通常會在 [記事本] 中開啟 Readme.txt。</span><span class="sxs-lookup"><span data-stu-id="adfd6-226">In this case, the **shellexecute** entry is read, and the Shell invokes the file handler associated with .txt files; typically this would open Readme.txt in Notepad.</span></span>
-   <span data-ttu-id="adfd6-227">在 Windows Vista 中，具有 **shellexecute** 專案的自動播放 .inf 檔案，會將媒體識別為自動播放類型「軟體和遊戲」。</span><span class="sxs-lookup"><span data-stu-id="adfd6-227">On Windows Vista, the presence of an Autorun.inf file with a **shellexecute** entry causes the media to be identified as AutoPlay type "Software and games".</span></span> <span data-ttu-id="adfd6-228">在此情況下，使用者會看到 [自動播放] 對話方塊，其中包含 **shellexecute** 專案所指定的動作 (在對話方塊中顯示為 [載入 Readme.txt]) ，以及與 [軟體和遊戲] 類型的媒體相關聯的預設動作。</span><span class="sxs-lookup"><span data-stu-id="adfd6-228">In this case the user is presented with an AutoPlay dialog that includes the action specified by the **shellexecute** entry (presented as "Load Readme.txt" in the dialog), along with default actions associated with media of type "Software and games".</span></span>

<span data-ttu-id="adfd6-229">若要指出應該使用 [自動播放]，而不是在 Windows XP 上執行，而且應該在 Windows Vista 上的 [自動播放] 對話方塊中隱藏 [自動執行 shellexecute] 專案指定的動作，請將 **UseAutoPlay** 插入至 [自動執行 .inf] 檔案，如下所示：</span><span class="sxs-lookup"><span data-stu-id="adfd6-229">To indicate that AutoPlay should be used rather than AutoRun on Windows XP, and that the action specified by the AutoRun shellexecute entry should be suppressed from the AutoPlay dialog on Windows Vista, insert **UseAutoPlay** into the Autorun.inf file as follows:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



<span data-ttu-id="adfd6-230">同樣地，當插入此 CD 時，Shell 所採取的動作會視使用中的 Windows 版本而定。</span><span class="sxs-lookup"><span data-stu-id="adfd6-230">Once again, the action taken by the Shell when this CD is inserted depends on the version of Windows in use.</span></span>

-   <span data-ttu-id="adfd6-231">在 Windows XP 之前的 Windows 版本中，仍會使用自動執行，並執行 **shellexecute** 所指定的動作（如先前所述）。</span><span class="sxs-lookup"><span data-stu-id="adfd6-231">On versions of Windows earlier than Windows XP, AutoRun is still used and the action specified by **shellexecute** is performed, as described previously.</span></span> <span data-ttu-id="adfd6-232"> (請注意，windows XP 之前的 Windows 版本只會提供自動執行時間。 ) </span><span class="sxs-lookup"><span data-stu-id="adfd6-232">(Note that only AutoRun is available on versions of Windows earlier than Windows XP.)</span></span>
-   <span data-ttu-id="adfd6-233">在 Windows XP 上， **UseAutoPlay** 專案會導致自動播放用來取代自動播放。</span><span class="sxs-lookup"><span data-stu-id="adfd6-233">On Windows XP, the **UseAutoPlay** entry causes AutoPlay to be used in place of AutoRun.</span></span> <span data-ttu-id="adfd6-234">在此情況下，自動播放會判斷媒體包含 Windows Media 音訊 ( .wma) 檔案，並將內容分類為「音樂檔案」。</span><span class="sxs-lookup"><span data-stu-id="adfd6-234">In this case, AutoPlay determines that the media contains a Windows Media Audio (.wma) file and categorizes the content as "Music files".</span></span> <span data-ttu-id="adfd6-235">使用者會看到 [自動播放] 對話方塊，其中包含「音樂檔案」自動播放媒體類型的已註冊處理常式。自動運行 shellexecute 專案會被忽略。</span><span class="sxs-lookup"><span data-stu-id="adfd6-235">The user is presented with an AutoPlay dialog containing registered handlers for the "Music files" AutoPlay media type; the AutoRun shellexecute entry is ignored.</span></span>

### <a name="shellexecute"></a><span data-ttu-id="adfd6-236">shellexecute</span><span class="sxs-lookup"><span data-stu-id="adfd6-236">shellexecute</span></span>

[<span data-ttu-id="adfd6-237">版本5.0。</span><span class="sxs-lookup"><span data-stu-id="adfd6-237">Version 5.0.</span></span>](versions.md) <span data-ttu-id="adfd6-238">**Shellexecute** 專案會指定自動執行將用來呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)的應用程式或資料檔案。</span><span class="sxs-lookup"><span data-stu-id="adfd6-238">The **shellexecute** entry specifies an application or data file that AutoRun will use to call [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a><span data-ttu-id="adfd6-239">參數</span><span class="sxs-lookup"><span data-stu-id="adfd6-239">Parameters</span></span>

-   <span data-ttu-id="adfd6-240">*filepath*</span><span class="sxs-lookup"><span data-stu-id="adfd6-240">*filepath*</span></span>

    <span data-ttu-id="adfd6-241">字串，包含包含資料或可執行檔之目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="adfd6-241">A string that contains the fully qualified path of the directory that contains the data or executable file.</span></span> <span data-ttu-id="adfd6-242">如果未指定路徑，則檔案必須位於磁片磁碟機的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="adfd6-242">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="adfd6-243">*filename*</span><span class="sxs-lookup"><span data-stu-id="adfd6-243">*filename*</span></span>

    <span data-ttu-id="adfd6-244">字串，其中包含檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="adfd6-244">A string that contains the file's name.</span></span> <span data-ttu-id="adfd6-245">如果是可執行檔，則會啟動它。</span><span class="sxs-lookup"><span data-stu-id="adfd6-245">If it is an executable file, it is launched.</span></span> <span data-ttu-id="adfd6-246">如果它是資料檔案，它必須是 [檔案類型](fa-file-types.md)的成員。</span><span class="sxs-lookup"><span data-stu-id="adfd6-246">If it is a data file, it must be a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="adfd6-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 會啟動與檔案類型相關聯的預設命令。</span><span class="sxs-lookup"><span data-stu-id="adfd6-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) launches the default command associated with the file type.</span></span>

-   <span data-ttu-id="adfd6-248">*paramx*</span><span class="sxs-lookup"><span data-stu-id="adfd6-248">*paramx*</span></span>

    <span data-ttu-id="adfd6-249">包含應傳遞給 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)的任何其他參數。</span><span class="sxs-lookup"><span data-stu-id="adfd6-249">Contains any additional parameters that should be passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

### <a name="remarks"></a><span data-ttu-id="adfd6-250">備註</span><span class="sxs-lookup"><span data-stu-id="adfd6-250">Remarks</span></span>

<span data-ttu-id="adfd6-251">此專案類似于 [開啟](#parameters)，但它可讓您使用檔案 [關聯](fa-intro.md) 資訊來執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="adfd6-251">This entry is similar to [open](#parameters), but it allows you to use [file association](fa-intro.md) information to run the application.</span></span>

### <a name="shell"></a><span data-ttu-id="adfd6-252">殼層</span><span class="sxs-lookup"><span data-stu-id="adfd6-252">shell</span></span>

<span data-ttu-id="adfd6-253">**Shell** 專案會指定磁片磁碟機快捷方式功能表的預設命令。</span><span class="sxs-lookup"><span data-stu-id="adfd6-253">The **shell** entry specifies a default command for the drive's shortcut menu.</span></span>


```
shell=verb
```



### <a name="parameters"></a><span data-ttu-id="adfd6-254">參數</span><span class="sxs-lookup"><span data-stu-id="adfd6-254">Parameters</span></span>

-   <span data-ttu-id="adfd6-255">*動詞命令*</span><span class="sxs-lookup"><span data-stu-id="adfd6-255">*verb*</span></span>

    <span data-ttu-id="adfd6-256">對應至功能表命令的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="adfd6-256">The verb that corresponds to the menu command.</span></span> <span data-ttu-id="adfd6-257">動詞和其相關聯的功能表命令必須在具有 [shell \\ 動詞](#shellverb) 專案的 [自動播放] 檔案中定義。</span><span class="sxs-lookup"><span data-stu-id="adfd6-257">The verb and its associated menu command must be defined in the Autorun.inf file with a [shell\\verb](#shellverb) entry.</span></span>

### <a name="remarks"></a><span data-ttu-id="adfd6-258">備註</span><span class="sxs-lookup"><span data-stu-id="adfd6-258">Remarks</span></span>

<span data-ttu-id="adfd6-259">當使用者以滑鼠右鍵按一下磁片磁碟機圖示時，會出現快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="adfd6-259">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="adfd6-260">如果有執行中的 .inf 檔案，則會從它取得預設快捷方式功能表命令。</span><span class="sxs-lookup"><span data-stu-id="adfd6-260">If an Autorun.inf file is present, the default shortcut menu command is taken from it.</span></span> <span data-ttu-id="adfd6-261">當使用者按兩下磁片磁碟機的圖示時，也會執行此命令。</span><span class="sxs-lookup"><span data-stu-id="adfd6-261">This command also executes when the user double-clicks the drive's icon.</span></span>

<span data-ttu-id="adfd6-262">若要指定預設快捷方式功能表命令，請先使用 [shell \\ 動詞](#shellverb)來定義其動詞命令、命令字串和功能表文字。</span><span class="sxs-lookup"><span data-stu-id="adfd6-262">To specify the default shortcut menu command, first define its verb, command string, and menu text with [shell\\verb](#shellverb).</span></span> <span data-ttu-id="adfd6-263">然後使用 shell 將它設為預設快捷方式功能表命令。</span><span class="sxs-lookup"><span data-stu-id="adfd6-263">Then use shell to make it the default shortcut menu command.</span></span> <span data-ttu-id="adfd6-264">否則，預設的功能表項目文字會是「自動播放」，這會啟動 [開啟](#parameters) 專案所指定的應用程式。</span><span class="sxs-lookup"><span data-stu-id="adfd6-264">Otherwise, the default menu item text will be "AutoPlay", which launches the application specified by the [open](#parameters) entry.</span></span>

### <a name="shellverb"></a><span data-ttu-id="adfd6-265">shell \\ 動詞</span><span class="sxs-lookup"><span data-stu-id="adfd6-265">shell\\verb</span></span>

<span data-ttu-id="adfd6-266">**Shell \\ 動詞** 專案會將自訂命令新增至磁片磁碟機的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="adfd6-266">The **shell\\verb** entry adds a custom command to the drive's shortcut menu.</span></span>


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a><span data-ttu-id="adfd6-267">參數</span><span class="sxs-lookup"><span data-stu-id="adfd6-267">Parameters</span></span>

-   <span data-ttu-id="adfd6-268">*動詞命令*</span><span class="sxs-lookup"><span data-stu-id="adfd6-268">*verb*</span></span>

    <span data-ttu-id="adfd6-269">功能表命令的動詞。</span><span class="sxs-lookup"><span data-stu-id="adfd6-269">The menu command's verb.</span></span> <span data-ttu-id="adfd6-270">**Shell \\**_動詞_*_\\ 命令_* 專案會將動詞與可執行檔產生關聯。</span><span class="sxs-lookup"><span data-stu-id="adfd6-270">The **shell\\**_verb_*_\\command_* entry associates the verb with an executable file.</span></span> <span data-ttu-id="adfd6-271">動詞不能包含內嵌的空格。</span><span class="sxs-lookup"><span data-stu-id="adfd6-271">Verbs must not contain embedded spaces.</span></span> <span data-ttu-id="adfd6-272">依預設， *動詞* 是顯示在快捷方式功能表中的文字。</span><span class="sxs-lookup"><span data-stu-id="adfd6-272">By default, *verb* is the text that is displayed in the shortcut menu.</span></span>

-   <span data-ttu-id="adfd6-273">*Filename.exe*</span><span class="sxs-lookup"><span data-stu-id="adfd6-273">*Filename.exe*</span></span>

    <span data-ttu-id="adfd6-274">執行動作之應用程式的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="adfd6-274">The path and file name of the application that performs the action.</span></span>

-   <span data-ttu-id="adfd6-275">*MenuText*</span><span class="sxs-lookup"><span data-stu-id="adfd6-275">*MenuText*</span></span>

    <span data-ttu-id="adfd6-276">此參數會指定快捷方式功能表中顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="adfd6-276">This parameter specifies the text that is displayed in the shortcut menu.</span></span> <span data-ttu-id="adfd6-277">如果省略，則會顯示 *動詞* 。</span><span class="sxs-lookup"><span data-stu-id="adfd6-277">If it is omitted, *verb* is displayed.</span></span> <span data-ttu-id="adfd6-278">*MenuText* 可以是混合大小寫，而且可以包含空格。</span><span class="sxs-lookup"><span data-stu-id="adfd6-278">*MenuText* can be mixed-case and can contain spaces.</span></span> <span data-ttu-id="adfd6-279">您可以藉由在字母前面加上連字號 (&) ，來設定功能表項目的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="adfd6-279">You can set a shortcut key for the menu item by putting an ampersand (&) in front of the letter.</span></span>

### <a name="remarks"></a><span data-ttu-id="adfd6-280">備註</span><span class="sxs-lookup"><span data-stu-id="adfd6-280">Remarks</span></span>

<span data-ttu-id="adfd6-281">當使用者以滑鼠右鍵按一下磁片磁碟機圖示時，會出現快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="adfd6-281">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="adfd6-282">將 **shell \\ 動詞** 命令新增至磁片磁碟機的 [自動播放] .inf 檔案，可讓您將命令新增到這個快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="adfd6-282">Adding **shell\\verb** entries to the drive's Autorun.inf file allows you to add commands to this shortcut menu.</span></span>

<span data-ttu-id="adfd6-283">此專案有兩個部分，必須位於不同的行。</span><span class="sxs-lookup"><span data-stu-id="adfd6-283">There are two parts to this entry, which must be on separate lines.</span></span> <span data-ttu-id="adfd6-284">第一個部分是 **shell \\**_動詞_*_\\ 命令_*。</span><span class="sxs-lookup"><span data-stu-id="adfd6-284">The first part is **shell\\**_verb_*_\\command_*.</span></span> <span data-ttu-id="adfd6-285">此為必要。</span><span class="sxs-lookup"><span data-stu-id="adfd6-285">It is required.</span></span> <span data-ttu-id="adfd6-286">它會將名為 *動詞* 的字串與在命令執行時啟動的應用程式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="adfd6-286">It associates a string, called a *verb*, with the application to launch when the command runs.</span></span> <span data-ttu-id="adfd6-287">第二個部分是 **shell \\**_動詞_ 專案。</span><span class="sxs-lookup"><span data-stu-id="adfd6-287">The second part is the **shell\\**_verb_ entry.</span></span> <span data-ttu-id="adfd6-288">此為選用項目。</span><span class="sxs-lookup"><span data-stu-id="adfd6-288">It is optional.</span></span> <span data-ttu-id="adfd6-289">您可以將它包含在快捷方式功能表中，以指定顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="adfd6-289">You can include it to specify the text that displays in the shortcut menu.</span></span>

<span data-ttu-id="adfd6-290">若要指定預設的快捷方式功能表命令，請使用 **shell \\ 動詞** 來定義動詞，並使其成為具有 [shell](#autoruninf-entries) 專案的預設命令。</span><span class="sxs-lookup"><span data-stu-id="adfd6-290">To specify a default shortcut menu command, define the verb with **shell\\verb**, and make it the default command with the [shell](#autoruninf-entries) entry.</span></span>

<span data-ttu-id="adfd6-291">下列範例自動執行 .inf 片段會將 *readit* 動詞與命令字串 "Notepad abc \\readme.txt" 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="adfd6-291">The following sample Autorun.inf fragment associates the *readit* verb with the command string "Notepad abc\\readme.txt".</span></span> <span data-ttu-id="adfd6-292">功能表文字是「自述我」，而「」是定義為專案的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="adfd6-292">The menu text is "Read Me", and 'M' is defined as the item's shortcut key.</span></span> <span data-ttu-id="adfd6-293">當使用者選取此命令時， \\ 會使用 Microsoft 記事本開啟磁片磁碟機的 abcreadme.txt 檔。</span><span class="sxs-lookup"><span data-stu-id="adfd6-293">When the user selects this command, the drive's abc\\readme.txt file opens with Microsoft Notepad.</span></span>


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a><span data-ttu-id="adfd6-294">\[內容 \] 金鑰</span><span class="sxs-lookup"><span data-stu-id="adfd6-294">\[Content\] Keys</span></span>

<span data-ttu-id="adfd6-295">有三種檔案類型金鑰： **MusicFiles**、 **PictureFiles** 和 **VideoFiles**。</span><span class="sxs-lookup"><span data-stu-id="adfd6-295">There are three file type keys: **MusicFiles**, **PictureFiles**, and **VideoFiles**.</span></span>

<span data-ttu-id="adfd6-296">如果其中一項內容是透過不區分大小寫的值1、y、yes、t 或 true 來設定為 true，則不論媒體上是否存在該類型的內容，自動播放 UI 都會顯示與該內容類型相關聯的處理常式。</span><span class="sxs-lookup"><span data-stu-id="adfd6-296">If one of these contents is set to true through one the case-insensitive values 1, y, yes, t, or true, the Autoplay UI displays the handlers associated with that content type regardless of whether content of that type exists on the media.</span></span>

<span data-ttu-id="adfd6-297">如果其中一項內容是透過不區分大小寫值0、n、否、f 或 false 的值設定為 false，則即使在媒體上偵測到該類型的內容，自動播放 UI 也不會顯示與該內容類型相關聯的處理常式。</span><span class="sxs-lookup"><span data-stu-id="adfd6-297">If one of these contents is set to false through one the case-insensitive values 0, n, no, f, or false, the Autoplay UI does not display the handlers associated with that content type even if content of that type is detected on the media.</span></span>

<span data-ttu-id="adfd6-298">使用本節的目的是要讓內容作者能夠將內容意圖傳達給自動播放。</span><span class="sxs-lookup"><span data-stu-id="adfd6-298">Use of this section is intended to allow content authors to communicate the intent of content to Autoplay.</span></span> <span data-ttu-id="adfd6-299">比方說，CD 可以歸類為只包含音樂內容，即使它也有圖片和影片，也會被視為具有混合的內容。</span><span class="sxs-lookup"><span data-stu-id="adfd6-299">For instance, a CD can be categorized as containing only music content even though it also has pictures and videos and would otherwise be seen as having mixed content.</span></span>

<span data-ttu-id="adfd6-300">只有在 Windows Vista 和更新版本中才支援 [ **\[ 內容 \]** ] 區段。</span><span class="sxs-lookup"><span data-stu-id="adfd6-300">The **\[Content\]** section is only supported under Windows Vista and later.</span></span>


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a><span data-ttu-id="adfd6-301">\[ExclusiveContentPaths 索引 \] 鍵</span><span class="sxs-lookup"><span data-stu-id="adfd6-301">\[ExclusiveContentPaths\] Keys</span></span>

<span data-ttu-id="adfd6-302">本節所列的資料夾限制自動播放只搜尋這些資料夾及其內容的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="adfd6-302">Folders listed in this section limit Autoplay to searching only those folders and their subfolders for content.</span></span> <span data-ttu-id="adfd6-303">您可以使用或不使用前置反斜線 () 來提供它們 \\ 。</span><span class="sxs-lookup"><span data-stu-id="adfd6-303">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="adfd6-304">在任一種情況下，都會從媒體的根目錄取得絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="adfd6-304">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="adfd6-305">如果資料夾的名稱中有空格，請勿用引號括住，因為引號會以文字形式放在路徑的一部分。</span><span class="sxs-lookup"><span data-stu-id="adfd6-305">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="adfd6-306">使用本節的目的是要讓內容作者能夠將內容意圖傳達給自動播放，並藉由將掃描限制在媒體的某些重要區域，縮短掃描時間。</span><span class="sxs-lookup"><span data-stu-id="adfd6-306">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="adfd6-307">以下是所有有效的路徑</span><span class="sxs-lookup"><span data-stu-id="adfd6-307">The following are all valid paths</span></span>


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="adfd6-308">只有在 Windows Vista 和更新版本下才支援 **\[ ExclusiveContentPaths \]** 區段。</span><span class="sxs-lookup"><span data-stu-id="adfd6-308">The **\[ExclusiveContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="ignorecontentpaths-keys"></a><span data-ttu-id="adfd6-309">\[IgnoreContentPaths 索引 \] 鍵</span><span class="sxs-lookup"><span data-stu-id="adfd6-309">\[IgnoreContentPaths\] Keys</span></span>

<span data-ttu-id="adfd6-310">在搜尋內容的媒體時，自動播放會忽略此區段中所列的資料夾及其子資料夾。</span><span class="sxs-lookup"><span data-stu-id="adfd6-310">Folders listed in this section, and their subfolders, are ignored by Autoplay when searching a media for content.</span></span> <span data-ttu-id="adfd6-311">您可以使用或不使用前置反斜線 () 來提供它們 \\ 。</span><span class="sxs-lookup"><span data-stu-id="adfd6-311">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="adfd6-312">在任一種情況下，都會從媒體的根目錄取得絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="adfd6-312">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="adfd6-313">如果資料夾的名稱中有空格，請勿用引號括住，因為引號會以文字形式放在路徑的一部分。</span><span class="sxs-lookup"><span data-stu-id="adfd6-313">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="adfd6-314">本節中的路徑優先于 **\[ ExclusiveContentPaths \]** 區段中的路徑。</span><span class="sxs-lookup"><span data-stu-id="adfd6-314">Paths in this section take precedence over paths in the **\[ExclusiveContentPaths\]** section.</span></span> <span data-ttu-id="adfd6-315">如果 **\[ IgnoreContentPaths \]** 中提供的路徑是 **\[ ExclusiveContentPaths \]** 中指定之路徑的子資料夾，它仍會被忽略。</span><span class="sxs-lookup"><span data-stu-id="adfd6-315">If a path given in **\[IgnoreContentPaths\]** is a subfolder of a path given in **\[ExclusiveContentPaths\]**, it is still ignored.</span></span>

<span data-ttu-id="adfd6-316">使用本節的目的是要讓內容作者能夠將內容意圖傳達給自動播放，並藉由將掃描限制在媒體的某些重要區域，縮短掃描時間。</span><span class="sxs-lookup"><span data-stu-id="adfd6-316">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="adfd6-317">以下是所有有效的路徑</span><span class="sxs-lookup"><span data-stu-id="adfd6-317">The following are all valid paths</span></span>


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="adfd6-318">只有在 Windows Vista 和更新版本下才支援 **\[ IgnoreContentPaths \]** 區段。</span><span class="sxs-lookup"><span data-stu-id="adfd6-318">The **\[IgnoreContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="deviceinstall-keys"></a><span data-ttu-id="adfd6-319">\[DeviceInstall 索引 \] 鍵</span><span class="sxs-lookup"><span data-stu-id="adfd6-319">\[DeviceInstall\] Keys</span></span>

### <a name="driverpath"></a><span data-ttu-id="adfd6-320">DriverPath</span><span class="sxs-lookup"><span data-stu-id="adfd6-320">DriverPath</span></span>

<span data-ttu-id="adfd6-321">**DriverPath** 專案會指定要以遞迴方式搜尋驅動程式檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="adfd6-321">The **DriverPath** entry specifies a directory to search recursively for driver files.</span></span> <span data-ttu-id="adfd6-322">此命令是在驅動程式安裝期間使用，不是自動執行操作的一部分。</span><span class="sxs-lookup"><span data-stu-id="adfd6-322">This command is used during a driver installation and is not part of an AutoRun operation.</span></span> <span data-ttu-id="adfd6-323">只有在 Windows XP 下才支援 **\[ DeviceInstall \]** 區段。</span><span class="sxs-lookup"><span data-stu-id="adfd6-323">The **\[DeviceInstall\]** section is only supported under Windows XP.</span></span>


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a><span data-ttu-id="adfd6-324">參數</span><span class="sxs-lookup"><span data-stu-id="adfd6-324">Parameters</span></span>

-   <span data-ttu-id="adfd6-325">*directorypath*</span><span class="sxs-lookup"><span data-stu-id="adfd6-325">*directorypath*</span></span>

    <span data-ttu-id="adfd6-326">Windows 搜尋驅動程式檔案的目錄路徑，以及其所有子目錄。</span><span class="sxs-lookup"><span data-stu-id="adfd6-326">A path to a directory that Windows searches for driver files, along with all of its subdirectories.</span></span>

### <a name="remarks"></a><span data-ttu-id="adfd6-327">備註</span><span class="sxs-lookup"><span data-stu-id="adfd6-327">Remarks</span></span>

<span data-ttu-id="adfd6-328">請勿在 *directorypath* 中使用磁碟機號，因為它們會從一部電腦變更為下一部電腦。</span><span class="sxs-lookup"><span data-stu-id="adfd6-328">Do not use drive letters in *directorypath* as they change from one computer to the next.</span></span>

<span data-ttu-id="adfd6-329">若要搜尋多個目錄，請在此範例中新增每個目錄的 **DriverPath** 專案。</span><span class="sxs-lookup"><span data-stu-id="adfd6-329">To search multiple directories, add a **DriverPath** entry for each directory as in this example.</span></span>


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



<span data-ttu-id="adfd6-330">如果 **\[ DeviceInstall \]** 區段中未提供任何 **DriverPath** 專案，或 **DriverPath** 專案沒有值，則會在搜尋驅動程式檔案期間略過該磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="adfd6-330">If no **DriverPath** entry is provided in the **\[DeviceInstall\]** section or the **DriverPath** entry has no value, then that drive is skipped during a search for driver files.</span></span>

 

 
