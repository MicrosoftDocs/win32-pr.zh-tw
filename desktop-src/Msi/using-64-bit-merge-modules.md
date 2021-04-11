---
description: 撰寫64位合併模組時，請遵循這些指導方針。
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: 使用64位合併模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693844"
---
# <a name="using-64-bit-merge-modules"></a><span data-ttu-id="d4492-103">使用64位合併模組</span><span class="sxs-lookup"><span data-stu-id="d4492-103">Using 64-bit Merge Modules</span></span>

<span data-ttu-id="d4492-104">64位合併模組具有此主題中所識別的任何特性。</span><span class="sxs-lookup"><span data-stu-id="d4492-104">A 64-bit merge module has any of the characteristics identified in this this topic.</span></span>

-   <span data-ttu-id="d4492-105">合併模組至少包含一個已針對64位作業系統編譯的元件。</span><span class="sxs-lookup"><span data-stu-id="d4492-105">The merge module contains at least one component that has been compiled for 64-bit operating systems.</span></span>
-   <span data-ttu-id="d4492-106">Merge 模組不包含64位元件，但僅供 [64 位 Windows Installer](64-bit-windows-installer-packages.md) 套件使用。</span><span class="sxs-lookup"><span data-stu-id="d4492-106">The merge module contains no 64-bit components, but is intended for use only with [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>

<span data-ttu-id="d4492-107">合併模組可如下所示使用：</span><span class="sxs-lookup"><span data-stu-id="d4492-107">Merge modules can be used as follows:</span></span>

-   <span data-ttu-id="d4492-108">64位合併模組可以合併至 [64 位 Windows Installer](64-bit-windows-installer-packages.md) 套件。</span><span class="sxs-lookup"><span data-stu-id="d4492-108">A 64-bit merge module can be merged into a [64-bit Windows Installer](64-bit-windows-installer-packages.md) package.</span></span> <span data-ttu-id="d4492-109">合併模組和 Windows Installer 封裝中的 [**範本摘要**](template-summary.md) 屬性必須設定為相同類型的64位處理器。</span><span class="sxs-lookup"><span data-stu-id="d4492-109">The [**Template Summary**](template-summary.md) properties in the merge module and in the Windows Installer package must be set to the same type of 64-bit processor.</span></span> <span data-ttu-id="d4492-110">X64 合併模組只能合併為 x64 封裝，且 Intel64 合併模組只能合併到 Intel64 封裝中。</span><span class="sxs-lookup"><span data-stu-id="d4492-110">A x64 merge module can be merged only into x64 packages and an Intel64 merge module can be merged only into Intel64 packages.</span></span>
-   <span data-ttu-id="d4492-111">32位合併模組可以合併至32位或 [64 位 Windows Installer](64-bit-windows-installer-packages.md) 套件。</span><span class="sxs-lookup"><span data-stu-id="d4492-111">A 32-bit merge module can be merged into 32-bit or [64-bit Windows Installer](64-bit-windows-installer-packages.md) packages.</span></span>
-   <span data-ttu-id="d4492-112">64位合併模組可以合併到32位作業系統上的64位封裝中。</span><span class="sxs-lookup"><span data-stu-id="d4492-112">A 64-bit merge module can be merged into a 64-bit package on a 32-bit operating system.</span></span>

<span data-ttu-id="d4492-113">撰寫64位合併模組時，請遵守下列各項：</span><span class="sxs-lookup"><span data-stu-id="d4492-113">Adhere to the following when authoring a 64-bit merge module:</span></span>

-   <span data-ttu-id="d4492-114">使用與撰寫32位合併模組時相同的一般程式。</span><span class="sxs-lookup"><span data-stu-id="d4492-114">Use the same general procedure as when authoring 32-bit merge modules.</span></span> <span data-ttu-id="d4492-115">如需詳細資訊，請參閱 [關於合併模組](about-merge-modules.md) 和 [撰寫合併模組](authoring-merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="d4492-115">For information, see [About Merge Modules](about-merge-modules.md) and [Authoring Merge Modules](authoring-merge-modules.md).</span></span>
-   <span data-ttu-id="d4492-116">如果執行 Intel64 系統，您必須使用 Intel64 值設定 [**範本摘要**](template-summary.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d4492-116">You must set the [**Template Summary**](template-summary.md) property with the Intel64 value if running an Intel64 system.</span></span> <span data-ttu-id="d4492-117">如果您執行的是 x64 系統，就必須以 x64 值設定 **範本摘要** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d4492-117">You must set the **Template Summary** property with the x64 value if running an x64 system.</span></span> <span data-ttu-id="d4492-118">如需詳細資訊，請參閱 [合併模組摘要資訊資料流程參考](merge-module-summary-information-stream-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="d4492-118">For information see [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md).</span></span>
-   <span data-ttu-id="d4492-119">當相同元件的32位和64位合併模組同時存在時，建議模組具有不同的簽章。</span><span class="sxs-lookup"><span data-stu-id="d4492-119">When both 32-bit and 64-bit merge modules exist for the same component, it is recommended that the modules have different signatures.</span></span> <span data-ttu-id="d4492-120">這會讓套件包含元件的兩個版本。</span><span class="sxs-lookup"><span data-stu-id="d4492-120">This will enable a package to contain both versions of the component.</span></span>

<span data-ttu-id="d4492-121">如需詳細資訊，請參閱 [64 位作業系統上的 Windows Installer](windows-installer-on-64-bit-operating-systems.md)。</span><span class="sxs-lookup"><span data-stu-id="d4492-121">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md).</span></span>

 

 



