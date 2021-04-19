---
description: 要求物件是使用 COM CoCreateInstance 建立的，而且會公開一個介面 ITRequest。
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: 要求物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982413"
---
# <a name="request-object"></a><span data-ttu-id="3b787-103">要求物件</span><span class="sxs-lookup"><span data-stu-id="3b787-103">Request Object</span></span>

<span data-ttu-id="3b787-104">要求物件是使用 COM **CoCreateInstance** 建立的，而且會公開一個介面 [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)。</span><span class="sxs-lookup"><span data-stu-id="3b787-104">The Request Object is created using COM **CoCreateInstance** and exposes one interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest).</span></span> <span data-ttu-id="3b787-105">此介面會公開 [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) 方法，此方法可讓 TAPI 3 應用程式使用輔助電話語音。</span><span class="sxs-lookup"><span data-stu-id="3b787-105">This interface exposes the [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) method, which allows a TAPI 3 application to use Assisted Telephony.</span></span> <span data-ttu-id="3b787-106">輔助電話語音提供具備電話語音功能的應用程式，並使用簡單的機制來撥打電話，而不需要讓開發人員完全 >serilog.sinks.literate 電話語音。</span><span class="sxs-lookup"><span data-stu-id="3b787-106">Assisted Telephony provides telephony-enabled applications with a simple mechanism for making phone calls without requiring the developer to become fully literate in telephony.</span></span>

<span data-ttu-id="3b787-107">例如，試算表應用程式可以使用輔助電話語音新增「打撥」按鈕，而不需要執行完整 TAPI 應用程式中更詳盡的控制項。</span><span class="sxs-lookup"><span data-stu-id="3b787-107">For example, a spreadsheet application can add a "Make Call" button using Assisted Telephony without implementing the more elaborate controls available in a full TAPI application.</span></span>

<span data-ttu-id="3b787-108">如需其他資訊，請參閱「 [輔助電話語音」總覽](assisted-telephony-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="3b787-108">See the [Assisted Telephony Overview](assisted-telephony-overview.md) for additional information.</span></span>

 

 



