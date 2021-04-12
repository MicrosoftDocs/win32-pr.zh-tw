---
description: COM + 引進了中性的單元，以簡化多執行緒環境中的程式設計。 中立的單元是沒有使用者介面之元件的 COM + 慣用模型。
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: 中性單元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385929"
---
# <a name="neutral-apartments"></a>中性單元

COM + 引進了中性的單元，以簡化多執行緒環境中的程式設計。 中立的單元是沒有使用者介面之元件的 COM + 慣用模型。

在過去，為了避免瓶頸，需要伺服器擴充性的 COM + 開發人員必須執行無限制執行緒的元件;但是，無限制執行緒模型很複雜，因為它們必須處理連鎖的存取。 在中立的單元中，物件會遵循多執行緒單元的指導方針，但可以在任何類型的執行緒上執行。 當執行緒在中立的單元中執行時，會收到物件的內容，而不會造成執行緒切換。

每個進程只能有一個中立的單元。 若要選取中立的單元，請使用下列登錄設定：

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

具有使用者介面的元件應該繼續使用單一執行緒單元作為慣用的模型。 若要選取單一執行緒的單元，請使用下列登錄設定：

**>threadingmodel** = 公寓

 

 



