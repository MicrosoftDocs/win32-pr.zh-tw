---
description: 網路提供者是支援特定網路通訊協定的 DLL。
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: 網路提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5443ec7366b0f7ad74037f868e1ca4a93dbd913d0c13fda46c7b9fdabd0e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786596"
---
# <a name="network-providers"></a>網路提供者

網路提供者是支援特定網路通訊協定的 DLL。 它也會實行 [網路提供者 API](network-provider-api.md)。 這可讓它與 Windows 作業系統互動，以接收標準的網路要求，例如連線或中斷連接要求。 為了處理這些要求，網路提供者接著會呼叫網路提供者所支援之網路通訊協定適用的特定網路 API。 換句話說，網路提供者會將網路特定功能包裝在 DLL 中，以公開 Windows 的標準介面。

使用網路提供者時，Windows 可以支援許多不同類型的網路通訊協定，而不需要知道每個網路的網路特定詳細資料。 這是不可或缺的，因為新的網路通訊協定一直都在開發中。 使用網路提供者時，支援新的通訊協定只需要建立並安裝新的網路提供者。

如需網路提供者函式和結構的詳細資訊，請參閱下列主題：

-   [網路提供者函式](authentication-functions.md)
-   [網路提供者結構](authentication-structures.md)

 

 



