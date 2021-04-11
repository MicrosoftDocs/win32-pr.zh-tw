---
description: 本主題說明 WSDAPI 中的多宿主裝置支援，並提供用戶端和裝置開發人員的執行建議。
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: 執行多宿主 WSD 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3537b96a577db47419d55cb5c6f732f8f7906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194904"
---
# <a name="implementing-a-multi-homed-wsd-device"></a>執行多宿主 WSD 裝置

Web 服務 (DPWS) 的[WS 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)和[裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/)不會描述多宿主裝置的執行。 本主題說明 WSDAPI 中的多宿主裝置支援，並提供用戶端和裝置開發人員的執行建議。 在本主題中，會假設探索訊息是透過 IPv4 和 IPv6 (傳送，如果可用) 具有相同的訊息識別碼和應用程式排序資訊。

## <a name="discovery-in-a-multi-homed-environment"></a>多重主目錄環境中的探索

As mentioned in [Hello](hello-message.md) and [XAddrs](xaddr-validation-rules.md) section of [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md), WSDAPI never provides XAddrs in a Hello message. 也就是說，您可以在所有網路介面上，使用相同的訊息識別碼和應用程式排序資訊來傳送相同的 Hello 訊息。 這可讓用戶端與裝置共用一個以上的子網時，讓用戶端衝突偵測更容易從相同的裝置捨棄多個 Hello 訊息。

由於 [XAddrs](xaddr-validation-rules.md) 不會在 [Hello](hello-message.md) 訊息中傳送，因此用戶端必須傳送 [解析](resolve-message.md) 訊息以取得相關的裝置位址。 解析應該在具有相同訊息識別碼的所有用戶端介面上傳送，且裝置應該視需要篩選重複的訊息。 針對解析訊息使用相同的訊息識別碼，可讓裝置挑選慣用的介面，以便在必要時與用戶端進行通訊。

傳送 [ResolveMatch](resolvematches-message.md) 訊息時，裝置應該提供與網路介面相關的 [XAddrs](xaddr-validation-rules.md) ，而該網路介面的訊息是透過這個介面來單播。 這種作法有助於避免多次用戶端連接嘗試和複雜的重試邏輯。

## <a name="metadata-exchange-in-a-multi-homed-environment"></a>多主控環境中的中繼資料交換

在多重主目錄環境中執行中繼資料交換比執行探索更難，因為中繼資料版本設定。 如果用戶端透過多個介面要求中繼資料，則用戶端可以透過不同的介面接收多個 [GetResponse](getresponse--metadata-exchange--message.md) 訊息。 這些 GetResponse 訊息可以包含具有相同中繼資料版本的不同 **關聯** 性中繼資料區段。 這會減少中繼資料版本號碼的值。

有一個替代方法，其中會傳送單一 [GetResponse](getresponse--metadata-exchange--message.md) 訊息以回應服務的所有位址。 這種方法的缺點是可能會洩漏私用資訊，例如可間接存取網路的拓撲。

在 Windows Vista 中，WSDAPI 提供的中繼資料只包含對接收到中繼資料要求的介面有效的位址。

 

 



