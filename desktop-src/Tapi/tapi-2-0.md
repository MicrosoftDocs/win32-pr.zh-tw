---
description: TAPI 2.0 針對基本的 TAPI 1.4 功能提供少量的增強功能。
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319147"
---
# <a name="tapi-20"></a><span data-ttu-id="80ec6-103">TAPI 2。0</span><span class="sxs-lookup"><span data-stu-id="80ec6-103">TAPI 2.0</span></span>

<span data-ttu-id="80ec6-104">TAPI 2.0 針對基本的 TAPI 1.4 功能提供少量的增強功能。</span><span class="sxs-lookup"><span data-stu-id="80ec6-104">TAPI 2.0 provides a small number of enhancements to the basic TAPI 1.4 functionality.</span></span> <span data-ttu-id="80ec6-105">不過，有一些主要的架構變更大幅改善其穩定性。</span><span class="sxs-lookup"><span data-stu-id="80ec6-105">However, there were some major architectural changes that greatly improved its stability.</span></span> <span data-ttu-id="80ec6-106">大部分的變更都是將 TAPI 帶入 Windows NT 4.0 所需的基本變更，並充分利用其功能 (完整的32位支援、服務和 Unicode) 。</span><span class="sxs-lookup"><span data-stu-id="80ec6-106">Most of the changes were fundamental changes necessary to bring TAPI to Windows NT 4.0 and take advantage of its features (full 32-bit support, services, and Unicode).</span></span> <span data-ttu-id="80ec6-107">不過，這些變更是 TAPI 內部的變更，對 TAPI 應用程式的影響很小。</span><span class="sxs-lookup"><span data-stu-id="80ec6-107">However, these changes were internal to TAPI and had little effect on TAPI applications.</span></span>

<span data-ttu-id="80ec6-108">透過 Thunking 層支援 TAPI 1.3 和 1.4 (16 位應用程式的應用程式，) 在 Windows Server 2003 作業系統、Windows XP、Windows 2000 和 Windows NT 上運作正常。</span><span class="sxs-lookup"><span data-stu-id="80ec6-108">Applications that support TAPI 1.3 and 1.4 (16-bit applications by way of a thunking layer) work well on Windows Server 2003 operating systems, Windows XP, Windows 2000, and Windows NT.</span></span> <span data-ttu-id="80ec6-109">不過，對服務提供者開發人員的影響相當重要。</span><span class="sxs-lookup"><span data-stu-id="80ec6-109">However, the effect on service-provider developers was significant.</span></span> <span data-ttu-id="80ec6-110">這些作業系統的服務提供者必須是完全32位的 Unicode Dll，這些 Dll 可以在 TAPISRV 的內容中執行，而不是在 TAPI 應用程式的內容中， (與所有先前的 Win16 Tsp) 。</span><span class="sxs-lookup"><span data-stu-id="80ec6-110">Service providers for these operating systems must be fully 32-bit Unicode DLLs that can run in the context of TAPISRV, not in the context of the TAPI application (as did all earlier Win16-based TSPs).</span></span> <span data-ttu-id="80ec6-111">針對 TAPI 1.4 所設計的 Tsp 無法在 Windows Server 2003 作業系統、Windows XP、Windows 2000 或 Windows NT 上運作。</span><span class="sxs-lookup"><span data-stu-id="80ec6-111">TSPs designed for TAPI 1.4 do not work on Windows Server 2003 operating systems, Windows XP, Windows 2000, or Windows NT.</span></span>

<span data-ttu-id="80ec6-112">TAPI 2.0 也新增了「撥打電話中心」支援的重要功能，以及 (QOS) 支援的服務品質。</span><span class="sxs-lookup"><span data-stu-id="80ec6-112">TAPI 2.0 also adds the important features of call center support and Quality of Service (QOS) support.</span></span>

<span data-ttu-id="80ec6-113">Windows 隨附的 TAPI 系統二進位檔支援所有應用程式的 TAPI 1.3 和1.4 版。</span><span class="sxs-lookup"><span data-stu-id="80ec6-113">The TAPI system binaries that come with Windows support TAPI versions 1.3 and 1.4 for all applications.</span></span> <span data-ttu-id="80ec6-114">不過，16位應用程式不能使用 TAPI 2.0，而且您不能使用16位 TAPI 的 TSP。</span><span class="sxs-lookup"><span data-stu-id="80ec6-114">However, 16-bit applications cannot use TAPI 2.0, and you cannot use a 16-bit TAPI 2.x TSP.</span></span>

 

 



