---
description: 保存作業可讓單一位址處理多個通訊會話。
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: 保留
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afacd6d9664e9a095a1e8b0c725dc0171da709fdecffb88b428231a5b5359a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003636"
---
# <a name="hold"></a>保留

保存作業可讓單一位址處理多個通訊會話。 將會話放在硬性保存後，就可以釋出使用者的線路/位址來進行其他呼叫。 通話通常無法轉移或包含在會議電話中，但諮詢電話可以。 諮詢電話是使用 [會議](conference-ovr.md) 或 [轉移](transfer-ovr.md) 作業起始的。

在呼叫成功放置之後，撥號狀態通常會轉換成舉 servicerequeststatusenum.onhold 狀態。 當呼叫保留時，應用程式可以接收有關已保存撥號狀態變更的訊息。 例如，如果持有的合作物件停止回應，則撥號狀態可以轉換為已中斷連線。

在橋接的情況下，保留作業可能不會實際將通話放置在待命狀態。 呼叫中其他工作站的狀態可以管理 (例如，無法在其他工作站參與時嘗試「保留」呼叫，) ;相反地，呼叫可以直接變更為非作用中狀態，同時維持在其他工作站的連線。

並非所有服務提供者都支援使用這項作業。

**TAPI 2.x：** 請參閱 [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold)、 [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)。

**TAPI 3.x：** 請參閱 [**ITBasicCallControl：： Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold)。

 

 
