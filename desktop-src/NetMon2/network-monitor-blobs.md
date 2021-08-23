---
description: 網路監視器二進位大型物件 (BLOB) 是一般資料結構，其中包含網路介面卡 (Nic) 的設定和位置資訊。
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: 網路監視器 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d15ce2a8f85860720c6f38b0d6c019a33e57df0a1b589ba23455db0319d0436
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799548"
---
# <a name="network-monitor-blobs"></a>網路監視器 Blob

網路監視器二進位大型物件 (BLOB) 是一般資料結構，其中包含網路介面卡 (Nic) 的設定和位置資訊。 使用 Blob 來代表 Nic，並篩選 Nic 清單中的專案。 BLOB 也可以包含應用程式特定的資料，而不會影響它們所保留的其他資料。 BLOB 實作為所有必須使用 BLOB Api 存取 Blob 的層級不透明。

## <a name="blob-structure"></a>BLOB 結構

BLOB 可視為用來指定字串的階層式樹狀結構。 此樹狀結構有三個層級：擁有者、類別和標記。 擁有者是一種字串，通常表示讀取專案的物件。 此類別也是字串，它會指定擁有者底下的一般功能群組標記。 標記是專案的實際名稱。

Blob 的結構化特性包括：

-   一個進程內的 BLOB 協助程式會由每個 BLOB 內建的 mutex 彼此保護。
-   每個 BLOB 都有內部版本號碼，讓協助專家可以處理目前和未來的 BLOB 表單。 如果您透過遠端程序呼叫將 BLOB 傳送到另一部電腦，可能會發生版本衝突。
-   BLOB 本身是 void 的指標。 請注意，應用程式應該使用 **const** 修飾詞來配置 blob，以避免變更內容。
-   每個指示項及其值都是字串。 請注意， **GetString** 函式所傳回的字串實際上是指向 BLOB 的指標，不應該變更。 基於這個理由，必須將這些字串指定為 **const char** _ \_ pX *，讓應用程式不會意外變更它們。

一般情況下，所有具有 **const** 指示項的參數都鼓勵呼叫端避免變更值，而不是禁止 helper 函式變更它們。 事實上，helper 函數通常會變更這些值。

 

 



