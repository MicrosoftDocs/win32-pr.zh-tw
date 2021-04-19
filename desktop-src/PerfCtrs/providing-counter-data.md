---
description: 在 Windows Vista 中，效能計數器會將新的架構 () 2.0 版，以提供計數器資料。
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: 提供計數器資料
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997127"
---
# <a name="providing-counter-data"></a><span data-ttu-id="06341-103">提供計數器資料</span><span class="sxs-lookup"><span data-stu-id="06341-103">Providing Counter Data</span></span>

<span data-ttu-id="06341-104">透過 Windows 效能計數器發佈資料的軟體元件稱為效能資料提供者。</span><span class="sxs-lookup"><span data-stu-id="06341-104">Software components that publish data via Windows Performance Counters are called performance data providers.</span></span>

<span data-ttu-id="06341-105">Windows 支援兩種效能資料提供者。</span><span class="sxs-lookup"><span data-stu-id="06341-105">Windows supports two kinds of performance data providers.</span></span> <span data-ttu-id="06341-106">舊版效能資料提供者 (**V1 提供者**) 是使用來執行的。INI 檔案和效能 DLL。</span><span class="sxs-lookup"><span data-stu-id="06341-106">Legacy performance data providers (**V1 providers**) are implemented using an .INI file and a performance DLL.</span></span> <span data-ttu-id="06341-107">新式效能資料提供者 (**V2 提供者**) 使用。男人 (XML 資訊清單) 和效能計數器提供者 Api。</span><span class="sxs-lookup"><span data-stu-id="06341-107">Modern performance data providers (**V2 providers**) use a .MAN (XML manifest) and the performance counter provider APIs.</span></span>

## <a name="manifests"></a><span data-ttu-id="06341-108">資訊清單</span><span class="sxs-lookup"><span data-stu-id="06341-108">Manifests</span></span>

<span data-ttu-id="06341-109">新式效能資料提供者使用。男人 (XML 資訊清單) 來定義計數器資料，並使用效能計數器提供者 Api 來管理提供者內容中的資料。</span><span class="sxs-lookup"><span data-stu-id="06341-109">Modern performance data providers use a .MAN (XML manifest) to define the counter data and use performance counter provider APIs to manage data within the context of the provider.</span></span>

<span data-ttu-id="06341-110">使用資訊清單和效能計數器提供者 Api 來執行的提供者通常稱為 **V2 提供者**。</span><span class="sxs-lookup"><span data-stu-id="06341-110">Providers implemented using a manifest and performance counter provider APIs are often called **V2 providers**.</span></span>

<span data-ttu-id="06341-111">Windows 在 Windows Vista 或更新版本上支援使用者模式 V2 提供者。</span><span class="sxs-lookup"><span data-stu-id="06341-111">Windows supports user-mode V2 providers on Windows Vista or later.</span></span> <span data-ttu-id="06341-112">如需使用者模式的詳細資料，請參閱 [使用2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md)。</span><span class="sxs-lookup"><span data-stu-id="06341-112">For user-mode details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="06341-113">Windows 在 Windows 7 或更新版本上支援核心模式 V2 提供者。</span><span class="sxs-lookup"><span data-stu-id="06341-113">Windows supports kernel-mode V2 providers on Windows 7 or later.</span></span> <span data-ttu-id="06341-114">如需核心模式的詳細資料，請參閱 [核心模式效能監視](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring)。</span><span class="sxs-lookup"><span data-stu-id="06341-114">For kernel-mode details, see [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span></span>

## <a name="performance-dll-deprecated"></a><span data-ttu-id="06341-115">效能 DLL (已淘汰) </span><span class="sxs-lookup"><span data-stu-id="06341-115">Performance DLL (deprecated)</span></span>

<span data-ttu-id="06341-116">在舊版效能計數器架構中，提供者會將效能 DLL 實作為在取用者的進程中執行的，以便在取用者要求時收集和提供計數器資料。</span><span class="sxs-lookup"><span data-stu-id="06341-116">In the legacy performance counter architecture, providers implemented a performance DLL to that ran in the consumer's process to collect and provide the counter data when a consumer requested it.</span></span> <span data-ttu-id="06341-117">提供者使用初始化 (。INI) 檔案和登錄專案，以定義計數器和設定效能 DLL。</span><span class="sxs-lookup"><span data-stu-id="06341-117">The provider used an initialization (.INI) file and registry entries to define the counters and to configure the performance DLL.</span></span>

<span data-ttu-id="06341-118">使用執行的提供者。INI 檔案和效能 DLL 通常稱為 **V1 提供者**。</span><span class="sxs-lookup"><span data-stu-id="06341-118">Providers implemented using an .INI file and a performance DLL are often called **V1 providers**.</span></span>

> [!CAUTION]
> <span data-ttu-id="06341-119">雖然您仍然可以使用效能 DLL 來提供計數器資料，但此架構已被取代，因為效能和可靠性有顯著的限制。</span><span class="sxs-lookup"><span data-stu-id="06341-119">Although you can still use a performance DLL to provide counter data, this architecture is deprecated due to significant performance and reliability limitations.</span></span> <span data-ttu-id="06341-120">此外，V1 提供者通常較難實行，因為它們需要傳送必須在取用者進程中執行的個別 DLL。</span><span class="sxs-lookup"><span data-stu-id="06341-120">In addition, V1 providers are often harder to implement since they require shipping a separate DLL that must run in the consumer's process.</span></span>

<span data-ttu-id="06341-121">如需詳細資訊，請參閱 [使用效能 DLL 提供計數器資料](providing-counter-data-using-a-performance-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="06341-121">For details, see [Providing Counter Data Using a Performance DLL](providing-counter-data-using-a-performance-dll.md).</span></span>
