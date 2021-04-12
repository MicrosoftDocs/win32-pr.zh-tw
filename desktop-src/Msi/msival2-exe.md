---
description: Msival2.exe 是一種命令列公用程式，可執行一組內部一致性評估工具（面向）。
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195275"
---
# <a name="msival2exe"></a><span data-ttu-id="5b5f2-103">Msival2.exe</span><span class="sxs-lookup"><span data-stu-id="5b5f2-103">Msival2.exe</span></span>

<span data-ttu-id="5b5f2-104">Msival2.exe 是一種命令列公用程式，可執行一組 [內部一致性評估工具（面向）](internal-consistency-evaluators-ices.md)。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-104">Msival2.exe is a command line utility that can run a suite of [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="5b5f2-105">此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="5b5f2-106">如需有關 Ices-003 和 .CUB 檔案的詳細資訊，請參閱 [使用內部一致性評估](using-internal-consistency-evaluators.md)工具。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-106">For more information about ICEs and the CUB file, see [Using Internal Consistency Evaluators](using-internal-consistency-evaluators.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5f2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b5f2-107">Syntax</span></span>

<span data-ttu-id="5b5f2-108">**Msival2** *{DATABASE} {.cub file} \[ -f \] \[ -l {Logfile} \] \[ -i {ice id} \[ \] \] ： {ICE id} ...*</span><span class="sxs-lookup"><span data-stu-id="5b5f2-108">**Msival2** *{database}{CUB file}\[-f\]\[-l {logfile}\]\[-i {ICE Id}\[:{ICE Id}...\]\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="5b5f2-109">命令列選項</span><span class="sxs-lookup"><span data-stu-id="5b5f2-109">Command Line Options</span></span>

<span data-ttu-id="5b5f2-110">Msival2.exe 會使用下列不區分大小寫的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-110">Msival2.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="5b5f2-111">斜線分隔符號也可以用來取代虛線。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="5b5f2-112">選項</span><span class="sxs-lookup"><span data-stu-id="5b5f2-112">Option</span></span> | <span data-ttu-id="5b5f2-113">Description</span><span class="sxs-lookup"><span data-stu-id="5b5f2-113">Description</span></span>                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5f2-114">-f</span><span class="sxs-lookup"><span data-stu-id="5b5f2-114">-f</span></span>     | <span data-ttu-id="5b5f2-115">篩選出顯示結果中的所有參考訊息。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-115">Filter out all informational messages from the displayed results.</span></span> <span data-ttu-id="5b5f2-116">會顯示所有其他類型的訊息。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-116">All other types of messages are displayed.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="5b5f2-117">-i</span><span class="sxs-lookup"><span data-stu-id="5b5f2-117">-i</span></span>     | <span data-ttu-id="5b5f2-118">依照指定的順序，僅執行命令列上所列的 Ices-003。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-118">Run only the ICEs listed on the command line in the order specified.</span></span> <span data-ttu-id="5b5f2-119">每個 ICE 自訂動作都應該列出，因為它出現在 .CUB 檔案的 [CustomAction 資料表](customaction-table.md) 中。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-119">Each ICE custom action should be listed as it appears in the [CustomAction table](customaction-table.md) of the CUB file.</span></span> <span data-ttu-id="5b5f2-120">如果省略這個選項，此工具會執行由 .CUB 檔案的作者指定的一組預設的一組。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-120">If this option is omitted, the tool runs the default set of ICEs specified by the author of the CUB file.</span></span> |
| <span data-ttu-id="5b5f2-121">-l</span><span class="sxs-lookup"><span data-stu-id="5b5f2-121">-l</span></span>     | <span data-ttu-id="5b5f2-122">將結果寫入指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-122">Write results to the specified file.</span></span> <span data-ttu-id="5b5f2-123">檔案不能已經存在。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-123">The file must not already exist.</span></span> <span data-ttu-id="5b5f2-124">如果檔案存在，則不會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="5b5f2-124">If the file exists, it is not overwritten.</span></span>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="5b5f2-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b5f2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b5f2-126">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="5b5f2-126">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="5b5f2-127">內部一致性評估工具-Ices-003</span><span class="sxs-lookup"><span data-stu-id="5b5f2-127">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)
</dt> <dt>

[<span data-ttu-id="5b5f2-128">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5b5f2-128">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



