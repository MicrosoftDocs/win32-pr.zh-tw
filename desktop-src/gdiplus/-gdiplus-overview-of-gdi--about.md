---
description: Windows GDI + 是 Windows XP 作業系統或 Windows Server 2003 的子系統，負責顯示畫面和印表機的資訊。 GDI + 是透過一組 c + + 類別公開的 API。
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: GDI + 簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991318"
---
# <a name="overview-of-gdi"></a><span data-ttu-id="18712-104">GDI + 簡介</span><span class="sxs-lookup"><span data-stu-id="18712-104">Overview of GDI+</span></span>

<span data-ttu-id="18712-105">Windows GDI + 是 Windows XP 作業系統或 Windows Server 2003 的子系統，負責顯示畫面和印表機的資訊。</span><span class="sxs-lookup"><span data-stu-id="18712-105">Windows GDI+ is the subsystem of the Windows XP operating system or Windows Server 2003 that is responsible for displaying information on screens and printers.</span></span> <span data-ttu-id="18712-106">GDI + 是透過一組 c + + 類別公開的 API。</span><span class="sxs-lookup"><span data-stu-id="18712-106">GDI+ is an API that is exposed through a set of C++ classes.</span></span>

<span data-ttu-id="18712-107">正如其名所示，GDI + 是 Windows 圖形裝置介面 (GDI) 的後續版本，包括在舊版 Windows 中的圖形裝置介面。</span><span class="sxs-lookup"><span data-stu-id="18712-107">As its name suggests, GDI+ is the successor to Windows Graphics Device Interface (GDI), the graphics device interface included with earlier versions of Windows.</span></span> <span data-ttu-id="18712-108">Windows XP 或 Windows Server 2003 支援 GDI，以與現有的應用程式相容，但新應用程式的程式設計人員應該針對其所有圖形需求使用 GDI +，因為 GDI + 會優化許多 GDI 的功能，同時也提供額外的功能。</span><span class="sxs-lookup"><span data-stu-id="18712-108">Windows XP or Windows Server 2003 supports GDI for compatibility with existing applications, but programmers of new applications should use GDI+ for all their graphics needs because GDI+ optimizes many of the capabilities of GDI and also provides additional features.</span></span>

<span data-ttu-id="18712-109">圖形裝置介面（例如 GDI +）可讓應用程式設計人員在螢幕或印表機上顯示資訊，而不需要擔心特定顯示裝置的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="18712-109">A graphics device interface, such as GDI+, allows application programmers to display information on a screen or printer without having to be concerned about the details of a particular display device.</span></span> <span data-ttu-id="18712-110">應用程式程式設計師會呼叫 GDI + 類別所提供的方法，而這些方法接著會對特定設備磁碟機進行適當的呼叫。</span><span class="sxs-lookup"><span data-stu-id="18712-110">The application programmer makes calls to methods provided by GDI+ classes and those methods in turn make the appropriate calls to specific device drivers.</span></span> <span data-ttu-id="18712-111">GDI + 會將應用程式與圖形硬體隔離，而這是一種可讓開發人員建立裝置獨立應用程式的保溫。</span><span class="sxs-lookup"><span data-stu-id="18712-111">GDI+ insulates the application from the graphics hardware, and it is this insulation that allows developers to create device-independent applications.</span></span>

 

 



