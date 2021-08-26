---
description: 撥置中心控制項會擴充 TAPI 3 物件模型，以支援 (ACD) 系統的自動呼叫散發需求。
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: 使用撥置中心控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f166658cce86faa0003b762ec697286a434a06b36b18ae92a861d1f6757fa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991538"
---
# <a name="using-call-center-controls"></a>使用撥置中心控制項

撥置中心控制項會擴充 TAPI 3 物件模型，以支援 (ACD) 系統的自動呼叫散發需求。 撥接中心是在電話銀行撥打電話或撥入來電的地點。 例如，銀行或信用卡公司會使用撥入中心來處理帳戶查詢。

電話中心應用程式分成三種基本類型：

-   [ACD Proxy](acd-proxy.md)：處理伺服器上的傳入或傳出會話，這可以是來自專屬電話交換器到網際網路閘道的任何內容。
-   [ACD 代理程式用戶端](acd-agent-client.md)：服務正在接收或發出呼叫的個別代理程式。
-   ACD 監督員用戶端：提供代理程式和 ACD 作業的整體觀點。

> [!Note]  
> 針對 Windows 2000，可使用 TAPI 2.2 提供 proxy 功能，而不會執行監督員功能。

 

Windows SDK 的 [範例] 區段包含 Netds \\ tapi \\ Tapi2 \\ ACD 和 Netds \\ tapi \\ Tapi3 \\ ACD 下的 ACD 程式碼範例。

 

 



