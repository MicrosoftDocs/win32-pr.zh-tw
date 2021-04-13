---
description: 從協調3.0 或更新版本的 Windows 2000 電話語音服務提供者開始，必須有相符的媒體服務提供者。
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: 媒體服務提供者通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321567"
---
# <a name="media-service-provider-communication"></a><span data-ttu-id="908f0-103">媒體服務提供者通訊</span><span class="sxs-lookup"><span data-stu-id="908f0-103">Media Service Provider Communication</span></span>

<span data-ttu-id="908f0-104">從協調3.0 或更新版本的 Windows 2000 電話語音服務提供者開始，必須有相符的媒體服務提供者。</span><span class="sxs-lookup"><span data-stu-id="908f0-104">Starting with Windows 2000 telephony service providers that negotiate a version of 3.0 or later must have a matching media service provider.</span></span> <span data-ttu-id="908f0-105">營運責任的精確劃分是實作為相依。</span><span class="sxs-lookup"><span data-stu-id="908f0-105">The precise division of operational responsibilities is implementation dependent.</span></span> <span data-ttu-id="908f0-106">例如，TSP 可能會使用相符的 MSP 來執行傳入會話的媒體類型判斷。</span><span class="sxs-lookup"><span data-stu-id="908f0-106">For example, a TSP might use the matching MSP to perform media type determination on an incoming session.</span></span> <span data-ttu-id="908f0-107">不過，TSP 必須符合 TSPI 的規定，這表示從 MSP 取得該判斷，並將其報告至 TAPI。</span><span class="sxs-lookup"><span data-stu-id="908f0-107">However, the TSP must conform to the TSPI, which means getting that determination from the MSP and reporting it to TAPI.</span></span>

<span data-ttu-id="908f0-108">TSPI 提供下列函式和訊息，以允許 TSP 和 MSP 之間的虛擬連接：</span><span class="sxs-lookup"><span data-stu-id="908f0-108">TSPI provides the following functions and messages to allow a virtual connection between a TSP and an MSP:</span></span>

-   [<span data-ttu-id="908f0-109">**TSPI \_ lineCloseMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="908f0-109">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="908f0-110">**TSPI \_ lineCreateMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="908f0-110">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="908f0-111">**TSPI \_ lineMSPIdentify**</span><span class="sxs-lookup"><span data-stu-id="908f0-111">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="908f0-112">**TSPI \_ lineReceiveMSPData**</span><span class="sxs-lookup"><span data-stu-id="908f0-112">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="908f0-113">**行 \_ QOSINFO**</span><span class="sxs-lookup"><span data-stu-id="908f0-113">**LINE\_QOSINFO**</span></span>](line-qosinfo.md)
-   [<span data-ttu-id="908f0-114">**行 \_ SENDMSPDATA**</span><span class="sxs-lookup"><span data-stu-id="908f0-114">**LINE\_SENDMSPDATA**</span></span>](line-sendmspdata.md)

 

 
