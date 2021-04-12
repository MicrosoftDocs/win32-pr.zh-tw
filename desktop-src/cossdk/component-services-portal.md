---
description: 擴充使用以 COM 為基礎的技術所撰寫的應用程式。
ms.assetid: b21a6b08-c17c-4fcc-bc60-39037bc9902f
title: 'COM + (元件服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b778c31957ddfe3f71db23b2f5be2a3ee681fde0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936264"
---
# <a name="com-component-services"></a><span data-ttu-id="e5fb0-103">COM + (元件服務) </span><span class="sxs-lookup"><span data-stu-id="e5fb0-103">COM+ (Component Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="e5fb0-104">目的</span><span class="sxs-lookup"><span data-stu-id="e5fb0-104">Purpose</span></span>

<span data-ttu-id="e5fb0-105">COM + 是 Microsoft 元件物件模型的演進， (COM) 和 Microsoft Transaction Server (MTS) 。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-105">COM+ is an evolution of Microsoft Component Object Model (COM) and Microsoft Transaction Server (MTS).</span></span> <span data-ttu-id="e5fb0-106">COM + 是以 COM、MTS 和其他以 COM 為基礎的技術為基礎，建立並擴充以撰寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-106">COM+ builds on and extends applications written using COM, MTS, and other COM-based technologies.</span></span> <span data-ttu-id="e5fb0-107">COM + 會處理您先前必須自行程式設計的許多資源管理工作，例如執行緒配置和安全性。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-107">COM+ handles many of the resource management tasks that you previously had to program yourself, such as thread allocation and security.</span></span> <span data-ttu-id="e5fb0-108">COM + 也藉由提供執行緒共用、物件共用和即時物件啟用，讓您的應用程式更具擴充性。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-108">COM+ also makes your applications more scalable by providing thread pooling, object pooling, and just-in-time object activation.</span></span> <span data-ttu-id="e5fb0-109">COM + 也會藉由提供交易支援來協助保護資料的完整性，即使交易橫跨網路的多個資料庫也是如此。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-109">COM+ also helps protect the integrity of your data by providing transaction support, even if a transaction spans multiple databases over a network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e5fb0-110">適用時</span><span class="sxs-lookup"><span data-stu-id="e5fb0-110">Where applicable</span></span>

<span data-ttu-id="e5fb0-111">COM + 可以用來開發適用于 Windows 的全企業、任務關鍵性、分散式應用程式。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-111">COM+ can be used to develop enterprise-wide, mission-critical, distributed applications for Windows.</span></span>

<span data-ttu-id="e5fb0-112">如果您是系統管理員，您將會安裝、部署及設定 COM + 應用程式及其元件。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-112">If you are a system administrator, you will be installing, deploying, and configuring COM+ applications and their components.</span></span> <span data-ttu-id="e5fb0-113">如果您是應用程式的程式設計人員，您將會撰寫元件，並將其與應用程式整合。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-113">If you are an application programmer, you will be writing components and integrating them as applications.</span></span> <span data-ttu-id="e5fb0-114">如果您是工具廠商，您將會開發或修改可在 COM + 環境中工作的工具。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-114">If you are a tools vendor, you will be developing or modifying tools to work in the COM+ environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e5fb0-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="e5fb0-115">Developer audience</span></span>

<span data-ttu-id="e5fb0-116">COM + 主要是針對 Microsoft Visual C++ 和 Microsoft Visual Basic 開發人員所設計。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-116">COM+ is designed primarily for Microsoft Visual C++ and Microsoft Visual Basic developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e5fb0-117">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="e5fb0-117">Run-time requirements</span></span>

<span data-ttu-id="e5fb0-118">從 Windows XP 和 Windows Server 2003 開始，Windows 中包含 COM + 1.5 版。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-118">COM+ version 1.5 is included in Windows starting with Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e5fb0-119">COM + 1.0 版包含在 Windows 2000 中。</span><span class="sxs-lookup"><span data-stu-id="e5fb0-119">COM+ version 1.0 is included in Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e5fb0-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="e5fb0-120">In this section</span></span>

-   [<span data-ttu-id="e5fb0-121">COM + 1.5 的新功能</span><span class="sxs-lookup"><span data-stu-id="e5fb0-121">What's New in COM+ 1.5</span></span>](what-s-new-in-com--1-5.md)
-   [<span data-ttu-id="e5fb0-122">COM + 開發人員總覽</span><span class="sxs-lookup"><span data-stu-id="e5fb0-122">COM+ Developers Overview</span></span>](com--developers-overview.md)
-   [<span data-ttu-id="e5fb0-123">COM + 服務</span><span class="sxs-lookup"><span data-stu-id="e5fb0-123">COM+ Services</span></span>](com--services.md)
-   [<span data-ttu-id="e5fb0-124">COM + 一般工作</span><span class="sxs-lookup"><span data-stu-id="e5fb0-124">COM+ General Tasks</span></span>](com--general-tasks.md)
-   [<span data-ttu-id="e5fb0-125">COM + 參考</span><span class="sxs-lookup"><span data-stu-id="e5fb0-125">COM+ Reference</span></span>](com--reference.md)

## <a name="related-topics"></a><span data-ttu-id="e5fb0-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5fb0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5fb0-127">COM</span><span class="sxs-lookup"><span data-stu-id="e5fb0-127">COM</span></span>](/windows/desktop/com/component-object-model--com--portal)
</dt> </dl>

 

 
