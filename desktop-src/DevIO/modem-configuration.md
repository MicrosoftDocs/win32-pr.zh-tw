---
description: 數據機設定功能可讓您在建立連線之前設定數據機。
ms.assetid: 67d8f3c4-0295-4028-8b12-1a5e26979df5
title: 數據機設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7abd6c5319011b8821487b6adf0351dc799e61f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847470"
---
# <a name="modem-configuration"></a><span data-ttu-id="170af-103">數據機設定</span><span class="sxs-lookup"><span data-stu-id="170af-103">Modem Configuration</span></span>

<span data-ttu-id="170af-104">數據機設定功能可讓您在建立連線之前設定數據機。</span><span class="sxs-lookup"><span data-stu-id="170af-104">Modem configuration functions enable you to configure a modem before making a connection.</span></span> <span data-ttu-id="170af-105">應用程式可以設定數據機選項，並判斷數據機的功能，而不需使用任何數據機裝置的特定命令。</span><span class="sxs-lookup"><span data-stu-id="170af-105">An application can set modem options and determine the features of a modem without using commands specific to any modem device.</span></span> <span data-ttu-id="170af-106">以下是應用程式在進行呼叫之前可以設定的一般功能：</span><span class="sxs-lookup"><span data-stu-id="170af-106">Following are the general features an application may set before making a call:</span></span>

-   <span data-ttu-id="170af-107">作業的主要模式 (同步、非同步，以及是否已啟用) 的錯誤控制。</span><span class="sxs-lookup"><span data-stu-id="170af-107">Primary mode of operation (synchronous, asynchronous, and whether error control is enabled).</span></span>
-   <span data-ttu-id="170af-108">42個錯誤控制 (由 CCITT 建議的) 所定義，包括特定參數。</span><span class="sxs-lookup"><span data-stu-id="170af-108">V.42 error control (defined by CCITT recommendation V.42), including specific parameters.</span></span> <span data-ttu-id="170af-109">CCITT 代表國際電報與電話諮詢委員會。</span><span class="sxs-lookup"><span data-stu-id="170af-109">CCITT stands for the International Telegraph and Telephone Consultative Committee.</span></span>
-   <span data-ttu-id="170af-110">42bis (由 CCITT 建議的 42bis) 和 MNP5 資料壓縮所定義。</span><span class="sxs-lookup"><span data-stu-id="170af-110">V.42bis (defined by CCITT recommendation V.42bis) and MNP5 data compression.</span></span>
-   <span data-ttu-id="170af-111">超時選項，包括呼叫設定、非活動及緩衝的資料傳遞。</span><span class="sxs-lookup"><span data-stu-id="170af-111">Time-out options, including call setup, inactivity, and buffered data delivery.</span></span>

<span data-ttu-id="170af-112">在設定數據機的設定之前，應用程式應該使用 [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) 函式來判斷數據機裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="170af-112">Before setting a modem's configuration, an application should determine the capabilities of the modem device by using the [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) function.</span></span> <span data-ttu-id="170af-113">此函數會填入 [**COMMPROP**](/windows/desktop/api/WinBase/ns-winbase-commprop) 結構。</span><span class="sxs-lookup"><span data-stu-id="170af-113">This function fills in a [**COMMPROP**](/windows/desktop/api/WinBase/ns-winbase-commprop) structure.</span></span> <span data-ttu-id="170af-114">此結構包含適用于所有通訊裝置的一般部分，以及每個提供者子類型特有的部分。</span><span class="sxs-lookup"><span data-stu-id="170af-114">This structure contains both a general portion, which applies to all communications devices, and a portion that is specific to each provider subtype.</span></span> <span data-ttu-id="170af-115">針對數據機裝置， **COMMPROP** 結構的提供者特定部分是 [**MODEMDEVCAPS**](/windows/desktop/api/Mcx/ns-mcx-modemdevcaps) 結構。</span><span class="sxs-lookup"><span data-stu-id="170af-115">For modem devices, the provider-specific portion of the **COMMPROP** structure is a [**MODEMDEVCAPS**](/windows/desktop/api/Mcx/ns-mcx-modemdevcaps) structure.</span></span>

<span data-ttu-id="170af-116">應用程式可以使用 [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) 和 [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) 函式來取得和設定數據機目前的設定，這兩個函式都使用 [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) 結構。</span><span class="sxs-lookup"><span data-stu-id="170af-116">An application can get and set the current configuration of a modem by using the [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) and [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) functions, both of which use a [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure.</span></span> <span data-ttu-id="170af-117">此結構包含適用于所有通訊裝置的一般部分，以及每個提供者子類型特有的部分。</span><span class="sxs-lookup"><span data-stu-id="170af-117">This structure contains both a general portion, which applies to all communications devices, and a portion that is specific to each provider subtype.</span></span> <span data-ttu-id="170af-118">針對數據機裝置， **COMMCONFIG** 結構的提供者特定部分是 [**MODEMSETTINGS**](/windows/desktop/api/Mcx/ns-mcx-modemsettings) 結構。</span><span class="sxs-lookup"><span data-stu-id="170af-118">For modem devices, the provider-specific portion of the **COMMCONFIG** structure is a [**MODEMSETTINGS**](/windows/desktop/api/Mcx/ns-mcx-modemsettings) structure.</span></span>

<span data-ttu-id="170af-119">設定數據機之後，應用程式就可以使用電話語音應用程式開發介面 (TAPI) 來實際建立連接。</span><span class="sxs-lookup"><span data-stu-id="170af-119">After configuring a modem, an application can use the Telephony Application Programming Interface (TAPI) to actually establish a connection.</span></span>

<span data-ttu-id="170af-120">數據機設定功能不提供數據機的長期管理和維護。</span><span class="sxs-lookup"><span data-stu-id="170af-120">The modem configuration functions do not provide for long-term management and maintenance of a modem.</span></span> <span data-ttu-id="170af-121">數據機服務提供者應該提供 [數據機設定] 對話方塊以供此用途。</span><span class="sxs-lookup"><span data-stu-id="170af-121">Modem service providers should supply modem configuration dialog boxes for this purpose.</span></span>

 

 



