---
description: 一致且完成的旗標
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: 一致且完成的旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568b0c614c745f46d8bbcc816b65f501e02de1e0455f0b64216662ec52308213
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954358"
---
# <a name="consistent-and-done-flags"></a>一致且完成的旗標

在啟動交易對象之前，COM + 一律會建立內容物件。 內容物件會保存物件相關資訊，例如其建立者及其交易識別碼。 每個內容物件也包含 *一致的旗* 標和 *完成的旗* 標。 這些旗標一起決定交易對象的狀態。

一致性旗標表示交易對象為一致或不一致。 讓物件的狀態保持一致的特定詳細資料，取決於程式設計人員。 當方法呼叫將此旗標設為 True 時，表示物件是一致的。 False 表示物件不一致。 COM + 會在建立物件實例時將旗標設定為 True。 一致的物件已準備好繼續進行交易。 當物件維持使用中狀態時，後續的方法呼叫可以重複地將一致旗標從 True 切換為 False，反之亦然。

完成旗標會決定交易的持續時間。 當方法呼叫傳回時，COM + 會檢查完成的旗標。 如果方法將此旗標設定為 True，COM + 就會停用該物件，並記下一致的旗標。 當 done 旗標為 False 時，COM + 都不會停用物件，也不會記下一致的旗標。 當 COM + 建立物件實例時，會將完成的旗標設定為 False。

「一致」旗標會將投票轉換成認可或中止執行的交易，而「完成」旗標會完成投票。 當方法呼叫傳回上的 [完成] 旗標設為 True 或物件停用時，COM + 會檢查一致的旗標。 雖然物件的一致旗標可能會在每個方法呼叫中重複變更，但只有最後一個變更計數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管理 COM + 中的自動交易](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[設定一致且完成的旗標](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



