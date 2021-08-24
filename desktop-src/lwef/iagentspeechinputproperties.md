---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660848eae85465ea322bcb08a218c6ee463eb384d3a4766cacf6a86038662386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609328"
---
# <a name="iagentspeechinputproperties"></a>IAgentSpeechInputProperties

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

IAgentSpeechInputProperties 可讓您存取伺服器所維護的語音輸入屬性。 大部分的屬性都是唯讀的用戶端應用程式，但使用者可以在 Microsoft Agent 屬性工作表中變更它們。 只有當相容的語音引擎已安裝且已啟用時，Microsoft 代理程式伺服器才會傳回值。 查詢這些屬性會嘗試啟動語音引擎。

**依照 Vtable 順序的方法**



| IAgentSpeechInputProperties 方法                                     | 描述                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**GetEnabled**](iagentspeechinputproperties--getenabled.md)           | 傳回是否啟用語音辨識引擎。 |
| [**GetHotKey**](iagentspeechinputproperties--gethotkey.md)             | 傳回接聽按鍵的目前金鑰指派。  |
| [**GetListeningTip**](iagentspeechinputproperties--getlisteningtip.md) | 傳回是否啟用接聽提示。             |



 

舊版 Microsoft 代理) 程式 (支援的 [**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**)、 [**GetLCID**](https://www.bing.com/search?q=**GetLCID**)、 [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)和 [**SetEngine**](https://www.bing.com/search?q=**SetEngine**)方法，仍支援回溯相容性。 不過，這些方法不會 stub，也不會傳回有用的值。 使用 [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) 和 [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) 來查詢及設定要搭配字元使用的語音辨識引擎。 請記住，引擎必須符合字元目前的語言設定。

 

 




