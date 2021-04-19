---
title: Windows 色彩系統
description: 色彩管理配置可在 Microsoft Windows 作業系統中執行，以改善各種數位通訊形式的色彩內容呈現。從 Windows 2000、Windows XP 及 Windows Server 2003 開始使用的色彩管理配置稱為影像色彩管理 (ICM) 2.0。 從 Windows Vista 開始使用的色彩管理配置稱為 Windows Color System (WCS) 1.0。 WCS 1.0 色彩管理配置是 ICM 2.0 Api 和功能的超集合。
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ccb84caa4ff10ab4c97115b9759730cd0ef26
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106976409"
---
# <a name="windows-color-system"></a><span data-ttu-id="c53cd-105">Windows 色彩系統</span><span class="sxs-lookup"><span data-stu-id="c53cd-105">Windows Color System</span></span>

## <a name="purpose"></a><span data-ttu-id="c53cd-106">目的</span><span class="sxs-lookup"><span data-stu-id="c53cd-106">Purpose</span></span>

<span data-ttu-id="c53cd-107">色彩管理配置可在 Microsoft Windows 作業系統中執行，以改善各種數位通訊形式的色彩內容呈現。</span><span class="sxs-lookup"><span data-stu-id="c53cd-107">Color management schemes are implemented in Microsoft Windows operating systems to improve the rendering of color content in all forms of digital communication.</span></span>

<span data-ttu-id="c53cd-108">從 Windows 2000、Windows XP 及 Windows Server 2003 開始使用的色彩管理配置稱為影像色彩管理 (ICM) 2.0。</span><span class="sxs-lookup"><span data-stu-id="c53cd-108">The color management scheme that's used starting with Windows 2000, Windows XP, and Windows Server 2003 is called Image Color Management (ICM) 2.0.</span></span> <span data-ttu-id="c53cd-109">從 Windows Vista 開始使用的色彩管理配置稱為 Windows Color System (WCS) 1.0。</span><span class="sxs-lookup"><span data-stu-id="c53cd-109">The color management scheme that's used starting with Windows Vista is called Windows Color System (WCS) 1.0.</span></span> <span data-ttu-id="c53cd-110">WCS 1.0 色彩管理配置是 ICM 2.0 Api 和功能的超集合。</span><span class="sxs-lookup"><span data-stu-id="c53cd-110">The WCS 1.0 color management scheme is a superset of ICM 2.0 APIs and functionality.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="c53cd-111">適用時</span><span class="sxs-lookup"><span data-stu-id="c53cd-111">Where applicable</span></span>

<span data-ttu-id="c53cd-112">ICM 可用於 Windows 2000 和更新版本作業系統上的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="c53cd-112">ICM can be used in all applications on Windows 2000 and later operating systems.</span></span> <span data-ttu-id="c53cd-113">WCS 可用於 Windows Vista 和更新版本的作業系統上的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="c53cd-113">WCS can be used in all applications on Windows Vista and later operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c53cd-114">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="c53cd-114">Developer audience</span></span>

<span data-ttu-id="c53cd-115">WCS API 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="c53cd-115">The WCS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="c53cd-116">您必須熟悉 Windows 圖形化使用者介面、訊息驅動架構，以及色彩管理概念的工作知識。</span><span class="sxs-lookup"><span data-stu-id="c53cd-116">Familiarity with the Windows graphical user interface, message-driven architecture, and a working knowledge of color management concepts are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c53cd-117">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="c53cd-117">Run-time requirements</span></span>

<span data-ttu-id="c53cd-118">使用 ICM API 的應用程式需要 Windows 2000 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c53cd-118">Applications that use the ICM API require Windows 2000 or later.</span></span> <span data-ttu-id="c53cd-119">使用 WCS API 的應用程式需要 Windows Vista 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c53cd-119">Applications that use the WCS API require Windows Vista or later.</span></span> <span data-ttu-id="c53cd-120">如需函式的特定執行時間資訊，請參閱該函式之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="c53cd-120">For specific run-time information on a function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c53cd-121">本節內容</span><span class="sxs-lookup"><span data-stu-id="c53cd-121">In this section</span></span>

-   [<span data-ttu-id="c53cd-122">安全性考慮： Windows 色彩系統</span><span class="sxs-lookup"><span data-stu-id="c53cd-122">Security Considerations: Windows Color System</span></span>](security-considerations--windows-color-system.md)
-   [<span data-ttu-id="c53cd-123">基本色彩管理概念</span><span class="sxs-lookup"><span data-stu-id="c53cd-123">Basic color management concepts</span></span>](basic-color-management-concepts.md)
-   [<span data-ttu-id="c53cd-124">Windows 色彩系統架構和演算法</span><span class="sxs-lookup"><span data-stu-id="c53cd-124">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
-   [<span data-ttu-id="c53cd-125">關於 Windows Color System 版本1。0</span><span class="sxs-lookup"><span data-stu-id="c53cd-125">About Windows Color System Version 1.0</span></span>](about-windows-color-system-version-1-0.md)
-   [<span data-ttu-id="c53cd-126">使用 WCS 1。0</span><span class="sxs-lookup"><span data-stu-id="c53cd-126">Using WCS 1.0</span></span>](using-wcs-1-0.md)
-   [<span data-ttu-id="c53cd-127">參考</span><span class="sxs-lookup"><span data-stu-id="c53cd-127">Reference</span></span>](reference.md)
-   [<span data-ttu-id="c53cd-128">WCS 1.0 詞彙</span><span class="sxs-lookup"><span data-stu-id="c53cd-128">WCS 1.0 Glossary</span></span>](wcs-1-0-glossary.md)

## <a name="related-topics"></a><span data-ttu-id="c53cd-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="c53cd-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c53cd-130">Opengl</span><span class="sxs-lookup"><span data-stu-id="c53cd-130">OpenGL</span></span>](../opengl/introduction-to-opengl.md)
</dt> <dt>

[<span data-ttu-id="c53cd-131">Windows 多媒體</span><span class="sxs-lookup"><span data-stu-id="c53cd-131">Windows Multimedia</span></span>](../multimedia/windows-multimedia-start-page.md)
</dt> <dt>

[<span data-ttu-id="c53cd-132">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="c53cd-132">Windows GDI</span></span>](../gdi/windows-gdi.md)
</dt> </dl>

 

 