---
title: 使用者配置的範例支援
description: 使用者配置的範例支援
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows Media Format SDK，使用者配置的範例支援
- Advanced Systems Format (ASF) 、使用者配置的範例支援
- ASF (Advanced Systems Format) ，使用者配置的範例支援
- 使用者配置的範例支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021207"
---
# <a name="user-allocated-sample-support"></a>使用者配置的範例支援

在正常情況下，讀取器物件和同步讀取器物件都會為每個傳遞至您應用程式的範例建立新的緩衝區物件。 這是因為讀取物件無法知道您的應用程式在取得它們之後，會如何處理這些範例。 雖然許多應用程式只會讀取範例以立即呈現範例，但有些應用程式可能需要長時間維護範例。 因此，讀取物件無法重複使用它所配置的任何緩衝區;它會將它們傳遞給您的應用程式，然後對其進行控制。

這種方法的問題在於檔案可以包含大量的範例。 如果其中每一個都需要建立新的緩衝區物件，很多處理器時間就會浪費在配置和釋放記憶體。 在時間緊迫的應用程式（例如媒體播放機）中，此額外負荷可能會對效能造成很大的危害。

為了減輕讀取器配置的範例效能問題，讀取器和同步讀取器都支援使用者配置的範例。 若要使用您的應用程式所配置的範例，讀取物件會呼叫您所執行的範例配置回呼方法。 回呼用來將緩衝區傳遞給讀取物件的邏輯完全由您負責。 您可以針對整個檔案使用緩衝區集區，或使用多個緩衝區集區，每個輸出或串流各有一個，或針對您的應用程式運作的任何其他配置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定檔案讀取的緩衝區**](allocating-buffers-for-file-reading.md)
</dt> <dt>

[**檔案讀取功能**](file-reading-features.md)
</dt> </dl>

 

 




