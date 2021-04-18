---
description: ICE64 會檢查使用者設定檔中的新目錄在漫遊案例中是否已正確移除。
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513717"
---
# <a name="ice64"></a><span data-ttu-id="733a1-103">ICE64</span><span class="sxs-lookup"><span data-stu-id="733a1-103">ICE64</span></span>

<span data-ttu-id="733a1-104">ICE64 會檢查使用者設定檔中的新目錄在漫遊案例中是否已正確移除。</span><span class="sxs-lookup"><span data-stu-id="733a1-104">ICE64 checks that new directories in the user profile are removed correctly in roaming scenarios.</span></span>

<span data-ttu-id="733a1-105">若無法修正 ICE64 回報的警告或錯誤，通常會導致在卸載期間完全清除電腦時發生問題。</span><span class="sxs-lookup"><span data-stu-id="733a1-105">Failure to fix a warning or error reported by ICE64 generally leads to problems in completely cleaning the computer during an uninstallation.</span></span> <span data-ttu-id="733a1-106">當已安裝應用程式的漫遊使用者第一次登入電腦時，會將所有配置檔案複製到電腦上。</span><span class="sxs-lookup"><span data-stu-id="733a1-106">When a roaming user who has installed the application logs on to a computer for the first time, all of the profile is copied down onto the computer.</span></span> <span data-ttu-id="733a1-107">在漫遊設定檔下載) 之後的公告 (，安裝程式會確認目錄是否已存在，因此不會在卸載時將它刪除。</span><span class="sxs-lookup"><span data-stu-id="733a1-107">On advertisement (which takes place after the roaming profile download), the Installer verifies that the directory is already there and therefore does not delete it on uninstallation.</span></span> <span data-ttu-id="733a1-108">這會將目錄永久保留在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="733a1-108">This leaves the directory on the user's computer permanently.</span></span>

## <a name="result"></a><span data-ttu-id="733a1-109">結果</span><span class="sxs-lookup"><span data-stu-id="733a1-109">Result</span></span>

<span data-ttu-id="733a1-110">如果未移除使用者設定檔中應移除的新目錄，ICE64 會在漫遊情況下張貼警告或錯誤。</span><span class="sxs-lookup"><span data-stu-id="733a1-110">ICE64 posts a warning or an error in a roaming situation if a new directory in the user profile that should be removed is not removed.</span></span>

## <a name="example"></a><span data-ttu-id="733a1-111">範例</span><span class="sxs-lookup"><span data-stu-id="733a1-111">Example</span></span>

<span data-ttu-id="733a1-112">ICE64 會針對所顯示的範例報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="733a1-112">ICE64 reports the following error for the example shown.</span></span>

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

<span data-ttu-id="733a1-113">資料夾 ' MyOtherFolder ' 是自訂的設定檔資料夾。</span><span class="sxs-lookup"><span data-stu-id="733a1-113">The folder 'MyOtherFolder' is a custom profile folder.</span></span> <span data-ttu-id="733a1-114">因為它未列在 RemoveFile 資料表中，所以在某些情況下不會移除它。</span><span class="sxs-lookup"><span data-stu-id="733a1-114">Because it is not listed in the RemoveFile table, it is not removed in some scenarios.</span></span>

<span data-ttu-id="733a1-115">若要修正這個錯誤，請在 RemoveFile 資料表中建立資料夾的資料列。</span><span class="sxs-lookup"><span data-stu-id="733a1-115">To fix this error, create a row for the folder in the RemoveFile table.</span></span>

[<span data-ttu-id="733a1-116">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="733a1-116">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="733a1-117">目錄</span><span class="sxs-lookup"><span data-stu-id="733a1-117">Directory</span></span>     | <span data-ttu-id="733a1-118">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="733a1-118">Directory\_Parent</span></span> | <span data-ttu-id="733a1-119">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="733a1-119">DefaultDir</span></span>  |
|---------------|-------------------|-------------|
| <span data-ttu-id="733a1-120">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="733a1-120">AppDataFolder</span></span> | <span data-ttu-id="733a1-121">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="733a1-121">TARGETDIR</span></span>         |             |
| <span data-ttu-id="733a1-122">MyFolder</span><span class="sxs-lookup"><span data-stu-id="733a1-122">MyFolder</span></span>      | <span data-ttu-id="733a1-123">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="733a1-123">AppDataFolder</span></span>     | <span data-ttu-id="733a1-124">DataFolder</span><span class="sxs-lookup"><span data-stu-id="733a1-124">DataFolder</span></span>  |
| <span data-ttu-id="733a1-125">MyOtherFolder</span><span class="sxs-lookup"><span data-stu-id="733a1-125">MyOtherFolder</span></span> | <span data-ttu-id="733a1-126">AppDataFolder</span><span class="sxs-lookup"><span data-stu-id="733a1-126">AppDataFolder</span></span>     | <span data-ttu-id="733a1-127">DataFolder2</span><span class="sxs-lookup"><span data-stu-id="733a1-127">DataFolder2</span></span> |



 

[<span data-ttu-id="733a1-128">RemoveFile 資料表</span><span class="sxs-lookup"><span data-stu-id="733a1-128">RemoveFile Table</span></span>](removefile-table.md)



| <span data-ttu-id="733a1-129">FileKey</span><span class="sxs-lookup"><span data-stu-id="733a1-129">FileKey</span></span> | <span data-ttu-id="733a1-130">元件\_</span><span class="sxs-lookup"><span data-stu-id="733a1-130">Component\_</span></span> | <span data-ttu-id="733a1-131">FileName</span><span class="sxs-lookup"><span data-stu-id="733a1-131">FileName</span></span> | <span data-ttu-id="733a1-132">DirProperty</span><span class="sxs-lookup"><span data-stu-id="733a1-132">DirProperty</span></span> | <span data-ttu-id="733a1-133">InstallMode</span><span class="sxs-lookup"><span data-stu-id="733a1-133">InstallMode</span></span> |
|---------|-------------|----------|-------------|-------------|
| <span data-ttu-id="733a1-134">Key1</span><span class="sxs-lookup"><span data-stu-id="733a1-134">Key1</span></span>    | <span data-ttu-id="733a1-135">Component1</span><span class="sxs-lookup"><span data-stu-id="733a1-135">Component1</span></span>  |          | <span data-ttu-id="733a1-136">MyFolder</span><span class="sxs-lookup"><span data-stu-id="733a1-136">MyFolder</span></span>    | <span data-ttu-id="733a1-137">2</span><span class="sxs-lookup"><span data-stu-id="733a1-137">2</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="733a1-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="733a1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="733a1-139">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="733a1-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



