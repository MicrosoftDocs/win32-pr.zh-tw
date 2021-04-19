---
description: 如果應用程式不想讓來自 TAPI 或服務提供者的會話外來事件產生任何干擾，它應該保護呼叫的安全。
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: 保護會話的安全
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991373"
---
# <a name="secure-a-session"></a>保護會話的安全

如果應用程式不想讓來自 TAPI 或服務提供者的會話外來事件產生任何干擾，它應該保護呼叫的安全。 例如，在類比環境通話等候的聲場中，可以在原始電話上終結傳真或數據機會話。

應用程式可以在呼叫進行時或在呼叫已經存在時，保護呼叫的安全。

並非所有服務提供者都支援使用這項作業。

**TAPI 2.x：** 請參閱 [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall)。

**TAPI 3.x：** 請參閱 [**ITAddress：： Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward)。

 

 
