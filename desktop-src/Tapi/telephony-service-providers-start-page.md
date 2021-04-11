---
description: 電話語音服務提供者 (TSP) 是動態連結程式庫 (DLL) ，可透過一組匯出的服務功能來支援通訊裝置控制項。
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: 電話語音服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852028"
---
# <a name="telephony-service-providers"></a><span data-ttu-id="51329-103">電話語音服務提供者</span><span class="sxs-lookup"><span data-stu-id="51329-103">Telephony Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="51329-104">目的</span><span class="sxs-lookup"><span data-stu-id="51329-104">Purpose</span></span>

<span data-ttu-id="51329-105">電話語音服務提供者 (TSP) 是動態連結程式庫 (DLL) ，可透過一組匯出的服務功能來支援通訊裝置控制項。</span><span class="sxs-lookup"><span data-stu-id="51329-105">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="51329-106">TAPI 應用程式使用標準化的命令、TAPI 會將資訊傳遞給電話語音服務提供者，而 TSP 則會處理必須與裝置交換的特定命令。</span><span class="sxs-lookup"><span data-stu-id="51329-106">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="51329-107">TSP 必須符合電話語音服務提供者介面 (TSPI) ，才能以 Microsoft 電話語音環境內的服務提供者形式運作。</span><span class="sxs-lookup"><span data-stu-id="51329-107">A TSP must conform to the Telephony Service Provider Interface (TSPI) to function as a service provider within the Microsoft Telephony environment.</span></span> <span data-ttu-id="51329-108">TSPI 會定義由通訊設備提供的電話語音服務提供者所公開的外部函數。</span><span class="sxs-lookup"><span data-stu-id="51329-108">TSPI defines the external functions exposed by a telephony service provider supplied with communications equipment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="51329-109">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="51329-109">Developer audience</span></span>

<span data-ttu-id="51329-110">您可以用多種語言撰寫啟用 TAPI 的應用程式，包括 JAVA、Visual Basic 和 C/c + +。</span><span class="sxs-lookup"><span data-stu-id="51329-110">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="51329-111">使用電信或其他電話語音應用程式的先前開發經驗很有説明，但並非必要。</span><span class="sxs-lookup"><span data-stu-id="51329-111">Previous development experience with telecommunications or other telephony applications is helpful but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="51329-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="51329-112">Run-time requirements</span></span>

<span data-ttu-id="51329-113">TSPI 可讓您開發所有 Windows 版本的 Tsp。</span><span class="sxs-lookup"><span data-stu-id="51329-113">TSPI enables development of TSPs for all versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="51329-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="51329-114">In this section</span></span>



| <span data-ttu-id="51329-115">主題</span><span class="sxs-lookup"><span data-stu-id="51329-115">Topic</span></span>                                                                | <span data-ttu-id="51329-116">描述</span><span class="sxs-lookup"><span data-stu-id="51329-116">Description</span></span>                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="51329-117">概觀</span><span class="sxs-lookup"><span data-stu-id="51329-117">Overview</span></span>](about-the-telephony-service-provider-tsp-.md)<br/> | <span data-ttu-id="51329-118">關於 TSPI 架構和元件的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="51329-118">General information about TSPI's architecture and components.</span></span><br/> |
| [<span data-ttu-id="51329-119">參考</span><span class="sxs-lookup"><span data-stu-id="51329-119">Reference</span></span>](tspi-reference.md)<br/>                           | <span data-ttu-id="51329-120">TSPI 介面的檔。</span><span class="sxs-lookup"><span data-stu-id="51329-120">Documentation for the TSPI interfaces.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="51329-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="51329-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51329-122">Microsoft 電話語音總覽</span><span class="sxs-lookup"><span data-stu-id="51329-122">Microsoft Telephony Overview</span></span>](./microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="51329-123">媒體服務提供者</span><span class="sxs-lookup"><span data-stu-id="51329-123">Media Service Providers</span></span>](./media-service-providers-start-page.md)
</dt> <dt>

[<span data-ttu-id="51329-124">TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="51329-124">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="51329-125">TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="51329-125">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> </dl>

 

