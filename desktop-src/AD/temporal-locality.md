---
title: 時態性位置
description: 時態性位置是減少部分更新視窗的規避策略。
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462004"
---
# <a name="temporal-locality"></a>時態性位置

*時態性位置* 是減少部分更新視窗的規避策略。 從指定來源複本進行的變更複寫會以遞增的 USN 順序進行。 在一段時間內立即關閉的寫入將會有 Usn （彼此接近），並會在一段時間內緊密地傳播。 建立或更新多個相關物件的應用程式，應該盡可能將物件盡可能保持在一起。 例如，應用程式可以從使用者收集所有必要的輸入，並在使用者按一下 [套用] 按鈕時將它套用至目錄。

時態性位置也可減少因物件不一致而導致衝突解決問題的機率。

 

 




