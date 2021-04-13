---
description: 在 COM + 程式設計模型中，您可以設計您的元件來執行最佳&\# 郵件; 啟用商務邏輯或建立資料庫連接&\# 郵件; 並依賴 Microsoft Windows 的交易處理架構來自動化交易。
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: 管理 COM + 中的自動交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510675"
---
# <a name="managing-automatic-transactions-in-com"></a>管理 COM + 中的自動交易

在 COM + 程式設計模型中，您可以設計您的元件來執行最棒的動作：啟用商務邏輯或建立資料庫連接，並依賴 Microsoft Windows 的交易處理架構來自動化交易。

## <a name="starting-a-transaction"></a>啟動交易

COM + 在遇到下列其中一種情況時，會自動開始交易：

-   當非交易式用戶端呼叫需要交易的元件時，或需要新的交易時。
-   當交易式用戶端呼叫需要新交易的元件時。

如果 COM + 判斷物件應該有新的交易，它會先開始交易，然後將物件放在其中。 此程序包含下列步驟：

1.  COM + 會建立內容物件、將 [JIT](com--just-in-time-activation.md) 啟動和 [同步](com--synchronization.md) 處理屬性設定為 [必要]，並將 [一致] [和 [完成] 旗標](consistent-and-done-flags.md) 分別設定為 True 和 False。
2.  COM + 會與分散式交易協調器 (DTC) 通訊以開始交易。 DTC 會協調實體交易。
3.  DTC 會產生交易識別碼，並將它傳回給 COM +。 交易識別碼會建立交易界限。 參與交易的所有物件都會共用相同的識別碼。
4.  當用戶端建立物件時，COM + 會在交易界限內啟用它。

## <a name="ending-a-transaction"></a>結束交易

在發生下列其中一種情況時，COM + 會藉由認可或中止來結束自動交易：

-   交易的根物件會完成其工作，且 COM + 會釋放它。 在根物件停用之後，交易會嘗試認可。
-   用戶端會釋放根物件。 如果沒有參考，根物件就會停用，而且交易會嘗試認可。
-   交易超過其超時閾值。 如果未在交易超時期間內認可交易，則會自動中止交易，並停用與交易相關聯的所有物件。 預設的交易超時期限為60秒。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[一致且完成的旗標](consistent-and-done-flags.md)
</dt> <dt>

[藉由通知根物件來加速交易](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[藉由呼叫 SetComplete 來終止自動交易](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



