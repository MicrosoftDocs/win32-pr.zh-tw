---
description: Rich Edit 3.0 支援 HexToUnicode IME，可讓使用者以兩種方式的其中一種，使用快速鍵在十六進位和 Unicode 字元之間進行轉換。
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: HexToUnicode IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a57ce56821f200c9fd9ff80560908f5a72ecfdb0f51ce981e1aff40ce785b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068148"
---
# <a name="hextounicode-ime"></a>HexToUnicode IME

Rich Edit 3.0 支援 HexToUnicode IME，可讓使用者以兩種方式的其中一種，使用快速鍵在十六進位和 Unicode 字元之間進行轉換。

使用第一個轉換方法，使用者以十六進位鍵入字元碼，然後輸入 ALT + X。 IME 會以 Unicode 字元取代插入點前面的十六進位數位。 如果目前的字型不支援字元碼，則會選擇支援它的適當字型。 若要從 Unicode 轉換為十六進位，使用者可輸入 SHIFT + ALT + X。 這個專案會將插入點前面的 Unicode 字元取代為十六進位數位。 尤其是，此方法可讓使用者判斷「遺漏圖像」指標所表示的字元。 如果十六進位字元碼緊接在某些合法的 (非字元) 十六進位字元，使用者會選取要在輸入 ALT + X 之前轉換的特定數位。 第一個方法的問題是，ALT + X 有時會用來做為 exit 命令的按鍵組合 (也就是 eXit) 。 例如，在 Microsoft Office 中，此命令只會 **顯示為 [檔案] 功能表的** 選項。

在十六進位和 Unicode 字元之間轉換的第二種方法牽涉到數位板。 使用這個方法時，使用者可以輸入 ALT + NumPad 數位 (值大於 255) ，以使用十進位值輸入 Unicode 字元。 這個方法與第一個方法並不一樣，因為使用者無法看到輸入了哪些十六進位數位。 此外，使用者不能更正十六進位數位，除非重新輸入所有數位。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於輸入方法管理員](about-input-method-manager.md)
</dt> </dl>

 

 



