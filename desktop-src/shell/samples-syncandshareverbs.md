---
description: 示範如何註冊可延伸 &0034 的動詞 \# ;同步&\# 0034; 和 &\# 0034; \#在 Windows 檔案總管命令列中共用&0034; 動詞。
title: 同步和共用動詞
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973748"
---
# <a name="sync-and-share-verbs"></a><span data-ttu-id="1d311-103">同步和共用動詞</span><span class="sxs-lookup"><span data-stu-id="1d311-103">Sync and Share Verbs</span></span>

<span data-ttu-id="1d311-104">示範如何註冊在 Windows 檔案總管命令列中擴充「同步處理」和「共用」動詞命令的動詞。</span><span class="sxs-lookup"><span data-stu-id="1d311-104">Demonstrates how to register a verb that extends the "Sync" and "Share" verbs in the Windows Explorer Command Bar.</span></span>

<span data-ttu-id="1d311-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="1d311-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1d311-106">需求</span><span class="sxs-lookup"><span data-stu-id="1d311-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1d311-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="1d311-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="1d311-108">執行範例</span><span class="sxs-lookup"><span data-stu-id="1d311-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="1d311-109">移除範例</span><span class="sxs-lookup"><span data-stu-id="1d311-109">Removing the Sample</span></span>](#removing-the-sample)

## <a name="requirements"></a><span data-ttu-id="1d311-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d311-110">Requirements</span></span>



| <span data-ttu-id="1d311-111">產品</span><span class="sxs-lookup"><span data-stu-id="1d311-111">Product</span></span>                                | <span data-ttu-id="1d311-112">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="1d311-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="1d311-113">Windows</span><span class="sxs-lookup"><span data-stu-id="1d311-113">Windows</span></span>                                | <span data-ttu-id="1d311-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d311-114">Windows 7</span></span>               |
| <span data-ttu-id="1d311-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="1d311-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="1d311-116">7.0</span><span class="sxs-lookup"><span data-stu-id="1d311-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="1d311-117">下載範例</span><span class="sxs-lookup"><span data-stu-id="1d311-117">Downloading the Sample</span></span>

| <span data-ttu-id="1d311-118">Location</span><span class="sxs-lookup"><span data-stu-id="1d311-118">Location</span></span>      | <span data-ttu-id="1d311-119">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="1d311-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d311-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="1d311-120">GitHub</span></span>  | [<span data-ttu-id="1d311-121">SyncAndShareVerbs 範例</span><span class="sxs-lookup"><span data-stu-id="1d311-121">SyncAndShareVerbs sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a><span data-ttu-id="1d311-122">執行範例</span><span class="sxs-lookup"><span data-stu-id="1d311-122">Running the Sample</span></span>

<span data-ttu-id="1d311-123">若要執行範例 (同步) ：</span><span class="sxs-lookup"><span data-stu-id="1d311-123">To run the sample (sync):</span></span>

1.  <span data-ttu-id="1d311-124">流覽至 `sync.reg` 包含該檔案的目錄</span><span class="sxs-lookup"><span data-stu-id="1d311-124">Navigate to the directory that contains the `sync.reg` file</span></span>
2.  <span data-ttu-id="1d311-125">`sync.reg `在命令列中輸入，或按兩下圖示進行 `sync.reg` 註冊。</span><span class="sxs-lookup"><span data-stu-id="1d311-125">Type `sync.reg ` at the command line, or double-click the icon for `sync.reg` register it.</span></span>
3.  <span data-ttu-id="1d311-126">開啟 Windows 檔案總管，然後選取檔案。</span><span class="sxs-lookup"><span data-stu-id="1d311-126">Open the Windows Explorer and select a file.</span></span>
4.  <span data-ttu-id="1d311-127">按一下命令列中的 [ **同步** 處理] 選項，然後選取子選項，例如 [ **繪製**]。</span><span class="sxs-lookup"><span data-stu-id="1d311-127">Click the **Sync** option in the Command Bar and select a suboption such as **Paint**.</span></span>

<span data-ttu-id="1d311-128">若要執行範例 (共用) ：</span><span class="sxs-lookup"><span data-stu-id="1d311-128">To run the sample (share):</span></span>

1.  <span data-ttu-id="1d311-129">流覽至包含該檔案的目錄 `share.reg` 。</span><span class="sxs-lookup"><span data-stu-id="1d311-129">Navigate to the directory that contains the `share.reg` file.</span></span>
2.  <span data-ttu-id="1d311-130">`share.reg`在命令列中輸入，或按兩下圖示進行 `share.reg` 註冊。</span><span class="sxs-lookup"><span data-stu-id="1d311-130">Type `share.reg` at the command line, or double-click the icon for `share.reg` register it.</span></span>
3.  <span data-ttu-id="1d311-131">開啟 Windows 檔案總管然後選取檔案。</span><span class="sxs-lookup"><span data-stu-id="1d311-131">Open Windows Explorer and select a file.</span></span> <span data-ttu-id="1d311-132">按一下命令列中的 [ **共用** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="1d311-132">Click the **Share** option in the Command Bar.</span></span>
4.  <span data-ttu-id="1d311-133">按一下命令列中的 [ **共用方式** ] 選項，然後選取子選項，例如 [ **繪製**]。</span><span class="sxs-lookup"><span data-stu-id="1d311-133">Click the **Share with** option in the Command Bar and select a suboption such as **Paint**.</span></span>

## <a name="removing-the-sample"></a><span data-ttu-id="1d311-134">移除範例</span><span class="sxs-lookup"><span data-stu-id="1d311-134">Removing the Sample</span></span>

<span data-ttu-id="1d311-135">若要移除範例 (同步) ：</span><span class="sxs-lookup"><span data-stu-id="1d311-135">To remove the sample (sync):</span></span>

1.  <span data-ttu-id="1d311-136">流覽至包含 Uninstallsync .reg 檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="1d311-136">Navigate to the directory that contains the Uninstallsync.reg file.</span></span>
2.  <span data-ttu-id="1d311-137">`uninstallsync.reg`在命令列中輸入，或按兩下的圖示 `uninstallsync.reg` 。</span><span class="sxs-lookup"><span data-stu-id="1d311-137">Type `uninstallsync.reg` at the command line, or double-click the icon for `uninstallsync.reg`.</span></span>

<span data-ttu-id="1d311-138">若要移除範例 (共用) ：</span><span class="sxs-lookup"><span data-stu-id="1d311-138">To remove the sample (share):</span></span>

1.  <span data-ttu-id="1d311-139">流覽至包含 Uninstallshare .reg 檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="1d311-139">Navigate to the directory that contains the Uninstallshare.reg file.</span></span>
2.  <span data-ttu-id="1d311-140">`uninstallshare.reg`在命令列中輸入，或按兩下圖示`uninstallshare.reg.`</span><span class="sxs-lookup"><span data-stu-id="1d311-140">Type `uninstallshare.reg` at the command line, or double-click the icon for `uninstallshare.reg.`</span></span>

 

 



