---
description: 如果檔案、.ini 檔案或快捷方式檔案已安裝到每個使用者的目錄中，ICE91 會張貼警告。
ms.assetid: 1834d841-b1d9-4646-8057-a41dd88310b6
title: ICE91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f5723369c21894817dacbc1755430a31f17199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988938"
---
# <a name="ice91"></a><span data-ttu-id="21a82-103">ICE91</span><span class="sxs-lookup"><span data-stu-id="21a82-103">ICE91</span></span>

<span data-ttu-id="21a82-104">如果檔案、.ini 檔案或快捷方式檔案已安裝到每個使用者的目錄中，ICE91 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="21a82-104">ICE91 posts a warning if a file, .ini file, or shortcut file is installed into a per-user only directory.</span></span> <span data-ttu-id="21a82-105">如果封裝只用于每個使用者 [安裝內容](installation-context.md) 中，而且永遠不會用於個別電腦安裝，則這些警告是無害的。</span><span class="sxs-lookup"><span data-stu-id="21a82-105">These warnings are harmless if the package is only used for installation in the per-user [installation context](installation-context.md) and never used for per-machine installations.</span></span>

<span data-ttu-id="21a82-106">檔案、.ini 檔或個別使用者目錄中的快捷方式會安裝在特定使用者的設定檔中。</span><span class="sxs-lookup"><span data-stu-id="21a82-106">Files, .ini files, or shortcuts in per-user only directories are installed into a particular user's profile.</span></span> <span data-ttu-id="21a82-107">即使使用者設定個別電腦安裝的 [**ALLUSERS**](allusers.md) 屬性、檔案、.ini 檔案或個別使用者目錄中的快捷方式，都不會複製到「所有使用者」設定檔，其他使用者也無法使用。</span><span class="sxs-lookup"><span data-stu-id="21a82-107">Even if the user sets the [**ALLUSERS**](allusers.md) property for a per-machine installations, files, .ini files, or shortcuts in per-user only directories are not copied in to the "All Users" profile and are not available to other users.</span></span> <span data-ttu-id="21a82-108">每個使用者唯一的目錄不會與 **ALLUSERS** 屬性不同。</span><span class="sxs-lookup"><span data-stu-id="21a82-108">The per-user only directories do not vary with the **ALLUSERS** property.</span></span> <span data-ttu-id="21a82-109">以下是每個使用者的唯一目錄清單：</span><span class="sxs-lookup"><span data-stu-id="21a82-109">The following is a list of the per-user only directories:</span></span>

-   <span data-ttu-id="21a82-110">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-110">AppDataFolder</span></span>
-   <span data-ttu-id="21a82-111">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-111">FavoritesFolder</span></span>
-   <span data-ttu-id="21a82-112">NetHoodFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-112">NetHoodFolder</span></span>
-   <span data-ttu-id="21a82-113">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-113">PersonalFolder</span></span>
-   <span data-ttu-id="21a82-114">PrintHoodFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-114">PrintHoodFolder</span></span>
-   <span data-ttu-id="21a82-115">RecentFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-115">RecentFolder</span></span>
-   <span data-ttu-id="21a82-116">SendToFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-116">SendToFolder</span></span>
-   <span data-ttu-id="21a82-117">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-117">MyPicturesFolder</span></span>
-   <span data-ttu-id="21a82-118">LocalAppDataFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-118">LocalAppDataFolder</span></span>

## <a name="result"></a><span data-ttu-id="21a82-119">結果</span><span class="sxs-lookup"><span data-stu-id="21a82-119">Result</span></span>

<span data-ttu-id="21a82-120">ICE91 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="21a82-120">ICE91 posts the following warnings.</span></span>



