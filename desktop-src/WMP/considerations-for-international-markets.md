---
title: 國際市場的考慮
description: 國際市場的考慮
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Windows Media Player 線上商店，國際市場
- 線上商店，國際市場
- 輸入1個線上商店，國際市場
- 輸入2個線上商店，國際市場
- 國際市場
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入1個線上商店、ServiceInfo 檔
- 輸入2個線上商店、ServiceInfo 檔
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82e2db056f748e1257649716c57a2f1774ee0b1b149966dce3851a75d08c8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580508"
---
# <a name="considerations-for-international-markets"></a>國際市場的考慮

如果您的公司建立多個市場的線上商店，您必須為每個市場提供 Microsoft ServiceInfo 檔的 URL。 您可以透過下列兩種方式之一來執行：

-   為每個市場建立個別的 ServiceInfo 檔。 在此情況下，您會為 Microsoft 提供指向每個市場中每個線上商店之個別 ServiceInfo 檔的 Url。
-   為所有市場建立單一 ServiceInfo 檔。 當您這樣做時，您會為每個市場提供相同的 URL 給 Microsoft。 以 ASP 頁面的形式建立的 ServiceInfo 檔，可以根據查詢字串參數動態偵測使用者的位置。

Windows Media Player 會將查詢字串附加至 ServiceInfo URL 要求，以提供使用者地區設定和位置設定的相關資訊。 如果您的線上商店使用這項資訊來決定要顯示的內容，您應該以動態方式將這些值附加至 ServiceInfo 檔中的您自己的 Url。 這是確保您的網頁 Url 一律會包含您預期之參數的最佳方式。

一旦決定使用者的位置和語言喜好設定之後，您可能會想要在未來的會話中保存此資訊。 您可以使用您通常會在網頁中使用的任何技術，例如 cookie，或使用您的 COM 物件來執行這項作業。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**動態建立 ServiceInfo 檔**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**ServiceInfo 元素**](serviceinfo-element.md)
</dt> </dl>

 

 




