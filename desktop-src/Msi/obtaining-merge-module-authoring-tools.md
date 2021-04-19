---
description: 若要產生合併模組，您需要取得用來編輯 .msm 檔案的軟體工具。
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: 取得合併模組撰寫工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969227"
---
# <a name="obtaining-merge-module-authoring-tools"></a><span data-ttu-id="9e5da-103">取得合併模組撰寫工具</span><span class="sxs-lookup"><span data-stu-id="9e5da-103">Obtaining Merge Module Authoring Tools</span></span>

<span data-ttu-id="9e5da-104">若要產生合併模組，您需要取得用來編輯 .msm 檔案的軟體工具。</span><span class="sxs-lookup"><span data-stu-id="9e5da-104">To generate a merge module, you need to obtain a software tool with which to edit an .msm file.</span></span> <span data-ttu-id="9e5da-105">因為 .msm 檔案基本上是簡化的 .msi 檔案，所以您可以使用用來建立安裝資料庫的相同工具。</span><span class="sxs-lookup"><span data-stu-id="9e5da-105">Because an .msm file is basically a simplified .msi file, you may be able to use the same tools used to create an installation database.</span></span> <span data-ttu-id="9e5da-106">例如，Orca.exe Windows Installer SDK 提供的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9e5da-106">For example, the application Orca.exe provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="9e5da-107">另一種方式是購買可從獨立軟體廠商取得的其中一個安裝程式封裝工具。</span><span class="sxs-lookup"><span data-stu-id="9e5da-107">An alternative is to purchase one of the installer packaging tools to be available from independent software vendors.</span></span> <span data-ttu-id="9e5da-108">開發中有數個協力廠商工具，可用來產生合併模組。</span><span class="sxs-lookup"><span data-stu-id="9e5da-108">There are several third-party tools under development that may be used for producing merge modules.</span></span> <span data-ttu-id="9e5da-109">如果您選擇使用協力廠商工具，您應該確認它會產生與本檔中所述標準一致的合併模組。</span><span class="sxs-lookup"><span data-stu-id="9e5da-109">If you choose to use a third-party tool you should verify that it generates merge modules that are consistent with the standard described in this document.</span></span> <span data-ttu-id="9e5da-110">尤其是，您應該判斷編輯工具尚未對合併模組執行下列任何一項動作。</span><span class="sxs-lookup"><span data-stu-id="9e5da-110">In particular, you should determine that the editing tools have not done any of the following to the merge module.</span></span>

-   <span data-ttu-id="9e5da-111">已將多餘的資料表新增至 [ModuleIgnoreTable 資料表](moduleignoretable-table.md)中未參考的合併模組。</span><span class="sxs-lookup"><span data-stu-id="9e5da-111">Added extraneous tables to the merge module that are not referenced in the [ModuleIgnoreTable table](moduleignoretable-table.md).</span></span>

    <span data-ttu-id="9e5da-112">刪除這些資料表，或將它們加入至 ModuleIgnoreTable 資料表。</span><span class="sxs-lookup"><span data-stu-id="9e5da-112">Delete these tables or add them to the ModuleIgnoreTable table.</span></span>

-   <span data-ttu-id="9e5da-113">將不必要的 [樣式表單](textstyle-table.md) 加入至合併模組。</span><span class="sxs-lookup"><span data-stu-id="9e5da-113">Added an unnecessary [TextStyle table](textstyle-table.md) to the merge module.</span></span>

    <span data-ttu-id="9e5da-114">如果您的合併模組沒有 UI (而且通常不應該) 您可以安全地刪除此資料表。</span><span class="sxs-lookup"><span data-stu-id="9e5da-114">If your merge module has no UI (and it generally should not) you can safely delete this table.</span></span>

-   <span data-ttu-id="9e5da-115">已將不必要的專案新增至 [目錄資料表](directory-table.md)。</span><span class="sxs-lookup"><span data-stu-id="9e5da-115">Added unnecessary entries to the [Directory table](directory-table.md).</span></span>

    <span data-ttu-id="9e5da-116">從目錄資料表中移除不必要的專案。</span><span class="sxs-lookup"><span data-stu-id="9e5da-116">Remove unnecessary entries from the Directory table.</span></span>

-   <span data-ttu-id="9e5da-117">從合併模組的驗證資料表中取出資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9e5da-117">Left information out of the merge module's \_Validation table.</span></span>

    <span data-ttu-id="9e5da-118">這可防止合併模組驗證。</span><span class="sxs-lookup"><span data-stu-id="9e5da-118">This prevents merge module validation.</span></span> <span data-ttu-id="9e5da-119">加入完整的 \_ 驗證資料表。</span><span class="sxs-lookup"><span data-stu-id="9e5da-119">Add a complete \_Validation table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e5da-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e5da-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e5da-121">在合併模組中撰寫使用者介面</span><span class="sxs-lookup"><span data-stu-id="9e5da-121">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="9e5da-122">撰寫合併模組目錄資料表</span><span class="sxs-lookup"><span data-stu-id="9e5da-122">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="9e5da-123">驗證合併模組</span><span class="sxs-lookup"><span data-stu-id="9e5da-123">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> </dl>

 

 



