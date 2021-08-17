---
description: 網路提供者 API 會指定單一功能功能。
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: 功能功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab47d2c8323131b396640d9154e33749c1716db0d369d3a374f69131468613d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141271"
---
# <a name="capabilities-functions"></a>功能功能

網路提供者 API 會指定單一功能功能。 當作業系統要求有關網路提供者功能的資訊時， [*多個提供者路由器*](/windows/desktop/SecGloss/m-gly) (MPR) 會呼叫網路的每個網路提供者的 [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) 功能。

[**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps)函式會傳回一個位元遮罩，指出網路提供者所支援之網路提供者 API 的功能。 **NPGetCaps** 函式是網路提供者必須實行的唯一功能。 作業系統會呼叫此函式，以判斷提供者支援的網路提供者 API 其他哪些功能。

 

 
