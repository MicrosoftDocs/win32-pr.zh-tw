---
title: ACF 主體
description: ACF 主體包含設定屬性，適用于在 IDL 檔案的介面主體中定義的類型和函式。
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1446b4f0e14849832766bc512a95d0ae0aeb249cebd814314b617ffa1e1125e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924618"
---
# <a name="the-acf-body"></a>ACF 主體

ACF 主體包含設定屬性，適用于在 IDL 檔案的介面主體中定義的類型和函式。 ACF 的主體可以是空的，也可以包含 ACF [**include**](/windows/desktop/Midl/include)、 [**typedef**](/windows/desktop/Midl/typedef)、function 和 parameter 屬性。 所有這些專案都是選擇性的。 套用至 ACF 主體中個別類型和函式的屬性會覆寫 ACF 標頭中的屬性。

ACF 會指定本機電腦上的行為，而且不會影響透過網路傳輸的資料。 它是用來指定要產生的存根詳細資料。 在 DCE 相容性模式中 ([**/osf**](/windows/desktop/Midl/-osf)) ，此 ACF 不會影響存根之間的互動，而是在存根和應用程式程式碼之間的互動。

在 ACF 中指定的參數必須是 IDL 檔案中指定的其中一個參數。 ACF 中參數的規格順序並不重要，因為比對是依名稱，而不是依位置。 ACF 中的參數清單可以是空的，即使對應的 IDL 簽章中的參數清單不 (，但) 不建議這樣做。 在 IDL 檔案中)  (未具名引數的抽象宣告子，會導致 MIDL 編譯器在處理 ACF 時發生錯誤，因為找不到參數。

ACF **include** 指示詞會指定在產生的標頭中顯示的標頭檔，作為標準 C 預處理器 **\# include** 語句的一部分。 ACF 關鍵字 **包含** 不同于 **\# include** 指示詞。 ACF 關鍵字 **包含** 會導致程式程式碼 "**\# include** *filename*" 出現在產生的標頭檔中，而 C 語言指示詞 "**\# include** *FILENAME*" 則會將該檔案的內容放在 ACF 中。

ACF [**typedef**](/windows/desktop/Midl/typedef) 語句可讓您將 ACF 類型屬性套用至 IDL 檔案中先前定義的類型。 ACF **typedef** 語法與 C **typedef** 語法不同。

ACF 函數屬性可讓您指定套用至整個函數的屬性。 如需詳細資訊，請參閱程式 **\[** [**代碼**](/windows/desktop/Midl/code) **\]** 、 **\[** [**優化**](/windows/desktop/Midl/optimize) **\]** 和 **\[** [**了 nocode**](/windows/desktop/Midl/nocode) **\]** 。

ACF 參數屬性可讓您指定套用至函數之個別參數的屬性。 如需詳細資訊，請參閱 **\[** [**位元組 \_ 計數**](/windows/desktop/Midl/byte-count) **\]** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**/app \_ 設定**](/windows/desktop/Midl/-app-config)
</dt> <dt>

[**/osf**](/windows/desktop/Midl/-osf)
</dt> <dt>

[**\[自動 \_ 處理\]**](../midl/auto-handle.md)
</dt> <dt>

[**\[代碼\]**](../midl/code.md)
</dt> <dt>

[**\[明確 \_ 控制碼\]**](../midl/explicit-handle.md)
</dt> <dt>

[介面定義語言 (IDL) 檔](the-interface-definition-language-idl-file.md)
</dt> <dt>

[**\[隱含 \_ 控制碼\]**](../midl/implicit-handle.md)
</dt> <dt>

[**包括**](/windows/desktop/Midl/include)
</dt> <dt>

[midl](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

[**\[了 nocode\]**](../midl/nocode.md)
</dt> <dt>

[**\[優化\]**](../midl/optimize.md)
</dt> <dt>

[**\[表示 \_ 為\]**](../midl/represent-as.md)
</dt> <dt>

[**著**](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 