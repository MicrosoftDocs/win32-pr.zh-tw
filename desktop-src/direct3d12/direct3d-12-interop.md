---
title: 使用 Direct3D 11、Direct3D 10 和 Direct2D
description: 本節涵蓋使用舊版 Direct3D 和 Direct2D 的 interop 技術、Direct3D 11on12 API，以及從 Direct3D 11 到 Direct3D 12 的移植指導方針。
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103612"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a><span data-ttu-id="5e81e-103">使用 Direct3D 11、Direct3D 10 和 Direct2D</span><span class="sxs-lookup"><span data-stu-id="5e81e-103">Working with Direct3D 11, Direct3D 10 and Direct2D</span></span>

<span data-ttu-id="5e81e-104">本節涵蓋使用舊版 Direct3D 和 Direct2D 的 interop 技術、Direct3D 11on12 API，以及從 Direct3D 11 到 Direct3D 12 的移植指導方針。</span><span class="sxs-lookup"><span data-stu-id="5e81e-104">This section covers interop techniques with earlier versions of Direct3D and Direct2D, the Direct3D 11on12 API, and porting guidelines from Direct3D 11 to Direct3D 12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5e81e-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="5e81e-105">In this section</span></span>



| <span data-ttu-id="5e81e-106">主題</span><span class="sxs-lookup"><span data-stu-id="5e81e-106">Topic</span></span>                                                                                             | <span data-ttu-id="5e81e-107">描述</span><span class="sxs-lookup"><span data-stu-id="5e81e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e81e-108">Direct3D 12 Interop</span><span class="sxs-lookup"><span data-stu-id="5e81e-108">Direct3D 12 Interop</span></span>](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | <span data-ttu-id="5e81e-109">D3D12 可以用來撰寫元件化應用程式。</span><span class="sxs-lookup"><span data-stu-id="5e81e-109">D3D12 can be used to write componentized applications.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="5e81e-110">Direct3D 11 on 12</span><span class="sxs-lookup"><span data-stu-id="5e81e-110">Direct3D 11 on 12</span></span>](direct3d-11-on-12.md)<br/>                                             | <span data-ttu-id="5e81e-111">D3D11On12 是一種機制，開發人員可以使用 D3D11 介面和物件來驅動 D3D12 API。</span><span class="sxs-lookup"><span data-stu-id="5e81e-111">D3D11On12 is a mechanism by which developers can use D3D11 interfaces and objects to drive the D3D12 API.</span></span> <span data-ttu-id="5e81e-112">D3D11on12 可讓使用 D3D11 撰寫的元件 (例如，D2D 文字和 UI) 與以 D3D12 API 為目標的元件一起運作。</span><span class="sxs-lookup"><span data-stu-id="5e81e-112">D3D11on12 enables components written using D3D11 (for example, D2D text and UI) to work together with components written targeting the D3D12 API.</span></span> <span data-ttu-id="5e81e-113">D3D11on12 也可讓應用程式從 D3D11 增量移植至 D3D12，方法是讓應用程式的某些部分繼續以較簡單的目標為目標，同時讓其他人以 D3D12 為效能，同時一律具有完整且正確的呈現。</span><span class="sxs-lookup"><span data-stu-id="5e81e-113">D3D11on12 also enables incremental porting of an application from D3D11 to D3D12, by enabling portions of the app to continue targeting D3D11 for simplicity while others target D3D12 for performance, while always having complete and correct rendering.</span></span> <span data-ttu-id="5e81e-114">D3D11On12 可讓您更輕鬆地使用 interop 技術來共用資源，並在兩個 Api 之間同步處理工作。</span><span class="sxs-lookup"><span data-stu-id="5e81e-114">D3D11On12 makes it simpler than using interop techniques to share resources and synchronize work between the two APIs.</span></span> <br/> |
| [<span data-ttu-id="5e81e-115">從 Direct3D 11 移植到 Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5e81e-115">Porting from Direct3D 11 to Direct3D 12</span></span>](porting-from-direct3d-11-to-direct3d-12.md)<br/> | <span data-ttu-id="5e81e-116">本節提供從自訂 Direct3D 11 圖形引擎移植到 Direct3D 12 的一些指引。</span><span class="sxs-lookup"><span data-stu-id="5e81e-116">This section provides some guidance on porting from a custom Direct3D 11 graphics engine to Direct3D 12.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="5e81e-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="5e81e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e81e-118">Direct3D 12 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="5e81e-118">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





