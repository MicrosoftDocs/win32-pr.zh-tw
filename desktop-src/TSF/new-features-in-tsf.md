---
title: TSF 中的新功能
description: 隨著 Microsoft WindowsXP Service Pack 1 的推出，文字服務架構 (TSF) 有數項新功能。
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- 文字服務架構 (TSF) 、新功能
- TSF (文字服務架構) 、新功能
- 文字服務，新功能
- 啟用 TSF 的應用程式，新功能
- 文字服務架構 (TSF) ，advanced support
- TSF (文字服務架構) ，advanced support
- 文字服務，advanced support
- 啟用 TSF 的應用程式，advanced support
- 文字服務架構 (TSF) 、Rich Edit
- TSF (文字服務架構) 、Rich Edit
- 文字服務，Rich Edit
- 啟用 TSF 的應用程式，Rich Edit
- Rich Edit
- 文字服務架構 (TSF) ，安全性
- TSF (文字服務架構) ，安全性
- 文字服務，安全性
- 啟用 TSF 的應用程式，安全性
- TSF 的安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73494d4538b25dfa0b004c8691391fb1c572c7ce6d82247cacae4fb9e0a838
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952017"
---
# <a name="new-features-in-tsf"></a>TSF 中的新功能

隨著 Microsoft WindowsXP Service Pack 1 的推出，文字服務架構 (TSF) 有數項新功能。

## <a name="extended-support-of-advanced-text-services"></a>Advanced Text Services 的延伸支援

已將支援新增至 TSF 和 Windows，為整個桌面的所有應用程式提供一致的使用者介面。 這項新的支援可讓不知道 TSF 的繼承應用程式或控制項充分利用一些 advanced text services。 例如，您現在可以在任何應用程式中，使用語音聽寫和手寫將文字輸入檔。

這項新功能只適用于 WindowsXP Service Pack 1 或更新版本。 預設會關閉它。 若要啟用它，請在 [**地區及語言選項**] 控制台的 [**文字服務] 和 [輸入語言**] 部分中，按一下 [新的 **Advanced** ] 索引標籤中的核取方塊。

![在 tsf 控制台中不知道應用程式支援](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a>豐富的編輯支援

[Microsoft® Rich Edit](../controls/rich-edit-controls.md) 版本4.1 （由應用程式用來以特殊字元和段落格式來查看和編輯文字）現在會公開 TSF 功能。 預設會關閉這項支援。 若要啟用 Rich Edit 中的 TSF，裝載應用程式會將特殊的視窗訊息傳送至 Rich Edit 控制項。

## <a name="security-improvements"></a>安全性改善

TSF 的安全性和穩定性已大幅改善，可降低惡意程式存取堆疊、堆積或其他安全記憶體位置的可能性。 軟體發展工具組 (SDK) 範例應用程式和文字服務的安全性也已有所改善。

 

 