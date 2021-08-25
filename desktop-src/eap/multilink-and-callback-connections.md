---
title: 多重連結和回呼連接
description: 針對多重連接連線中的第一個連結，驗證服務會 \_ \_ \_ \_ 在 PPP \_ eap 輸入結構的 fFlags 成員中設定 RAS eap 旗標第一個連結旗標 \_ 。
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7493550863a755a87668c96dbe0ce600d524a111b7e7300b97c307f4d30c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852318"
---
# <a name="multilink-and-callback-connections"></a>多重連結和回呼連接

針對多重連接連線中的第一個連結，驗證服務會 \_ \_ \_ \_ 在 [**PPP \_ eap \_ 輸入**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)結構的 **fFlags** 成員中設定 RAS eap 旗標第一個連結旗標。 驗證通訊協定可以使用此旗標的存在，來決定是否要針對多重連結連接的第一個連結來呈現使用者介面。

如果設定連線，讓伺服器回呼用戶端電腦，則 \_ \_ 不會在回呼上設定 RAS EAP 旗標的 \_ 第一個 \_ 連結旗標。

如果驗證通訊協定將 [**PPP \_ EAP \_ 輸出**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)的 **fSaveConnectionData** 成員設定為 **TRUE**，則多重連結連接中的後續連結會接收新的連線特定資料。 不過，在使用者特定資料的情況下，即使將 **PPP \_ EAP \_ 輸出** 的 **fSaveUserData** 成員設為 **TRUE**，驗證通訊協定仍會繼續取得原始使用者專屬的資料。

驗證通訊協定可能會使用 [互動式使用者介面](interactive-user-interface.md) 來收集多重連結連接的特定連結資料。 在此情況下，驗證服務會在後續連結期間，將產生的資料提供給驗證通訊協定。 不過，這項資料永遠不會儲存在持續性儲存體中。

 

 




