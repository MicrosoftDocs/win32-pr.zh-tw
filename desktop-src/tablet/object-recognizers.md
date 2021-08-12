---
description: 除了辨識文字之外，辨識器還可以辨識相關物件的類別。
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: 物件辨識器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabfd44a5eb126d48df70efd1c391584d12afc94e5e21c714aa0c740a7d486f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449659"
---
# <a name="object-recognizers"></a>物件辨識器

除了辨識文字之外，辨識器還可以辨識相關物件的類別。 物件辨識器會根據其用途辨識一般圖形。 物件辨識器可用來辨識：

-   音符
-   幾何圖形
-   數學方公式
-   Flow 圖表元素

通常，這類辨識器可辨識的物件會在二維空間或功能的關聯性中。 例如，在數學方程式的複雜關聯性中，辨識器可以針對明確整數的上限傳回不同的結果，而非分數的分子。

因為這些關聯性的一般本質，所以很難定義一組可針對每個物件辨識器運作的介面。

Tablet PC 技術為 Managed 程式庫和自動化介面中的物件辨識器提供了基本的架構。 不過，您必須開發自訂介面，以說明每個物件辨識器可辨識之物件之間的複雜空間關聯性。 具體而言，在物件辨識器中，平臺會提供基本的 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件，以便將 [**筆墨**](inkdisp-class.md) 物件與辨識器內容建立關聯，以及呼叫辨識器來執行辨識。

 

 



