---
description: 手寫辨識引擎（或辨識器）是處理筆墨並將筆墨轉換成文字的軟體。
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: 使用內容改善精確度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7564c18ace39c17e8877c3e5edee6464caea0c36d148cffbfcfb3b5ac09f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715272"
---
# <a name="using-context-to-improve-accuracy"></a>使用內容改善精確度

手寫辨識引擎（或辨識器）是處理筆墨並將筆墨轉換成文字的軟體。 內容是相關的應用程式特定資訊，您提供給辨識器以改善辨識精確度。 換句話說，內容是關於輸入的任何資訊片段，可協助辨識器正確處理欄位中的筆跡。

本節說明您可以利用 Tablet PC 應用程式中內容的不同方式，特別強調未啟用筆墨的應用程式的慣用程式設計技巧。

> [!Note]  
> Windows Vista 軟體發展工具組 (SDK) 的 Tablet PC 技術章節中有一些地方，在 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件及其 [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)和 [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)屬性方面使用「內容」一詞。 請勿將「內容」的其他使用方式與本節中的定義混淆。

 

 

 



