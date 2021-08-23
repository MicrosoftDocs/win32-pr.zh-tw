---
description: 若要取得每個辨識結果的信賴層級，您可以取得 RecognitionAlternate 物件的信賴屬性或手勢物件的信賴屬性。
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: 信賴屬性 [關於辨識]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3316e9637fe6dcf820f8412724363a25dab65ce9a291b8c3c70c5bcf9c83bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093021"
---
# <a name="confidence-property-about-recognition"></a>關於辨識的信賴財產 \[\]

若要取得每個辨識結果的信賴層級，您可以取得 [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate)物件的 [**信賴**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence)屬性或 [**手勢**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)物件的 [**信賴**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence)屬性。 信賴等級是一個數位，指出辨識器針對對應辨識區段傳回的每個替代辨識結果的信賴程度。

信賴度會以低、平均或高的方式傳回。 應用程式會使用這些結果來：

-   向使用者表示有多個可能存在。
-   依信賴等級排列替代項的次序。

## <a name="what-affects-confidence"></a>信賴度的影響

某些讓手寫辨識難以和影響信賴的事項包括：

-   難以判斷文字分割

![顯示寫入太近的影像](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   案例問題

![顯示「案例」一字手寫版本問題的影像](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   不常見的書寫樣式
-   獨立標點符號

![顯示太遠離文字之引號的影像](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   英文辨識器中的重音字元

> [!Note]  
> 信賴評估僅適用于美國英文和此版本中的所有手勢辨識器。 提供其他辨識器信賴屬性的方法會傳回 **E \_ >notimpl**。

 

 

 



