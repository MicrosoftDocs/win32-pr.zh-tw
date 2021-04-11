---
description: Microsoft 電話語音應用程式開發介面支援針對 Microsoft Windows 進行通訊應用程式的開發。 下表列出電話語音介面。
ms.assetid: e7348296-ee2d-4e0a-b274-3563dccea841
title: 電話語音應用程式設計介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19fd6a520c8a53440967eeef753b7ed8c90ba5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852031"
---
# <a name="telephony-application-programming-interfaces"></a><span data-ttu-id="b9d63-104">電話語音應用程式設計介面</span><span class="sxs-lookup"><span data-stu-id="b9d63-104">Telephony Application Programming Interfaces</span></span>

<span data-ttu-id="b9d63-105">Microsoft 電話語音應用程式開發介面支援針對 Microsoft Windows 進行通訊應用程式的開發。</span><span class="sxs-lookup"><span data-stu-id="b9d63-105">The Microsoft telephony application programming interfaces support the development of communications applications for Microsoft Windows.</span></span> <span data-ttu-id="b9d63-106">下表列出電話語音介面。</span><span class="sxs-lookup"><span data-stu-id="b9d63-106">The telephony interfaces are listed in the following table.</span></span>



| <span data-ttu-id="b9d63-107">介面</span><span class="sxs-lookup"><span data-stu-id="b9d63-107">Interface</span></span>                                                  | <span data-ttu-id="b9d63-108">描述</span><span class="sxs-lookup"><span data-stu-id="b9d63-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9d63-109">TAPI 2。x</span><span class="sxs-lookup"><span data-stu-id="b9d63-109">TAPI 2.x</span></span>](./tapi-2-2-start-page.md)               | <span data-ttu-id="b9d63-110">以 C 程式設計語言為基礎的 API，可讓您執行通訊應用程式，範圍從基本的數據機控制到使用多個代理程式和交換器的電話中心。</span><span class="sxs-lookup"><span data-stu-id="b9d63-110">A C-programming language based API that enables you to implement communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="b9d63-111">TAPI 3。x</span><span class="sxs-lookup"><span data-stu-id="b9d63-111">TAPI 3.x</span></span>](tapi-3-1-start-page.md)                        | <span data-ttu-id="b9d63-112">以 COM 為基礎的 API，可合併傳統和 IP 電話語音。</span><span class="sxs-lookup"><span data-stu-id="b9d63-112">A COM-based API that merges classic and IP telephony.</span></span>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="b9d63-113">TSPI</span><span class="sxs-lookup"><span data-stu-id="b9d63-113">TSPI</span></span>](./telephony-service-providers-start-page.md) | <span data-ttu-id="b9d63-114">電話語音服務提供者 (TSP) 是動態連結程式庫 (DLL) ，可透過一組匯出的服務功能來支援通訊裝置控制項。</span><span class="sxs-lookup"><span data-stu-id="b9d63-114">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="b9d63-115">TAPI 應用程式使用標準化的命令、TAPI 會將資訊傳遞給電話語音服務提供者，而 TSP 則會處理必須與裝置交換的特定命令。</span><span class="sxs-lookup"><span data-stu-id="b9d63-115">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span> |
| [<span data-ttu-id="b9d63-116">MSPI</span><span class="sxs-lookup"><span data-stu-id="b9d63-116">MSPI</span></span>](media-service-providers-start-page.md)             | <span data-ttu-id="b9d63-117">媒體服務提供者 (MSP) 可讓應用程式對特定傳輸機制的媒體具有相當大的控制權。</span><span class="sxs-lookup"><span data-stu-id="b9d63-117">A media service provider (MSP) allows an application considerable control over the media for a particular transport mechanism.</span></span> <span data-ttu-id="b9d63-118">MSP 一律與電話語音服務提供者 (TSP) 配對。</span><span class="sxs-lookup"><span data-stu-id="b9d63-118">An MSP is always paired with a telephony service provider (TSP).</span></span>                                                                                                                                                         |



 

 

 
