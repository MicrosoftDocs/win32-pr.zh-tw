---
title: 資料夾監控登錄設定
description: 資料夾監控登錄設定
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player，資料夾監控登錄設定
- Windows Media Player，檔案資料夾監控登錄設定
- Windows Media Player，登錄
- 登錄，資料夾監控設定
- 登錄，檔案資料夾監控設定
- 登錄，Windows Media Player 的設定
- 資料夾監控登錄設定
- 檔案資料夾監控登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383089"
---
# <a name="folder-monitoring-registry-settings"></a><span data-ttu-id="8799c-111">資料夾監控登錄設定</span><span class="sxs-lookup"><span data-stu-id="8799c-111">Folder Monitoring Registry Settings</span></span>

<span data-ttu-id="8799c-112">Windows Media Player 9 系列或更新版本可以監視新數位媒體檔案的檔案資料夾。</span><span class="sxs-lookup"><span data-stu-id="8799c-112">Windows Media Player 9 Series or later can monitor file folders for new digital media files.</span></span> <span data-ttu-id="8799c-113">當播放玩家偵測到受監視資料夾中的新檔案時，它會自動將檔案新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="8799c-113">When the Player detects a new file in a monitored folder, it automatically adds the file to the library.</span></span> <span data-ttu-id="8799c-114">在 Windows Media Player 9 到 Windows Media Player 11 中，使用者可以在 [**選項**] 對話方塊的 [媒體櫃] 索引標籤上，按一下 [**監視資料夾**] 來變更受監視的資料夾清單。</span><span class="sxs-lookup"><span data-stu-id="8799c-114">For Windows Media Player 9 through Windows Media Player 11, users can change the list of monitored folders by clicking **Monitor Folders** on the library tab of the **Options** dialog box.</span></span> <span data-ttu-id="8799c-115">針對 Windows Media Player 12，使用者可以依照主題 [將專案新增至 Windows Media Player 程式庫](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library)中的指示，來變更受監視資料夾的清單。</span><span class="sxs-lookup"><span data-stu-id="8799c-115">For Windows Media Player 12, a user can change the list of monitored folders by following the instructions in the topic [Add items to the Windows Media Player Library](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span></span> <span data-ttu-id="8799c-116">針對 Windows Media Player 9 到 Windows Media Player 11，您可以透過將值新增至登錄，以程式設計方式新增要監視的資料夾。</span><span class="sxs-lookup"><span data-stu-id="8799c-116">For Windows Media Player 9 through Windows Media Player 11, you can programmatically add a folder to be monitored by adding a value to the registry.</span></span> <span data-ttu-id="8799c-117">針對 Windows Media Player 12，您無法使用登錄，以程式設計方式新增或移除要監視的資料夾。</span><span class="sxs-lookup"><span data-stu-id="8799c-117">For Windows Media Player 12, you cannot use the registry to programmatically add or remove folders to be monitored.</span></span>

<span data-ttu-id="8799c-118">針對 Windows Media Player 9 到 Windows Media Player 11]，若要新增要監視的資料夾，您必須先在下列登錄機碼中建立或修改兩個值：</span><span class="sxs-lookup"><span data-stu-id="8799c-118">For Windows Media Player 9 through Windows Media Player 11, to add a folder for monitoring you must first create or modify two values in the following registry key:</span></span>

<span data-ttu-id="8799c-119">**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ 喜好設定\\**</span><span class="sxs-lookup"><span data-stu-id="8799c-119">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Preferences\\**</span></span>

<span data-ttu-id="8799c-120">新的值必須命名如下。</span><span class="sxs-lookup"><span data-stu-id="8799c-120">The new values must be named as follows.</span></span>



| <span data-ttu-id="8799c-121">名稱</span><span class="sxs-lookup"><span data-stu-id="8799c-121">Name</span></span>                           | <span data-ttu-id="8799c-122">類型</span><span class="sxs-lookup"><span data-stu-id="8799c-122">Type</span></span>           | <span data-ttu-id="8799c-123">Description</span><span class="sxs-lookup"><span data-stu-id="8799c-123">Description</span></span>                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8799c-124">**TrackFoldersDirectories**</span><span class="sxs-lookup"><span data-stu-id="8799c-124">**TrackFoldersDirectories**</span></span>    | <span data-ttu-id="8799c-125">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8799c-125">**REG\_DWORD**</span></span> | <span data-ttu-id="8799c-126">**DWORD** 值，表示要監視的資料夾計數。</span><span class="sxs-lookup"><span data-stu-id="8799c-126">A **DWORD** value that represents the count of folders to monitor.</span></span> <span data-ttu-id="8799c-127">這必須符合 \**TrackFoldersDirectories \* \* X* 值的計數。</span><span class="sxs-lookup"><span data-stu-id="8799c-127">This must match the count of \**TrackFoldersDirectories\*\*\*X* values.</span></span>                                                                                                                                         |
| <span data-ttu-id="8799c-128">\**TrackFoldersDirectories \* \* \* X*</span><span class="sxs-lookup"><span data-stu-id="8799c-128">\**TrackFoldersDirectories\*\*\*X*</span></span> | <span data-ttu-id="8799c-129">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="8799c-129">**REG\_SZ**</span></span>    | <span data-ttu-id="8799c-130">字串值，表示要監視的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="8799c-130">A string value that represents the path of the folder to monitor.</span></span> <span data-ttu-id="8799c-131">要監視的每個資料夾都需要個別的值。</span><span class="sxs-lookup"><span data-stu-id="8799c-131">Each folder to monitor requires a separate value.</span></span> <span data-ttu-id="8799c-132">尾碼 *X* 是一個整數，應一律從0開始，然後以1遞增。</span><span class="sxs-lookup"><span data-stu-id="8799c-132">The suffix *X* is an integer that should always begin at 0 and then increment by 1.</span></span> <span data-ttu-id="8799c-133">Windows Media Player 也會監視指定資料夾的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="8799c-133">Windows Media Player also monitors subfolders of the specified folder.</span></span> |



 

<span data-ttu-id="8799c-134">例如，若要新增第一個要監視的資料夾，請新增下列值：</span><span class="sxs-lookup"><span data-stu-id="8799c-134">For example, to add the first folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



<span data-ttu-id="8799c-135">然後，建立計數值：</span><span class="sxs-lookup"><span data-stu-id="8799c-135">Then, create the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



<span data-ttu-id="8799c-136">若要新增第二個要監視的資料夾，請新增下列值：</span><span class="sxs-lookup"><span data-stu-id="8799c-136">To add a second folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



<span data-ttu-id="8799c-137">然後，將計數值遞增：</span><span class="sxs-lookup"><span data-stu-id="8799c-137">Then, increment the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a><span data-ttu-id="8799c-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="8799c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8799c-139">**登錄設定**</span><span class="sxs-lookup"><span data-stu-id="8799c-139">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




