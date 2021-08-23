---
description: 這行概念在經過一段時間後就已演變出來，並已部分由位址和終端概念取代。 TAPI 3 不直接使用 line 的概念，但 TAPI 2 仍繼續納入此範例。
ms.assetid: 3e457c7d-da2e-4667-aade-053610abbb8a
title: 折線圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c299924a69d3e6e4889d14a72a571ca11ed2dc9e97514702f8ba4836f4c5b99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660200"
---
# <a name="line"></a>折線圖

這行概念在經過一段時間後就已演變出來，並已部分由位址和終端概念取代。 TAPI 3 不直接使用 line 的概念，但 TAPI 2 仍繼續納入此範例。

*線路裝置* 是一種實體裝置，例如傳真板、數據機或連接到網路的 ISDN 卡。 裝置可能未實際連接到 TAPI 應用程式執行所在的電腦，例如伺服器上的數據機集區。 線路裝置可讓應用程式將資訊傳送至網路或從中接收資訊，藉此支援通訊功能。 線路裝置包含一組一或多個可用於建立呼叫的同質通道。

在 TAPI 2.x 應用程式中，線路裝置是實體電話裝置的邏輯標記法。 雖然「行」通常會使用兩個端點來意味著某個專案，但您可以將線路裝置抽象化成單一點，因為 TAPI 會將它視為進入交換器的行進入點。

![線路裝置](images/ch0501.png)

雖然上圖中的三行是由不同的硬體所組成，而且用於不同的函式，但它們會抽象化為相同的裝置類型，並受到相同的規則控管。 電話不代表電話裝置，而是用於語音通話的線路裝置。 當使用此線路裝置進行傳入或傳出的呼叫時，應用程式也需要開啟並控制電話裝置類別的實例，在稍後的章節中會有詳細說明。

線路裝置類別是與裝置無關的實體線路裝置（如數據機）標記法。 它可包含一或多個相同的通道 (用於在應用程式與交換器或網路之間) 的信號及/或資訊。 因為屬於一行的通道具有相同的功能，所以它們是可互換的。 在許多情況下 (與「POTS) 」一樣，服務提供者會將一行模型為只有一個通道。 其他技術（例如 ISDN）會提供更多的通道，而服務提供者應適當地加以處理。

**TAPI 2.x：** 應用程式使用 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) 函式探索行功能。 使用 [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) 函式的版本協商必須先前已被呼叫。

**TAPI 3.x：** 應用程式主要依賴位址概念。

 

 