| <span data-ttu-id="21a82-121">ICE91 警告</span><span class="sxs-lookup"><span data-stu-id="21a82-121">ICE91 warning</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="21a82-122">Description</span><span class="sxs-lookup"><span data-stu-id="21a82-122">Description</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21a82-123">檔案 ' \[ 1 \] ' 將會安裝到每個使用者目錄 ' \[ 2 \] '，而不會因 [**ALLUSERS**](allusers.md) 值而不同。</span><span class="sxs-lookup"><span data-stu-id="21a82-123">The file '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="21a82-124">此檔案不會複製到每個使用者的設定檔中，即使需要每一部電腦安裝也一樣。</span><span class="sxs-lookup"><span data-stu-id="21a82-124">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>     | <span data-ttu-id="21a82-125">檔案會安裝到每個使用者的目錄中。</span><span class="sxs-lookup"><span data-stu-id="21a82-125">The file is installed into a per-user only directory.</span></span> <span data-ttu-id="21a82-126">它不會在每部電腦安裝期間安裝到每個使用者的設定檔中。</span><span class="sxs-lookup"><span data-stu-id="21a82-126">It is not installed into each user's profile during a per-machine installation.</span></span>      |
| <span data-ttu-id="21a82-127">IniFile ' \[ 1 \] ' 將會安裝到每個使用者目錄 ' \[ 2 \] '，而不會因 [**ALLUSERS**](allusers.md) 值而不同。</span><span class="sxs-lookup"><span data-stu-id="21a82-127">The IniFile '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="21a82-128">此檔案不會複製到每個使用者的設定檔中，即使需要每一部電腦安裝也一樣。</span><span class="sxs-lookup"><span data-stu-id="21a82-128">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span>  | <span data-ttu-id="21a82-129">.Ini 檔案會安裝到每個使用者的目錄中。</span><span class="sxs-lookup"><span data-stu-id="21a82-129">The .ini file is installed into a per-user only directory.</span></span> <span data-ttu-id="21a82-130">它不會在每部電腦安裝期間安裝到每個使用者的設定檔中。</span><span class="sxs-lookup"><span data-stu-id="21a82-130">It is not installed into each user's profile during a per-machine installation.</span></span> |
| <span data-ttu-id="21a82-131">快捷方式 ' \[ 1 \] ' 將會安裝到每個使用者目錄 ' \[ 2 \] '，而不會因 [**ALLUSERS**](allusers.md) 值而不同。</span><span class="sxs-lookup"><span data-stu-id="21a82-131">The shortcut '\[1\]' will be installed to the per user directory '\[2\]' that does not vary based on [**ALLUSERS**](allusers.md) value.</span></span> <span data-ttu-id="21a82-132">此檔案不會複製到每個使用者的設定檔中，即使需要每一部電腦安裝也一樣。</span><span class="sxs-lookup"><span data-stu-id="21a82-132">This file won't be copied to each user's profile even if a per machine installation is desired.</span></span> | <span data-ttu-id="21a82-133">此快捷方式會安裝到每個使用者的目錄中。</span><span class="sxs-lookup"><span data-stu-id="21a82-133">The shortcut is installed into a per-user only directory.</span></span> <span data-ttu-id="21a82-134">它不會在每部電腦安裝期間安裝到每個使用者的設定檔中。</span><span class="sxs-lookup"><span data-stu-id="21a82-134">It is not installed into each user's profile during a per-machine installation.</span></span>  |



 

## <a name="example"></a><span data-ttu-id="21a82-135">範例</span><span class="sxs-lookup"><span data-stu-id="21a82-135">Example</span></span>

<span data-ttu-id="21a82-136">ICE91 會報告下列範例警告：</span><span class="sxs-lookup"><span data-stu-id="21a82-136">ICE91 reports the following warnings for the example:</span></span>

``` syntax
The file 'File1' will be installed to the per user directory 'MyPicturesFolder' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The IniFile 'IniFile1' will be installed to the per user directory 'MyIniDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.

The shortcut 'Shortcut1' will be installed to the per user directory 'MyShortcutDir' that does not vary based on ALLUSERS value. This file won't be copied to each user's profile even if a per machine installation is desired.
```

