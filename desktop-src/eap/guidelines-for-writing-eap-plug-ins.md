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
# <a name="guidelines-for-writing-eap-dlls"></a>撰寫 EAP Dll 的指導方針

您可以撰寫 EAP Dll 或外掛程式，以在不同的案例中將效能優化。

## <a name="general-guidelines"></a>一般準則

-   為了建立加密的連線，EAP 外掛程式必須產生加密金鑰，並透過 Microsoft 廠商專屬的 RADIUS 屬性 MS-MPPE-傳送金鑰和 MS-MPPE-- 如需詳細資訊，請參閱 [**PPP \_ EAP \_ 輸出**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) 中的「備註」一節。

## <a name="wireless-guidelines"></a>無線指導方針

以下是撰寫 EAP 外掛程式的指導方針和建議，可支援在無線 (802.1 X) 案例中驗證電腦。 本節不適用於 VPN 和撥號案例。

-   為了不封鎖自動系統的執行，EAP 外掛程式不能進行任何使用者介面呼叫。
-   電腦驗證步驟的 EAP 外掛程式執行必須儘快完成，因此它不會妨礙作業系統啟動。
    > [!Note]  
    > 如果您的 EAP 通訊協定不支援電腦驗證，則必須檢查 [**PPP \_ eap \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)的 **fFlags** 欄位中是否已使用電腦驗證旗標、 **RAS \_ eap \_ 旗標 \_ 電腦 \_** 驗證，並傳回錯誤。

     

 

 




