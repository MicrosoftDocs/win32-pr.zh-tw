---
title: Direct3D 11 圖形
description: Direct3D 11 圖形
ms.assetid: 11413056-5033-4b4f-b80c-fccccb4057bc
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f154ddfc97dff17f061be41c818b4f56151b135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315769"
---
# <a name="direct3d-11-graphics"></a><span data-ttu-id="ff589-103">Direct3D 11 圖形</span><span class="sxs-lookup"><span data-stu-id="ff589-103">Direct3D 11 Graphics</span></span>

<span data-ttu-id="ff589-104">您可以使用 Microsoft Direct3D 11 圖形來建立適用于遊戲和科學和桌面應用程式的立體圖形。</span><span class="sxs-lookup"><span data-stu-id="ff589-104">You can use Microsoft Direct3D 11 graphics to create 3-D graphics for games and scientific and desktop applications.</span></span>

<span data-ttu-id="ff589-105">本章節包含使用 Direct3D 11 圖形進行程式設計的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ff589-105">This section contains information about programming with Direct3D 11 graphics.</span></span>

<span data-ttu-id="ff589-106">如需詳細資訊，請參閱 [Direct3D 11 功能](direct3d-11-features.md)。</span><span class="sxs-lookup"><span data-stu-id="ff589-106">For more information, see [Direct3D 11 Features](direct3d-11-features.md).</span></span>



|                                   |                                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff589-107">支援的執行時間環境</span><span class="sxs-lookup"><span data-stu-id="ff589-107">Supported runtime environments</span></span>    | <dl> <span data-ttu-id="ff589-108"><dt>Windows/c + +</dt></span><span class="sxs-lookup"><span data-stu-id="ff589-108"><dt>Windows/C++</dt></span></span> </dl>            |
| <span data-ttu-id="ff589-109">建議的程式設計語言</span><span class="sxs-lookup"><span data-stu-id="ff589-109">Recommended programming languages</span></span> | <span data-ttu-id="ff589-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="ff589-110">C/C++</span></span>                                                                                             |
| <span data-ttu-id="ff589-111">最低支援用戶端</span><span class="sxs-lookup"><span data-stu-id="ff589-111">Minimum supported Client</span></span>          | <dl> <span data-ttu-id="ff589-112"><dt>Windows 7</dt></span><span class="sxs-lookup"><span data-stu-id="ff589-112"><dt>Windows 7</dt></span></span> </dl>              |
| <span data-ttu-id="ff589-113">最低支援伺服器</span><span class="sxs-lookup"><span data-stu-id="ff589-113">Minimum supported Server</span></span>          | <dl> <span data-ttu-id="ff589-114"><dt>Windows Server 2008 R2</dt></span><span class="sxs-lookup"><span data-stu-id="ff589-114"><dt>Windows Server 2008 R2</dt></span></span> </dl> |

 

| <span data-ttu-id="ff589-115">主題</span><span class="sxs-lookup"><span data-stu-id="ff589-115">Topic</span></span>                                                                          | <span data-ttu-id="ff589-116">描述</span><span class="sxs-lookup"><span data-stu-id="ff589-116">Description</span></span>                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff589-117">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ff589-117">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)<br/>                | <span data-ttu-id="ff589-118">本節示範如何使用 Direct3D 11 API 來完成數個常見工作。</span><span class="sxs-lookup"><span data-stu-id="ff589-118">This section demonstrates how to use the Direct3D 11 API to accomplish several common tasks.</span></span><br/>                                                                                               |
| [<span data-ttu-id="ff589-119">Direct3D 11 的新功能</span><span class="sxs-lookup"><span data-stu-id="ff589-119">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)<br/> | <span data-ttu-id="ff589-120">本節說明在 Direct3D 11、Direct3D 11.1 和 Direct3D 11.2 中新增的功能。</span><span class="sxs-lookup"><span data-stu-id="ff589-120">This section describes features added in Direct3D 11, Direct3D 11.1, and Direct3D 11.2.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="ff589-121">Direct3D 11 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="ff589-121">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)<br/>      | <span data-ttu-id="ff589-122">程式設計指南包含如何使用 Direct3D 11 可程式化管線，為遊戲以及科學和桌面應用程式建立即時3D 圖形的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ff589-122">The programming guide contains information about how to use the Direct3D 11 programmable pipeline to create realtime 3D graphics for games as well as scientific and desktop applications.</span></span><br/> |
| [<span data-ttu-id="ff589-123">Direct3D 11 參考</span><span class="sxs-lookup"><span data-stu-id="ff589-123">Direct3D 11 Reference</span></span>](atoc-d3d11-graphics-reference.md)<br/>          | <span data-ttu-id="ff589-124">本節包含 Direct3D 11 圖形程式設計的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="ff589-124">This section contains the reference pages for Direct3D 11-based graphics programming.</span></span><br/>                                                                                                      |



 

<span data-ttu-id="ff589-125">除了 Windows 7 及更新版本以及 Windows Server 2008 R2 和更新版本所支援的 Direct3D 11 之外，還可以下載適用于 Windows Vista Service Pack 2 (SP2) 和 Windows Server 2008 的舊版，方法是下載 [KB 971644](https://support.microsoft.com/kb/971644) 和 [kb 971512](https://support.microsoft.com/kb/971512/)。</span><span class="sxs-lookup"><span data-stu-id="ff589-125">In addition to Direct3D 11 being supported by Windows 7 and later and Windows Server 2008 R2 and later, Direct3D 11 is available down-level for Windows Vista with Service Pack 2 (SP2) and Windows Server 2008 by downloading [KB 971644](https://support.microsoft.com/kb/971644) and [KB 971512](https://support.microsoft.com/kb/971512/).</span></span>

<span data-ttu-id="ff589-126">如需 Windows 8、Windows Server 2012 隨附之新 Direct3D 11.1 功能的相關資訊，以及透過 Windows 7 的 [Platform update](https://support.microsoft.com/kb/2670838)在 windows 7 和 windows Server 2008 R2 部分提供的相關資訊，請參閱 [Direct3D 11.1 功能](direct3d-11-1-features.md) 和 [windows 7 的平臺更新](/windows/desktop/direct3darticles/platform-update-for-windows-7)。</span><span class="sxs-lookup"><span data-stu-id="ff589-126">For info about new Direct3D 11.1 features that are included with Windows 8, Windows Server 2012, and are partially available on Windows 7 and Windows Server 2008 R2 via the [Platform Update for Windows 7](https://support.microsoft.com/kb/2670838), see [Direct3D 11.1 Features](direct3d-11-1-features.md) and the [Platform Update for Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7).</span></span>

 

