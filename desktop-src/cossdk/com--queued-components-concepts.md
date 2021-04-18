---
description: COM + 佇列元件概念
ms.assetid: ff11e251-311f-4612-8f0d-a4cbc5b4d872
title: COM + 佇列元件概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d1a8983e84d817e402454392ce95fc2b07a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971309"
---
# <a name="com-queued-components-concepts"></a>COM + 佇列元件概念

根據 [訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) 服務，com + 佇列元件服務提供簡單的方法，以非同步方式叫用和執行元件。 無論寄件者或接收者的可用性或存取性，都可以進行處理。

在 COM 方面， *佇列* 是儲存訊息以供稍後抓取的儲存區。 佇列提供無連接通訊的機制。 也就是說，寄件者和接收者不會直接連線，而且只會透過佇列進行通訊。 佇列提供一種方式來保存資訊，直到接收者準備好取得該資訊為止。 傳送者和接收者會間接進行通訊，以便彼此獨立運作，而不會受到另一個影響。

在過去，必須深入瞭解封送處理，才能佇列、傳送和接收非同步訊息。 現在，使用元件開發人員容易理解及使用的方法呼叫，COM + 佇列的元件服務會自動以訊息佇列訊息的形式來封送處理資料。 而且因為佇列的元件服務提供內建的交易支援，所以不一致的狀態在伺服器發生錯誤時不會危害資料。

本章節中的下列主題包含有關設計和寫入已排入佇列之元件的背景資訊。



| 主題                                                                           | 描述                                                                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [佇列處理的優點](benefits-of-queued-processing.md)<br/>   | 說明使用 COM + 佇列元件進行程式設計的優點。<br/>                                         |
| [已排入佇列的元件架構](queued-components-architecture.md)<br/> | 描述 COM + 佇列元件服務的架構。<br/>                                          |
| [交易式訊息佇列](transactional-message-queuing.md)<br/>   | 描述 COM + 佇列元件服務如何處理交易。<br/>                              |
| [已排入佇列的元件安全性](queued-components-security.md)<br/>         | 描述用戶端訊息和其含意的驗證原則選項。<br/>                 |
| [開發已排入佇列的元件](developing-queued-components.md)<br/>     | 描述撰寫 queuable 元件時的程式設計考慮。<br/>                                     |
| [佇列元件錯誤](queued-components-errors.md)<br/>             | 描述當您使用 COM + 佇列元件服務時，可能會遇到的最常見錯誤類型。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 佇列的元件工作](com--queued-components-tasks.md)
</dt> </dl>

 

 




