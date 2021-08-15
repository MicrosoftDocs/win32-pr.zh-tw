---
title: SpeechInput 物件
description: SpeechInput 物件
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d96dd52d5847b3fbaa81bbc21d4015698655fba1fe2523aaddc065e6d2ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975518"
---
# <a name="the-speechinput-object"></a>SpeechInput 物件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

[**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**)物件可讓您存取代理程式伺服器所維護的語音輸入屬性。 用戶端應用程式的屬性是唯讀的，但使用者可以在 Microsoft Agent 屬性工作表中變更它們。 只有當相容的語音引擎已安裝且已啟用時，伺服器才會傳回值。

不再支援 [**引擎**](https://www.bing.com/search?q=**Engine**)、 [**已安裝**](https://www.bing.com/search?q=**Installed**)和 [**語言**](https://www.bing.com/search?q=**Language**) 屬性，但 (回溯相容性) 會在查詢時傳回 null 值。 若要查詢或設定語音辨識的模式，請使用 [**SRModeID**](srmodeid-property.md) 屬性。

-   [SpeechInput 屬性](speechinput-properties.md)

 

 




