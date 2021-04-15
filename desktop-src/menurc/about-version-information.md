---
title: 關於版本資訊
description: 本主題討論版本資訊功能。
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- 資源，版本資訊
- 版本資訊
- 加入版本資訊
- 檔案衝突
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375105"
---
# <a name="about-version-information"></a><span data-ttu-id="2f4ca-107">關於版本資訊</span><span class="sxs-lookup"><span data-stu-id="2f4ca-107">About Version Information</span></span>

<span data-ttu-id="2f4ca-108">您可以使用版本資訊函式來判斷應該安裝檔案的位置，以及識別與目前已安裝之檔案的衝突。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-108">You can use the version information functions to determine where a file should be installed and identify conflicts with currently installed files.</span></span> <span data-ttu-id="2f4ca-109">這些函數可讓您避免下列問題：</span><span class="sxs-lookup"><span data-stu-id="2f4ca-109">These functions enable you to avoid the following problems:</span></span>

-   <span data-ttu-id="2f4ca-110">在較新版本上安裝較舊版本的元件</span><span class="sxs-lookup"><span data-stu-id="2f4ca-110">installing older versions of components over newer versions</span></span>
-   <span data-ttu-id="2f4ca-111">在混合語言系統中變更語言而不發出通知</span><span class="sxs-lookup"><span data-stu-id="2f4ca-111">changing the language in a mixed-language system without notification</span></span>
-   <span data-ttu-id="2f4ca-112">在不同的目錄中安裝程式庫的多個複本</span><span class="sxs-lookup"><span data-stu-id="2f4ca-112">installing multiple copies of a library in different directories</span></span>
-   <span data-ttu-id="2f4ca-113">將檔案複製到多個使用者共用的網路目錄</span><span class="sxs-lookup"><span data-stu-id="2f4ca-113">copying files to network directories shared by multiple users</span></span>

<span data-ttu-id="2f4ca-114">版本資訊函式可讓應用程式查詢版本資源以取得檔案資訊，並以純文字格式呈現資訊。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-114">The version information functions enable applications to query a version resource for file information and present the information in a clear format.</span></span> <span data-ttu-id="2f4ca-115">此資訊包括檔案的用途、作者、版本號碼等等。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-115">This information includes the file's purpose, author, version number, and so on.</span></span>

<span data-ttu-id="2f4ca-116">您可以將版本資訊新增至任何可以有 Windows 資源的檔案，例如 Dll、可執行檔或 fon 字型檔案。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-116">You can add version information to any files that can have Windows resources, such as DLLs, executable files, or .fon font files.</span></span> <span data-ttu-id="2f4ca-117">若要新增資訊，請建立 [VERSIONINFO 資源](/windows/desktop/menurc/versioninfo-resource) ，並使用資源編譯器來編譯資源。</span><span class="sxs-lookup"><span data-stu-id="2f4ca-117">To add the information, create a [VERSIONINFO Resource](/windows/desktop/menurc/versioninfo-resource) and use the resource compiler to compile the resource.</span></span>

 

 