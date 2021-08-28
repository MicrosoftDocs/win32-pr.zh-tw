---
title: 不要信任您的對等
description: '\ 0034; 請勿信任您的對等 \ 0034;是基本安全性規則，但通常會被忽略。'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf9235e8b01b6c7b10be96b1d34ed989b27421420d15489441aea948445cfde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021758"
---
# <a name="do-not-trust-your-peer"></a>不要信任您的對等

「請勿信任您的對等」是基本安全性規則，但通常會被忽略。 請勿假設通訊中的另一方會正常運作，而且不會假設您的對等會傳遞您預期的資料。 MIDL 和 RPC 會代表您執行一些檢查，但不會檢查所有的檢查。

知道哪些是 MIDL 或 RPC 驗證的參數層面，以及您必須自行驗證的層面。 例如，對於 in/out 內容控制碼，RPC 會確認內容控制碼不是不正確非 null 值。 它允許 null 值和有效值，但許多開發人員並不知道 null 值是否為 let。 這是要檢查的內容。

即使您通常信任對等，也請務必不要導入遭到入侵的機器或主體帳戶可以攻擊其他電腦的新路徑。 Imagine 使用者選擇他的生日做為密碼，並被攻擊者猜得到。 即使在使用者的要求經過驗證並存取其資料的情況下，仍請確定可利用的攻擊弱點並不存在，例如，可能會讓攻擊者控制您伺服器的堆疊溢位，並延長安全性缺口。

 

 




