---
description: 本節中的材質適用于撰寫自己的安裝程式的開發人員，他們想要深入瞭解 Windows Installer 資料庫資料表。 如需一般資訊，請參閱關於 Windows Installer。
ms.assetid: c4bedc0e-cd1a-4cdc-8dd1-4a774aaf533e
title: 摘要資訊串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd9d6792249433c4200a8e68515fbfeb409b390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983339"
---
# <a name="summary-information-stream"></a><span data-ttu-id="e2ec5-104">摘要資訊串流</span><span class="sxs-lookup"><span data-stu-id="e2ec5-104">Summary Information Stream</span></span>

<span data-ttu-id="e2ec5-105">本節中的材質適用于撰寫自己的安裝程式的開發人員，他們想要深入瞭解 Windows Installer 資料庫資料表。</span><span class="sxs-lookup"><span data-stu-id="e2ec5-105">The material in this section is intended for developers who are writing their own setup programs who want to learn more about Windows Installer database tables.</span></span> <span data-ttu-id="e2ec5-106">如需一般資訊，請參閱 [關於 Windows Installer](about-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="e2ec5-106">For general information, see [About Windows Installer](about-windows-installer.md).</span></span>

<span data-ttu-id="e2ec5-107">安裝程式會使用摘要資訊資料流程進行兩個目的。</span><span class="sxs-lookup"><span data-stu-id="e2ec5-107">The summary information stream is used by the installer for two purposes.</span></span> <span data-ttu-id="e2ec5-108">首先，它包含可透過 Microsoft Windows 檔案總管查看之封裝的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e2ec5-108">First, it contains information about the package that can be viewed through Microsoft Windows Explorer.</span></span> <span data-ttu-id="e2ec5-109">這項資訊可透過 **IStream** 介面進行存取。</span><span class="sxs-lookup"><span data-stu-id="e2ec5-109">This information is accessible through the **IStream** interface.</span></span> <span data-ttu-id="e2ec5-110">其次，它包含安裝程式用來安裝封裝的屬性。</span><span class="sxs-lookup"><span data-stu-id="e2ec5-110">Second, it contains properties that are used by the installer to install the package.</span></span> <span data-ttu-id="e2ec5-111">下列主題提供有關如何搭配安裝程式使用摘要資訊串流的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="e2ec5-111">The following topics provide information about how to use the summary information stream with the installer:</span></span>

-   [<span data-ttu-id="e2ec5-112">關於摘要資訊資料流程</span><span class="sxs-lookup"><span data-stu-id="e2ec5-112">About the Summary Information Stream</span></span>](about-the-summary-information-stream.md)
-   [<span data-ttu-id="e2ec5-113">使用摘要資訊資料流程</span><span class="sxs-lookup"><span data-stu-id="e2ec5-113">Using the Summary Information Stream</span></span>](using-the-summary-information-stream.md)
-   [<span data-ttu-id="e2ec5-114">摘要資訊資料流程參考</span><span class="sxs-lookup"><span data-stu-id="e2ec5-114">Summary Information Stream Reference</span></span>](summary-information-stream-reference.md)

 

 



