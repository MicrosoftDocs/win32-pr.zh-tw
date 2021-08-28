---
description: 有許多方式可以處理將收到的 SOAP 訊息分派至適當的服務。 這兩個最簡單的機制是傳輸層級分派，以及位址和動作分派。
ms.assetid: 988dc505-5d1f-46df-9340-107483bb9581
title: 分派 SOAP 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579c01d03a76fcadc1ee82a270c8e222cbf68aa739d10bed0749bb82bcda80ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030248"
---
# <a name="dispatching-soap-messages"></a>分派 SOAP 訊息

有許多方式可以處理將收到的 SOAP 訊息分派至適當的服務。 這兩個最簡單的機制是傳輸層級分派，以及位址和動作分派。

## <a name="transport-level-dispatch"></a>傳輸層級分派

使用傳輸層級分派時，會使用基礎 HTTP 伺服器 (例如 [HTTP API](/windows/desktop/Http/http-api-start-page)) 來管理將要求路由傳送至裝置及其服務。 伺服器會為每個服務提供不同的 URL，並為每個 URL 註冊不同的接收。 這可讓您設計程式碼，讓每個服務都與另一個服務隔離，不論是在相同進程內以個別元件的形式執行，或是以個別進程的形式執行。

傳輸層級分派有幾個優點。 您可以將訊息分派至適當的元件，而不需要先剖析 SOAP 封套或訊息內文。 此外，您可以重複使用大部分 HTTP 伺服器實施所提供之路由傳送訊息的現有機制，這表示不需要自訂分派程式碼。 此外，它也會隔離服務之間的 SOAP 處理常式代碼，以提供某種程度的安全性，因為安全服務可避免訊息流經通用程式碼。

## <a name="address-and-action-dispatch"></a>位址和動作分派

Address 和 action 分派相依于 SOAP 標頭，以決定要分派訊息的適當服務。 此模型也可能使用其他資訊（例如參考參數）來進一步協助分派。

這種模型鼓勵程式碼在多層式訊息堆疊中重複使用，因為所有的程式碼都是由所有服務所共用。 此外，服務的相異傳輸位址並不是必要的，這表示 UUID 位址可用於服務端點。 位址和動作分派也會直接轉譯為程式設計模型。 開發人員可以將服務和裝置插入管理路由的單一元件，而不需要系結至 HTTP 層或為每個服務建立個別的元件。

 

 
