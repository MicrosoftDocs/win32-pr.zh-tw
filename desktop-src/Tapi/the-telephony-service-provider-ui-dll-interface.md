---
description: 在 Microsoft 電話語音中，電話語音服務提供者是在與電話語音應用程式不同的進程中執行。
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: 電話語音服務提供程式 UI DLL 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969351"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a><span data-ttu-id="d7e66-103">電話語音服務提供程式 UI DLL 介面</span><span class="sxs-lookup"><span data-stu-id="d7e66-103">The Telephony Service Provider UI DLL Interface</span></span>

<span data-ttu-id="d7e66-104">在 Microsoft 電話語音中，電話語音服務提供者是在與電話語音應用程式不同的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="d7e66-104">In Microsoft Telephony, telephony service providers execute in a separate process from telephony applications.</span></span> <span data-ttu-id="d7e66-105">服務提供者會透過電話語音服務提供者介面與 TAPISRV 通訊 (TSPI) 並在其處理常式中執行;應用程式介面至 TAPI，會載入至應用程式內容中。</span><span class="sxs-lookup"><span data-stu-id="d7e66-105">Service providers communicate with TAPISRV through the Telephony service provider interface (TSPI) and execute in its process; applications interface to TAPI, which are loaded in the application context.</span></span>

<span data-ttu-id="d7e66-106">TAPI 的元件使用各種處理序間通訊機制，在應用程式與服務提供者之間傳遞函式要求和訊息。</span><span class="sxs-lookup"><span data-stu-id="d7e66-106">The components of TAPI use various interprocess communications mechanisms to convey function requests and messages between applications and service providers.</span></span> <span data-ttu-id="d7e66-107">應用程式和服務提供者可能不只會在不同的進程中執行，而是在完全不同的系統上執行。</span><span class="sxs-lookup"><span data-stu-id="d7e66-107">The applications and the service providers may be executing not only in separate processes, but on completely separate systems.</span></span> <span data-ttu-id="d7e66-108">因此，服務提供者無法在進程中或甚至是在執行的電腦上顯示對話方塊;您必須在應用程式執行所在的電腦上，從應用程式內容中叫用 UI。</span><span class="sxs-lookup"><span data-stu-id="d7e66-108">Service providers therefore cannot display dialog boxes in the process or even on the computer on which they are executing; UI must be invoked from within the application context, on the computer on which the application is executing.</span></span>

<span data-ttu-id="d7e66-109">本節定義在應用程式內容中載入及叫用服務提供者 UI 函式的機制。</span><span class="sxs-lookup"><span data-stu-id="d7e66-109">This section defines the mechanism by which service provider UI functions are loaded and invoked within the application context.</span></span> <span data-ttu-id="d7e66-110">當應用程式不會以其他方式在應用程式中開啟對話方塊時，也會定義一個機制，讓服務提供者可以在應用程式內容中，以自發的方式開啟對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d7e66-110">A mechanism is also defined by which service providers can spontaneously open dialog boxes in the application context when they would not otherwise be expected by the application.</span></span> <span data-ttu-id="d7e66-111">第二個案例的範例是，當數據機用來作為互動式語音通話的撥號程式時，資料數據機服務提供者所顯示的 [ **交談/掛斷** ] 對話方塊，而且必須通知使用者選擇電話，並通知服務提供者何時放置數據機 onhook。</span><span class="sxs-lookup"><span data-stu-id="d7e66-111">An example of this latter case would be the **Talk/Hangup** dialog box that is displayed by a data modem service provider when the modem is being used as a dialer for interactive voice calls, and the user must be told to pick up the phone and inform the service provider when to place the modem onhook.</span></span>

 

 



