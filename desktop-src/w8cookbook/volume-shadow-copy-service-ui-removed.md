---
title: 已移除本機磁片區的舊版 UI
description: 已移除本機磁片區的舊版 UI
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104463829"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a><span data-ttu-id="330d9-103">已移除本機磁片區的舊版 UI</span><span class="sxs-lookup"><span data-stu-id="330d9-103">Previous versions UI removed for local volumes</span></span>

## <a name="platform"></a><span data-ttu-id="330d9-104">平台</span><span class="sxs-lookup"><span data-stu-id="330d9-104">Platform</span></span>

<span data-ttu-id="330d9-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="330d9-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="330d9-106">Description</span><span class="sxs-lookup"><span data-stu-id="330d9-106">Description</span></span>

<span data-ttu-id="330d9-107">舊版 Windows 允許使用者從本機磁片區的「陰影複製」還原舊版的個別檔案。</span><span class="sxs-lookup"><span data-stu-id="330d9-107">Earlier versions of Windows allowed users to restore previous versions of individual files from “shadow copies” of local volumes.</span></span> <span data-ttu-id="330d9-108">這些陰影複製是透過磁片區陰影複製服務 (VSS) ，由「先前的版本」功能所建立。</span><span class="sxs-lookup"><span data-stu-id="330d9-108">These shadow copies are created by the “Previous Versions” feature through Volume Shadow Copy service (VSS).</span></span> <span data-ttu-id="330d9-109">在 Windows 7 中，使用者可以在系統屬性提供的系統保護 UI 中，設定和排程陰影複製。</span><span class="sxs-lookup"><span data-stu-id="330d9-109">In Windows 7, users could configure and schedule shadow copies in System Protection UI available through System Properties.</span></span>

<span data-ttu-id="330d9-110">不過，先前的版本很少使用，且會對整體 Windows 效能造成負面影響;因此已移除此功能。</span><span class="sxs-lookup"><span data-stu-id="330d9-110">However, Previous Versions were rarely used and negatively impacted the overall Windows performance; as a result the feature was removed.</span></span> <span data-ttu-id="330d9-111">在 Windows 8 中，這些功能已無法再使用：</span><span class="sxs-lookup"><span data-stu-id="330d9-111">In Windows 8, these features are no longer available:</span></span>

-   <span data-ttu-id="330d9-112">可以透過舊版 UI 流覽、搜尋或還原先前版本的檔案</span><span class="sxs-lookup"><span data-stu-id="330d9-112">The ability to browse, search or restore previous versions of files through Previous Versions UI</span></span>
-   <span data-ttu-id="330d9-113">透過系統保護 UI 設定或排程先前版本檔案的能力</span><span class="sxs-lookup"><span data-stu-id="330d9-113">The ability to configure or schedule previous versions of files through System Protection UI</span></span>

<span data-ttu-id="330d9-114">不過，使用者在存取 Windows server 上的檔案共用時，仍可使用 [先前的版本] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="330d9-114">However, users can still use the Previous Versions tab when accessing file shares on a Windows server.</span></span>

## <a name="manifestation"></a><span data-ttu-id="330d9-115">表現</span><span class="sxs-lookup"><span data-stu-id="330d9-115">Manifestation</span></span>

<span data-ttu-id="330d9-116">在 [Windows 檔案總管內容] 功能表中，本機磁片區無法再使用 [先前的版本] 選項。</span><span class="sxs-lookup"><span data-stu-id="330d9-116">The Previous Versions option is no longer available for local volumes in the Windows Explorer Properties menu.</span></span>

## <a name="solution"></a><span data-ttu-id="330d9-117">解決方法</span><span class="sxs-lookup"><span data-stu-id="330d9-117">Solution</span></span>

<span data-ttu-id="330d9-118">需要建立本機磁片區陰影複製的開發人員仍然可以藉由呼叫自訂程式碼中的 VSS Api 來這麼做。</span><span class="sxs-lookup"><span data-stu-id="330d9-118">Developers who need to create shadow copies of local volumes can still do so by calling VSS APIs in custom code.</span></span>

 

 




