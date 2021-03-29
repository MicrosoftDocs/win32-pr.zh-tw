---
description: 使用 TrueType 文字度量的應用程式可達到高程度的印表機和檔可攜性;即使它們必須維持與舊版 Windows 的相容性，也可以使用 TrueType 計量。
ms.assetid: 29b54315-7c4e-4b8c-ad79-0b85c7386860
title: 使用可移植的 TrueType 計量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83360b620bde11e20726b0ee4124d35bf6cf00b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991506"
---
# <a name="using-portable-truetype-metrics"></a>使用可移植的 TrueType 計量

使用 TrueType 文字度量的應用程式可達到高程度的印表機和檔可攜性;即使它們必須維持與舊版 Windows 的相容性，也可以使用 TrueType 計量。

設計寬度會克服實體裝置所引進之裝置相關文字的大部分問題。 設計寬度是一種邏輯寬度。 與任何柵格化問題或縮放轉換無關，每個字元都有邏輯寬度和高度。 組成邏輯頁面時，字串中的每個字元都有一個與實體裝置寬度無關的位置。 雖然邏輯寬度表示寬度可在所有點大小以線性方式調整，但 nonportable 或大部分的 TrueType 字型都不一定如此。 在較小的點大小，某些字元的高度會相對於其高度，以提供更好的可讀性。

TrueType 核心字型中的字元是針對 2048 by 2048 方格所設計。 設計寬度是以這些格線單位表示的字元寬度。  (TrueType 支援的任何整數格線大小上限為16384（16384）;以2倍的整數乘冪的格線大小比其他格線大小更快。 ) 

字型大綱是以名義單位來設計的。 Em 正方形是用於調整字型外框的名義方格。  (您可以使用 [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica)的 **OtmEMSquare** 成員和 [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)的 **ntmSizeEM** 成員，以名義單位來取得 em 平方的大小。 ) 當字型建立時，如果裝置單位中有 (的點大小) 等於其 em 正方形的大小，則此字型的 ABC 寬度就是所需的設計寬度。 例如，假設 em 正方形的大小為1000，而字型中字元的 ABC 寬度為150、400和150。 這個字型中為10個裝置單位高的字元，會分別有1.5、4和1.5 的 ABC 寬度。 由於 MM \_ 文字對應模式最常用於字型 (而 mm \_ 文字相當於裝置單位) ，這是簡單的計算。

由於 TrueType 設計寬度的高解析度，因此使用它們的應用程式必須考慮可以建立的大型數值。 如需詳細資訊，請參閱下列主題：

-   [裝置與設計單位](device-vs--design-units.md)
-   [便攜檔的計量](metrics-for-portable-documents.md)

 

 



