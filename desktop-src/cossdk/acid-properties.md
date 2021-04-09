---
description: 創造 by transaction 處理先鋒，縮寫 ACID 表示不可部分完成、一致、隔離且持久。
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: ACID 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110568"
---
# <a name="acid-properties"></a>ACID 屬性

創造 by transaction 處理先鋒，縮寫 ACID 表示不可部分完成、一致、隔離且持久。 為了確保可預測的行為，所有交易都必須擁有這些基本屬性，並將任務關鍵性交易的角色強化為全或無主張。

下列清單包含每個 ACID 屬性的定義和描述：

<dl> <dt>

<span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>原子
</dt> <dd>

交易必須剛好執行一次，而且必須是不可部分完成的，也就是所有工作都已完成或全都不是。 交易內的作業通常會共用通用意圖，且都是相互依存的。 藉由只執行這些作業的子集，系統可能會危及交易的整體意圖。 不可部分完成性可消除只處理一部分作業的機會。

</dd> <dt>

<span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>一致
</dt> <dd>

交易必須維持資料的一致性，將資料的一致狀態轉換成另一種一致的資料狀態。 維持一致性的大部分責任都與應用程式開發人員有關。

</dd> <dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>孤立
</dt> <dd>

交易必須是隔離單位，這表示並行的交易應該會像是在系統中唯一執行的交易一樣運作。 由於高度隔離可能會限制並行交易數目，因此有些應用程式會減少 exchange 中的隔離等級，以獲得更好的輸送量。 如需詳細資訊，請參閱設定 [交易隔離等級](configuring-transaction-isolation-levels.md) 。

</dd> <dt>

<span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>耐用
</dt> <dd>

交易必須可復原，因此必須具有持久性。 如果交易認可，系統會保證即使電腦在認可之後立即損毀，也可以保存其更新。 特製化記錄可讓系統的重新開機程式完成交易所需的未完成作業，使交易持久。

</dd> </dl>

 

 



