---
description: .
ms.assetid: c2094bbe-a4ca-4f30-b16e-14dced2912bc
title: Windows 屬性系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e96f931d37ef698339f9219a0dc8db43a6003e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971183"
---
# <a name="windows-property-system"></a><span data-ttu-id="3c586-103">Windows 屬性系統</span><span class="sxs-lookup"><span data-stu-id="3c586-103">Windows Property System</span></span>

## <a name="purpose"></a><span data-ttu-id="3c586-104">目的</span><span class="sxs-lookup"><span data-stu-id="3c586-104">Purpose</span></span>

<span data-ttu-id="3c586-105">Windows 屬性系統是資料定義的可擴充讀取/寫入系統，可提供統一的方式來表示 Shell 專案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3c586-105">The Windows Property System is an extensible read/write system of data definitions that provides a uniform way of expressing metadata about Shell items.</span></span> <span data-ttu-id="3c586-106">Windows Vista 和更新版本中的 Windows 屬性系統可讓您儲存和取得 Shell 專案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3c586-106">The Windows Property system in Windows Vista and later enables you to store and retrieve metadata for Shell items.</span></span> <span data-ttu-id="3c586-107">Shell 專案是任何一段內容，例如檔案、資料夾、電子郵件或連絡人。</span><span class="sxs-lookup"><span data-stu-id="3c586-107">A Shell item is any single piece of content, such as a file, folder, email, or contact.</span></span> <span data-ttu-id="3c586-108">屬性是與 Shell 專案相關聯之中繼資料的個別部分。</span><span class="sxs-lookup"><span data-stu-id="3c586-108">A property is an individual piece of metadata associated with a Shell item.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3c586-109">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="3c586-109">Developer audience</span></span>

<span data-ttu-id="3c586-110">開始閱讀 Windows 屬性系統 SDK 檔之前，您應該先瞭解下列各項的基本概念：</span><span class="sxs-lookup"><span data-stu-id="3c586-110">Before you start reading the Windows Property System SDK documentation, you should have a fundamental understanding of the following:</span></span>

-   <span data-ttu-id="3c586-111">元件物件模型 (COM)</span><span class="sxs-lookup"><span data-stu-id="3c586-111">Component Object Model (COM)</span></span>
-   <span data-ttu-id="3c586-112">Shell 命名空間程式設計</span><span class="sxs-lookup"><span data-stu-id="3c586-112">Shell Namespace programming</span></span>

<span data-ttu-id="3c586-113">如需 COM 的簡介，請參閱 [Com 基本](../com/com-fundamentals.md)概念。</span><span class="sxs-lookup"><span data-stu-id="3c586-113">For an introduction to COM, see [COM Fundamentals](../com/com-fundamentals.md).</span></span> <span data-ttu-id="3c586-114">如需 Shell 命名空間程式設計的簡介，請參閱 [使用 Shell 命名空間開始使用](../shell/namespace-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="3c586-114">For an introduction to Shell Namespace programming, see [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span></span>

<span data-ttu-id="3c586-115">如需使用 Windows 屬性系統的詳細說明，請參閱 [屬性系統總覽：開發案例](property-system-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="3c586-115">For uses of the Windows Property System, see [Property System Overview: Development Scenarios](property-system-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3c586-116">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="3c586-116">Run-time requirements</span></span>

<span data-ttu-id="3c586-117">使用 Windows 屬性系統的支援執行時間環境是 Windows Vista 或更新版本，而 Windows 軟體開發套件 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="3c586-117">The supported run-time environment for using the Windows Property System is Windows Vista or later and the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3c586-118">Windows XP 和 Microsoft Windows 桌面搜尋 (WDS) 3.0 或更新版本也包含 Windows 屬性系統的子集。</span><span class="sxs-lookup"><span data-stu-id="3c586-118">Windows XP and Microsoft Windows Desktop Search (WDS) 3.0 or later also include a subset of the Windows Property System.</span></span> <span data-ttu-id="3c586-119">若為 Windows 7 或更新版 Windows Vista SDK 下載，請參閱 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3c586-119">For the Windows 7 or updated Windows Vista SDK download, see the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3c586-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="3c586-120">In this section</span></span>

-   [<span data-ttu-id="3c586-121">屬性系統概觀</span><span class="sxs-lookup"><span data-stu-id="3c586-121">Property System Overview</span></span>](property-system-overview.md)
-   [<span data-ttu-id="3c586-122">Windows 屬性系統開發人員指南</span><span class="sxs-lookup"><span data-stu-id="3c586-122">Windows Property System Developer's Guide</span></span>](property-system-developer-s-guide.md)
-   [<span data-ttu-id="3c586-123">屬性系統參考</span><span class="sxs-lookup"><span data-stu-id="3c586-123">Property System Reference</span></span>](property-system-reference.md)
-   [<span data-ttu-id="3c586-124">屬性系統程式碼範例</span><span class="sxs-lookup"><span data-stu-id="3c586-124">Property System Code Samples</span></span>](property-system-code-samples.md)

 

 
