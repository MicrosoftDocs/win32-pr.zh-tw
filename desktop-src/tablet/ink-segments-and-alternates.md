---
description: 辨識器可能會發現數種將筆墨範例分成辨識區段的方式。 因此，辨識替代項的數目可能會錯開，即使是小型筆墨範例也是如此。
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: 筆跡區段和替代項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 702c2da4984afd22490827acdf65962abc789d7ad9f0ddab3e602bc688ac6542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883988"
---
# <a name="ink-segments-and-alternates"></a>筆跡區段和替代項

辨識器可能會發現數種將筆墨範例分成辨識區段的方式。 因此，辨識替代項的數目可能會錯開，即使是小型筆墨範例也是如此。

例如，"t o g e t h e r" 可能產生下列結果：

-   「取得她」 (再加上每個字的替代專案) 
-   「收集」 (再加上每個字組的替代項) 
-   "tog 乙太幣" (再加上每個字組的替代項) 
-   「tog at 她」 (再加上每個單字的替換) 
-   「一起」 (加上單字的替代項) 

[**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)物件支援在 [**筆跡**](inkdisp-class.md)物件內有效率地儲存完整的辨識結果。 **筆墨** 物件會將辨識替代項對應至 **筆墨** 物件中的筆觸，也可能包含其他資訊，例如基準位置、行索引和語言範圍。

 

 



