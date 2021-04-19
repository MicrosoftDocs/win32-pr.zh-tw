---
title: 程式庫分類登錄專案
description: 程式庫分類登錄專案
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows Media Player，程式庫
- Windows Media Player，分類登錄專案
- Windows Media Player、副檔名
- Windows Media Player，登錄
- 登錄、副檔名
- 登錄，程式庫分類專案
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
- 程式庫，分類登錄專案
- 程式庫，登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965180"
---
# <a name="library-classification-registry-entries"></a><span data-ttu-id="c3633-113">程式庫分類登錄專案</span><span class="sxs-lookup"><span data-stu-id="c3633-113">Library Classification Registry Entries</span></span>

<span data-ttu-id="c3633-114">當 Windows Media Player 遇到具有自訂副檔名的媒體檔案時，它並不知道檔案是否應分類為音訊、影片或其他類型。</span><span class="sxs-lookup"><span data-stu-id="c3633-114">When Windows Media Player encounters a media file that has a custom file name extension, it does not know whether the file should be classified as audio, video, or some other type.</span></span> <span data-ttu-id="c3633-115">根據預設，Windows Media Player 會將這些檔案放在程式庫的其他媒體部分。</span><span class="sxs-lookup"><span data-stu-id="c3633-115">By default, Windows Media Player places such files in the Other Media portion of the library.</span></span>

<span data-ttu-id="c3633-116">如果您的數位媒體檔案有自訂格式，您可以在使用者電腦上的登錄中放入兩個專案，以提供 Windows Media Player 的資訊，告訴您檔案在播放程式媒體櫃中的顯示位置。</span><span class="sxs-lookup"><span data-stu-id="c3633-116">If your digital media files have a custom format, you can provide Windows Media Player with information about where your files should appear in the Player's library by placing two entries in the registry on the user's computer.</span></span>

<span data-ttu-id="c3633-117">其中一個專案會進入下列子機碼。</span><span class="sxs-lookup"><span data-stu-id="c3633-117">One entry goes in the following subkey.</span></span>

<span data-ttu-id="c3633-118">**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**</span><span class="sxs-lookup"><span data-stu-id="c3633-118">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="c3633-119">登錄專案具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="c3633-119">The registry entry has the following format.</span></span>



| <span data-ttu-id="c3633-120">Name</span><span class="sxs-lookup"><span data-stu-id="c3633-120">Name</span></span>                                                  | <span data-ttu-id="c3633-121">資料類型</span><span class="sxs-lookup"><span data-stu-id="c3633-121">Data type</span></span>   | <span data-ttu-id="c3633-122">值</span><span class="sxs-lookup"><span data-stu-id="c3633-122">Value</span></span>                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| <span data-ttu-id="c3633-123">沒有句點 ( 的副檔名 ) 分隔符號</span><span class="sxs-lookup"><span data-stu-id="c3633-123">The file name extension without the dot (.) separator</span></span> | <span data-ttu-id="c3633-124">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="c3633-124">**REG\_SZ**</span></span> | <span data-ttu-id="c3633-125">指定程式庫位置的字串</span><span class="sxs-lookup"><span data-stu-id="c3633-125">A string that specifies a library location</span></span> |



 

<span data-ttu-id="c3633-126">另一個登錄專案會進入您所建立的下列子機碼。</span><span class="sxs-lookup"><span data-stu-id="c3633-126">The other registry entry goes in the following subkey that you create.</span></span>

<span data-ttu-id="c3633-127">**HKEY \_類別 \_ 根 \\** *customExtension*</span><span class="sxs-lookup"><span data-stu-id="c3633-127">**HKEY\_CLASSES\_ROOT\\** *customExtension*</span></span>

<span data-ttu-id="c3633-128">其中 *customExtension* 是副檔名，包括點 (. ) 分隔符號。</span><span class="sxs-lookup"><span data-stu-id="c3633-128">where *customExtension* is the file name extension including the dot (.) separator.</span></span>

<span data-ttu-id="c3633-129">登錄專案具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="c3633-129">The registry entry has the following format.</span></span>



| <span data-ttu-id="c3633-130">Name</span><span class="sxs-lookup"><span data-stu-id="c3633-130">Name</span></span>          | <span data-ttu-id="c3633-131">資料類型</span><span class="sxs-lookup"><span data-stu-id="c3633-131">Data type</span></span>   | <span data-ttu-id="c3633-132">值</span><span class="sxs-lookup"><span data-stu-id="c3633-132">Value</span></span>                                      |
|---------------|-------------|--------------------------------------------|
| <span data-ttu-id="c3633-133">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="c3633-133">PerceivedType</span></span> | <span data-ttu-id="c3633-134">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="c3633-134">**REG\_SZ**</span></span> | <span data-ttu-id="c3633-135">指定程式庫位置的字串</span><span class="sxs-lookup"><span data-stu-id="c3633-135">A string that specifies a library location</span></span> |



 

<span data-ttu-id="c3633-136">這兩個登錄專案都必須具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="c3633-136">Both registry entries must have the same value.</span></span> <span data-ttu-id="c3633-137">下表提供可能的值。</span><span class="sxs-lookup"><span data-stu-id="c3633-137">Possible values are given in the following table.</span></span>



| <span data-ttu-id="c3633-138">值</span><span class="sxs-lookup"><span data-stu-id="c3633-138">Value</span></span> | <span data-ttu-id="c3633-139">描述</span><span class="sxs-lookup"><span data-stu-id="c3633-139">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c3633-140">音訊</span><span class="sxs-lookup"><span data-stu-id="c3633-140">audio</span></span> | <span data-ttu-id="c3633-141">具有自訂延伸模組的檔案會出現在文件庫的音樂部分。</span><span class="sxs-lookup"><span data-stu-id="c3633-141">Files that have the custom extension appear in the music portion of the library.</span></span> |
| <span data-ttu-id="c3633-142">影片</span><span class="sxs-lookup"><span data-stu-id="c3633-142">video</span></span> | <span data-ttu-id="c3633-143">具有自訂延伸模組的檔案會出現在文件庫的影片部分。</span><span class="sxs-lookup"><span data-stu-id="c3633-143">Files that have the custom extension appear in the video portion of the library.</span></span> |



 

<span data-ttu-id="c3633-144">例如，下列登錄專案會指定副檔名為的檔案。 xyz 將會出現在文件庫的音樂部分：</span><span class="sxs-lookup"><span data-stu-id="c3633-144">For example, the following registry entries specify that files having the file name extension .xyz will appear in the music portion of the library:</span></span>


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



<span data-ttu-id="c3633-145">請注意，嘗試寫入使用者電腦上登錄的任何程式碼， \_ \_ 只有在目前的使用者具有系統管理許可權時，才可以寫入至 HKEY 本機電腦子樹。</span><span class="sxs-lookup"><span data-stu-id="c3633-145">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="c3633-146">下列 Windows Media Player 版本支援程式庫分類登錄專案。</span><span class="sxs-lookup"><span data-stu-id="c3633-146">Library classification registry entries are supported by the following versions of Windows Media Player.</span></span>

-   <span data-ttu-id="c3633-147">Windows Media Player 9 系列（含修正程式823275）</span><span class="sxs-lookup"><span data-stu-id="c3633-147">Windows Media Player 9 Series with hotfix 823275</span></span>
-   <span data-ttu-id="c3633-148">Windows Media Player 10 和更新版本</span><span class="sxs-lookup"><span data-stu-id="c3633-148">Windows Media Player 10 and later</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3633-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3633-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3633-150">**副檔名登錄設定**</span><span class="sxs-lookup"><span data-stu-id="c3633-150">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




