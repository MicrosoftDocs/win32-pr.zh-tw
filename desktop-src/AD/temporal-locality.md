---
title: 時態性位置
description: 時態性位置是減少部分更新視窗的規避策略。
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582371d387862e28414cb9b9c66623f2334b53f845117c9cd4bbddec19213dfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182789"
---
# <a name="temporal-locality"></a>時態性位置

*時態性位置* 是減少部分更新視窗的規避策略。 從指定來源複本進行的變更複寫會以遞增的 USN 順序進行。 在一段時間內立即關閉的寫入將會有 Usn （彼此接近），並會在一段時間內緊密地傳播。 建立或更新多個相關物件的應用程式，應該盡可能將物件盡可能保持在一起。 例如，應用程式可以從使用者收集所有必要的輸入，並在使用者按一下 [套用] 按鈕時將它套用至目錄。

時態性位置也可減少因物件不一致而導致衝突解決問題的機率。

 

 




