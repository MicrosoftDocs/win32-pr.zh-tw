---
title: 多重連結和回呼連接
description: 針對多重連接連線中的第一個連結，驗證服務會 \_ \_ \_ \_ 在 PPP \_ eap 輸入結構的 fFlags 成員中設定 RAS eap 旗標第一個連結旗標 \_ 。
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af39ebfa54469e2f44c44c800cebbfb176b33cad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106966433"
---
# <a name="multilink-and-callback-connections"></a><span data-ttu-id="42f6f-103">多重連結和回呼連接</span><span class="sxs-lookup"><span data-stu-id="42f6f-103">Multilink and Callback Connections</span></span>

<span data-ttu-id="42f6f-104">針對多重連接連線中的第一個連結，驗證服務會 \_ \_ \_ \_ 在 [**PPP \_ eap \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)結構的 **fFlags** 成員中設定 RAS eap 旗標第一個連結旗標。</span><span class="sxs-lookup"><span data-stu-id="42f6f-104">For the first link in a multilink connection, the authentication service sets the RAS\_EAP\_FLAG\_FIRST\_LINK flag in the **fFlags** member of the [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) structure.</span></span> <span data-ttu-id="42f6f-105">驗證通訊協定可以使用此旗標的存在，來決定是否要針對多重連結連接的第一個連結來呈現使用者介面。</span><span class="sxs-lookup"><span data-stu-id="42f6f-105">The authentication protocol can use the presence of this flag to determine whether to present a user interface specifically for the first link of a multilink connection.</span></span>

<span data-ttu-id="42f6f-106">如果設定連線，讓伺服器回呼用戶端電腦，則 \_ \_ 不會在回呼上設定 RAS EAP 旗標的 \_ 第一個 \_ 連結旗標。</span><span class="sxs-lookup"><span data-stu-id="42f6f-106">If the connection is configured so that the server calls back the client computer, the RAS\_EAP\_FLAG\_FIRST\_LINK flag will not be set on the callback.</span></span>

<span data-ttu-id="42f6f-107">如果驗證通訊協定將 [**PPP \_ EAP \_ 輸出**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)的 **fSaveConnectionData** 成員設定為 **TRUE**，則多重連結連接中的後續連結會接收新的連線特定資料。</span><span class="sxs-lookup"><span data-stu-id="42f6f-107">If the authentication protocol sets the **fSaveConnectionData** member of [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) to **TRUE**, subsequent links in the multilink connection receive the new connection-specific data.</span></span> <span data-ttu-id="42f6f-108">不過，在使用者特定資料的情況下，即使將 **PPP \_ EAP \_ 輸出** 的 **fSaveUserData** 成員設為 **TRUE**，驗證通訊協定仍會繼續取得原始使用者專屬的資料。</span><span class="sxs-lookup"><span data-stu-id="42f6f-108">In the case of user-specific data, however, the authentication protocol continues to get the original user-specific data even if it sets the **fSaveUserData** member of **PPP\_EAP\_OUTPUT** to **TRUE**.</span></span>

<span data-ttu-id="42f6f-109">驗證通訊協定可能會使用 [互動式使用者介面](interactive-user-interface.md) 來收集多重連結連接的特定連結資料。</span><span class="sxs-lookup"><span data-stu-id="42f6f-109">The authentication protocol may use an [interactive user interface](interactive-user-interface.md) to collect data for a particular link of a multilink connection.</span></span> <span data-ttu-id="42f6f-110">在此情況下，驗證服務會在後續連結期間，將產生的資料提供給驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="42f6f-110">In this case, the authentication service makes the resulting data available to the authentication protocol during subsequent links.</span></span> <span data-ttu-id="42f6f-111">不過，這項資料永遠不會儲存在持續性儲存體中。</span><span class="sxs-lookup"><span data-stu-id="42f6f-111">However, this data is never saved to persistent storage.</span></span>

 

 