<span data-ttu-id="21a82-137">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="21a82-137">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="21a82-138">檔案</span><span class="sxs-lookup"><span data-stu-id="21a82-138">File</span></span>  | <span data-ttu-id="21a82-139">元件\_</span><span class="sxs-lookup"><span data-stu-id="21a82-139">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="21a82-140">File1</span><span class="sxs-lookup"><span data-stu-id="21a82-140">File1</span></span> | <span data-ttu-id="21a82-141">C1</span><span class="sxs-lookup"><span data-stu-id="21a82-141">C1</span></span>          |



 

<span data-ttu-id="21a82-142">[元件資料表](component-table.md) (部分)  (部分)  (部分)  (部分) </span><span class="sxs-lookup"><span data-stu-id="21a82-142">[Component Table](component-table.md) (partial) (partial) (partial) (partial)</span></span>



| <span data-ttu-id="21a82-143">元件</span><span class="sxs-lookup"><span data-stu-id="21a82-143">Component</span></span> | <span data-ttu-id="21a82-144">目錄\_</span><span class="sxs-lookup"><span data-stu-id="21a82-144">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="21a82-145">C1</span><span class="sxs-lookup"><span data-stu-id="21a82-145">C1</span></span>        | <span data-ttu-id="21a82-146">MyDir</span><span class="sxs-lookup"><span data-stu-id="21a82-146">MyDir</span></span>       |



 

[<span data-ttu-id="21a82-147">IniFile 資料表</span><span class="sxs-lookup"><span data-stu-id="21a82-147">IniFile Table</span></span>](inifile-table.md)



| <span data-ttu-id="21a82-148">IniFile</span><span class="sxs-lookup"><span data-stu-id="21a82-148">IniFile</span></span>  | <span data-ttu-id="21a82-149">DirProperty</span><span class="sxs-lookup"><span data-stu-id="21a82-149">DirProperty</span></span> |
|----------|-------------|
| <span data-ttu-id="21a82-150">IniFile1</span><span class="sxs-lookup"><span data-stu-id="21a82-150">IniFile1</span></span> | <span data-ttu-id="21a82-151">MyIniDir</span><span class="sxs-lookup"><span data-stu-id="21a82-151">MyIniDir</span></span>    |



 

[<span data-ttu-id="21a82-152">快速鍵資料表</span><span class="sxs-lookup"><span data-stu-id="21a82-152">Shortcut Table</span></span>](shortcut-table.md)



| <span data-ttu-id="21a82-153">快速鍵</span><span class="sxs-lookup"><span data-stu-id="21a82-153">Shortcut</span></span>  | <span data-ttu-id="21a82-154">目錄\_</span><span class="sxs-lookup"><span data-stu-id="21a82-154">Directory\_</span></span>   |
|-----------|---------------|
| <span data-ttu-id="21a82-155">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="21a82-155">Shortcut1</span></span> | <span data-ttu-id="21a82-156">MyShortcutDir</span><span class="sxs-lookup"><span data-stu-id="21a82-156">MyShortcutDir</span></span> |



 

[<span data-ttu-id="21a82-157">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="21a82-157">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="21a82-158">目錄</span><span class="sxs-lookup"><span data-stu-id="21a82-158">Directory</span></span>     | <span data-ttu-id="21a82-159">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="21a82-159">Directory\_Parent</span></span>  |
|---------------|--------------------|
| <span data-ttu-id="21a82-160">MyDir</span><span class="sxs-lookup"><span data-stu-id="21a82-160">MyDir</span></span>         | <span data-ttu-id="21a82-161">FavoritesFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-161">FavoritesFolder</span></span>    |
| <span data-ttu-id="21a82-162">MyIniDir</span><span class="sxs-lookup"><span data-stu-id="21a82-162">MyIniDir</span></span>      | <span data-ttu-id="21a82-163">LocalAppDataFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-163">LocalAppDataFolder</span></span> |
| <span data-ttu-id="21a82-164">MyShortcutDir</span><span class="sxs-lookup"><span data-stu-id="21a82-164">MyShortcutDir</span></span> | <span data-ttu-id="21a82-165">PersonalFolder</span><span class="sxs-lookup"><span data-stu-id="21a82-165">PersonalFolder</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="21a82-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="21a82-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21a82-167">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="21a82-167">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



