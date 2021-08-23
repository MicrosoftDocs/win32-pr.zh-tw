---
description: 在2006年8月之前，WS-MetadataExchange 定義了自己的 Get metadata exchange 方法，其適用于 Web 服務的裝置設定檔 (DPWS) 。
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: WS-MetadataExchange 和 WS-Transfer 規格合規性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bec29d96b4ba3671f176349a56b891cd4d642762670fd16cf582da53208c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793968"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a>WS-MetadataExchange 和 WS-Transfer 規格合規性

在2006年8月之前， [透過 ws-metadataexchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) 定義了自己的 [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange 方法，其 [適用于 Web 服務的裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) 。 WS-MetadataExchange 規格1.1 版以 WS-Transfer 規格中定義的 Get 方法取代了此方法。

在目前的模型中，WS-Transfer 會提供 [Get](get--metadata-exchange--http-request-and-message.md) 方法，而不會參考主體的類型。 WS-MetadataExchange 描述內文的格式，以及在單一回應中封裝多個中繼資料片段的機制，而 DPWS 則描述服務應該包含在中繼資料回應中的特定中繼資料部分。

WSDAPI 未完全支援 WS-Transfer 規格。 因為裝置只需要 [Get](get--metadata-exchange--http-request-and-message.md) 方法，所以不會執行 WS-Transfer 的其他部分。 此外，WSDAPI 不會執行 WS-透過 ws-metadataexchange 中所述的選擇性 GetMetadata 方法。

 

 



