---
description: 本節將檢查透過網路運作速度很慢的範例應用程式部分。 在本節中，會對初始程式碼進行修改，以改善其效能。
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: 改善應用程式緩慢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff8f996267328805dc120d39218784a08383fb68ae9f6927e8983b6e1bec2d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097888"
---
# <a name="improving-a-slow-application"></a>改善應用程式緩慢

本節將檢查透過網路運作速度很慢的範例應用程式部分。 在本節中，會對初始程式碼進行修改，以改善其效能。

Mock 範例是稱為 Life 之遊戲的更新部分。 撰寫應用程式的方式是讓用戶端執行更新的計算，並將其傳送至伺服器。 伺服器接著會顯示產生的生命欄位。 用戶端的輸出是位元組串流（以三 (triplet) ，其中每個三個都代表一個資料格更新。 三元中的位元組分別代表資料格的資料列、資料行和值。

這個範例會以刻意執行不良的應用程式開始，提供可從中說明效能改善的基準。 然後，程式碼會經過改良三次，以解決影響效能的各種問題。 這些範例應該依序讀取，因為每個反復專案在舊版上都有改善。

基準代碼和改善該程式碼的修訂如下：

-   [基準版本：執行效能不佳的應用程式](the-baseline-version-a-very-poor-performing-application-2.md)
-   [修訂1：清除明顯的](revision-1-cleaning-up-the-obvious-2.md)
-   [修訂2：重新設計較少的連接](revision-2-redesigning-for-fewer-connects-2.md)
-   [修訂3：壓縮的區區塊轉送](revision-3-compressed-block-send-2.md)
-   [未來的改進](future-improvements-2.md)

> [!WARNING]
> 應用程式的前幾個範例提供刻意不佳的效能，以說明程式碼變更可能帶來的效能改進。 請勿在您的應用程式中使用這些程式碼範例;它們僅供說明之用。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[高效能 Windows 通訊端應用程式](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



