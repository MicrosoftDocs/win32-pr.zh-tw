---
title: Direct3D 11 的新功能
description: 本節說明在 Direct3D 11、Direct3D 11.1 和 Direct3D 11.2 中新增的功能。
ms.assetid: 08ad078f-9bc6-4f23-8faa-ccf168e79c2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d180867fd996b0e3ebe2482448e73617f55a16d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990915"
---
# <a name="whats-new-in-direct3d-11"></a><span data-ttu-id="f3b07-103">Direct3D 11 的新功能</span><span class="sxs-lookup"><span data-stu-id="f3b07-103">What's new in Direct3D 11</span></span>

<span data-ttu-id="f3b07-104">本節說明在 Direct3D 11、Direct3D 11.1 和 Direct3D 11.2 中新增的功能。</span><span class="sxs-lookup"><span data-stu-id="f3b07-104">This section describes features added in Direct3D 11, Direct3D 11.1, and Direct3D 11.2.</span></span>

<span data-ttu-id="f3b07-105">Microsoft Direct3D 11 是 Microsoft Direct3D 10/Microsoft Direct3D 10.1 轉譯 API 的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="f3b07-105">Microsoft Direct3D 11 is an extension of the Microsoft Direct3D 10/Microsoft Direct3D 10.1 rendering API.</span></span> <span data-ttu-id="f3b07-106">如需有關使用 Direct3D 11 的簡介資訊，請參閱 [direct3d 10 的程式設計指南](/windows/desktop/direct3d10/d3d10-graphics-programming-guide)。</span><span class="sxs-lookup"><span data-stu-id="f3b07-106">For more introductory material about using Direct3D 11, see the [Programming Guide for Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f3b07-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="f3b07-107">In this section</span></span>



| <span data-ttu-id="f3b07-108">主題</span><span class="sxs-lookup"><span data-stu-id="f3b07-108">Topic</span></span>                                                                                                  | <span data-ttu-id="f3b07-109">描述</span><span class="sxs-lookup"><span data-stu-id="f3b07-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3b07-110">Direct3D 11 功能</span><span class="sxs-lookup"><span data-stu-id="f3b07-110">Direct3D 11 Features</span></span>](direct3d-11-features.md)<br/>                                            | <span data-ttu-id="f3b07-111">程式設計指南包含如何使用 Direct3D 11 可程式化管線，為遊戲以及科學和桌面應用程式建立即時3D 圖形的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3b07-111">The programming guide contains information about how to use the Direct3D 11 programmable pipeline to create realtime 3D graphics for games, and for scientific and desktop applications.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="f3b07-112">Direct3D 11.1 功能</span><span class="sxs-lookup"><span data-stu-id="f3b07-112">Direct3D 11.1 Features</span></span>](direct3d-11-1-features.md)<br/>                                        | <span data-ttu-id="f3b07-113">以下是在 Direct3D 11.1 中新增的功能，其中包含在 Windows 8、Windows RT 和 Windows Server 2012 中。</span><span class="sxs-lookup"><span data-stu-id="f3b07-113">The following functionality has been added in Direct3D 11.1, which is included with Windows 8, Windows RT, and Windows Server 2012.</span></span> <span data-ttu-id="f3b07-114">您可以透過 windows 7 的平臺[更新，在](/windows/desktop/direct3darticles/platform-update-for-windows-7)windows 7 和 windows Server 2008 R2 上取得[Direct3D 11.1](direct3d-11-features.md)的部分支援（可透過[windows 7 的平臺更新取得](https://support.microsoft.com/kb/2670838)）。</span><span class="sxs-lookup"><span data-stu-id="f3b07-114">Partial support for [Direct3D 11.1](direct3d-11-features.md) is available on Windows 7 and Windows Server 2008 R2 via the [Platform Update for Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), which is available through the [Platform Update for Windows 7](https://support.microsoft.com/kb/2670838).</span></span><br/> |
| [<span data-ttu-id="f3b07-115">Direct3D 11.2 功能</span><span class="sxs-lookup"><span data-stu-id="f3b07-115">Direct3D 11.2 Features</span></span>](direct3d-11-2-features.md)<br/>                                        | <span data-ttu-id="f3b07-116">下列是在 Direct3D 11.2 中新增的功能，包括在 Windows 8.1、Windows RT 8.1 和 Windows Server 2012 R2 中。</span><span class="sxs-lookup"><span data-stu-id="f3b07-116">The following functionality has been added in Direct3D 11.2, which is included with Windows 8.1, Windows RT 8.1, and Windows Server 2012 R2.</span></span><br/>                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f3b07-117">Direct3D 11.3 功能</span><span class="sxs-lookup"><span data-stu-id="f3b07-117">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)<br/>                                        | <span data-ttu-id="f3b07-118">下列各節說明 Direct3D 11.3 中已新增的功能。</span><span class="sxs-lookup"><span data-stu-id="f3b07-118">The following sections describe the functionality has been added in Direct3D 11.3.</span></span> <span data-ttu-id="f3b07-119">這些功能也可在 Direct3D 12 中使用。</span><span class="sxs-lookup"><span data-stu-id="f3b07-119">These features are also available in Direct3D 12.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f3b07-120">Direct3D 11.4 功能</span><span class="sxs-lookup"><span data-stu-id="f3b07-120">Direct3D 11.4 Features</span></span>](direct3d-11-4-features.md)<br/>                                        | <span data-ttu-id="f3b07-121">Direct3D 11.4 已新增下列功能。</span><span class="sxs-lookup"><span data-stu-id="f3b07-121">The following functionality has been added in Direct3D 11.4.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="f3b07-122">先前版本中引進的功能</span><span class="sxs-lookup"><span data-stu-id="f3b07-122">Features Introduced In Previous Releases</span></span>](d3d11-features-introduced-previous-releases.md)<br/> | <span data-ttu-id="f3b07-123">探索先前的 SDK 更新新增了哪些新功能：</span><span class="sxs-lookup"><span data-stu-id="f3b07-123">Discover what new features have been added to the previous SDK updates:</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="f3b07-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="f3b07-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3b07-125">Direct3D 11 圖形</span><span class="sxs-lookup"><span data-stu-id="f3b07-125">Direct3D 11 Graphics</span></span>](atoc-dx-graphics-direct3d-11.md)
</dt> </dl>

 

