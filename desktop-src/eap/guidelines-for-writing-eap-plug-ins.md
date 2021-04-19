---
title: 撰寫 EAP Dll 的指導方針
description: 您可以撰寫 EAP Dll 或外掛程式，以在不同的案例中將效能優化。
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2d437df61811e6fb24b3a9b4ff406ced4905
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106991096"
---
# <a name="guidelines-for-writing-eap-dlls"></a><span data-ttu-id="a1cf5-103">撰寫 EAP Dll 的指導方針</span><span class="sxs-lookup"><span data-stu-id="a1cf5-103">Guidelines for Writing EAP DLLs</span></span>

<span data-ttu-id="a1cf5-104">您可以撰寫 EAP Dll 或外掛程式，以在不同的案例中將效能優化。</span><span class="sxs-lookup"><span data-stu-id="a1cf5-104">EAP DLLs or Plug-ins can be written to optimize their performance in different scenarios.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="a1cf5-105">一般準則</span><span class="sxs-lookup"><span data-stu-id="a1cf5-105">General Guidelines</span></span>

-   <span data-ttu-id="a1cf5-106">為了建立加密的連線，EAP 外掛程式必須產生加密金鑰，並透過 Microsoft 廠商專屬的 RADIUS 屬性 MS-MPPE-傳送金鑰和 MS-MPPE--</span><span class="sxs-lookup"><span data-stu-id="a1cf5-106">In order to create an encrypted connection, EAP plug-ins must generate encryption keys and return them through the Microsoft vendor-specific RADIUS Attributes MS-MPPE-Send-Keys and MS-MPPE-Recv-Keys.</span></span> <span data-ttu-id="a1cf5-107">如需詳細資訊，請參閱 [**PPP \_ EAP \_ 輸出**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) 中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="a1cf5-107">See the Remarks section in [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) for more information.</span></span>

## <a name="wireless-guidelines"></a><span data-ttu-id="a1cf5-108">無線指導方針</span><span class="sxs-lookup"><span data-stu-id="a1cf5-108">Wireless Guidelines</span></span>

<span data-ttu-id="a1cf5-109">以下是撰寫 EAP 外掛程式的指導方針和建議，可支援在無線 (802.1 X) 案例中驗證電腦。</span><span class="sxs-lookup"><span data-stu-id="a1cf5-109">The following are guidelines and recommendations for writing an EAP Plug-in that supports authenticating machines in wireless (802.1X) scenarios.</span></span> <span data-ttu-id="a1cf5-110">本節不適用於 VPN 和撥號案例。</span><span class="sxs-lookup"><span data-stu-id="a1cf5-110">This section does not apply to VPN and Dial-up scenarios.</span></span>

-   <span data-ttu-id="a1cf5-111">為了不封鎖自動系統的執行，EAP 外掛程式不能進行任何使用者介面呼叫。</span><span class="sxs-lookup"><span data-stu-id="a1cf5-111">In order not to block unattended systems' execution, EAP plug-ins must not make any user interface calls.</span></span>
-   <span data-ttu-id="a1cf5-112">電腦驗證步驟的 EAP 外掛程式執行必須儘快完成，因此它不會妨礙作業系統啟動。</span><span class="sxs-lookup"><span data-stu-id="a1cf5-112">The EAP Plug-in implementation of the machine authentication step must complete as quickly as possible so it does not hinder operating system startup.</span></span>
    > [!Note]  
    > <span data-ttu-id="a1cf5-113">如果您的 EAP 通訊協定不支援電腦驗證，則必須檢查 [**PPP \_ eap \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)的 **fFlags** 欄位中是否已使用電腦驗證旗標、 **RAS \_ eap \_ 旗標 \_ 電腦 \_** 驗證，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1cf5-113">If your EAP protocol does not support machine authentication, it must check for the machine authentication flag, **RAS\_EAP\_FLAG\_MACHINE\_AUTH** used in the **fFlags** field in [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), and return an error.</span></span>

     

 

 




