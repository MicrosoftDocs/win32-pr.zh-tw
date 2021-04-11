---
description: 鬆散結合的 Internet Explorer (LCIE) 藉由分隔元件的元件並放寬其類型，來改善瀏覽器的可靠性。
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Windows 7 和 Windows Server 2008 R2 應用程式品質指南) 的架構 (
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695363"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="4df69-103">Windows 7 和 Windows Server 2008 R2 應用程式品質指南) 的架構 (</span><span class="sxs-lookup"><span data-stu-id="4df69-103">Architecture (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="4df69-104">*鬆散結合的 Internet Explorer* (LCIE) 藉由分隔元件的元件並放寬其類型，來改善瀏覽器的可靠性。</span><span class="sxs-lookup"><span data-stu-id="4df69-104">*Loosely-coupled Internet Explorer* (LCIE) improves the browser’s reliability by separating its components and loosening their interdependence.</span></span>

<span data-ttu-id="4df69-105">尤其是，LCIE 會嘗試將 Windows Internet Explorer 框架和其索引標籤隔離到個別的進程。</span><span class="sxs-lookup"><span data-stu-id="4df69-105">In particular, LCIE tries to isolate the Windows Internet Explorer frame and its tabs into separate processes.</span></span> <span data-ttu-id="4df69-106">在 Windows Internet Explorer 8 中，此隔離可改善效能和擴充性。</span><span class="sxs-lookup"><span data-stu-id="4df69-106">In Windows Internet Explorer 8, this isolation improves performance and scalability.</span></span> <span data-ttu-id="4df69-107">此架構變更可能會影響延伸模組和附加元件的相容性，包括 ActiveX 控制項、瀏覽器協助程式物件 (Bho) ，以及使用舊版程式設計技術建立的 UI 工具列元件。</span><span class="sxs-lookup"><span data-stu-id="4df69-107">This architectural change might affect the compatibility of extensions and add-ons, including ActiveX Controls, Browser Helper Objects (BHOs), and UI toolbar components that are built by using older programming techniques.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4df69-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="4df69-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4df69-109">設計影響瀏覽器相容性的更新</span><span class="sxs-lookup"><span data-stu-id="4df69-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



