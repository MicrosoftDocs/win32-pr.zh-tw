---
description: 說明如何使用輸入範圍來進行辨識。
ms.assetid: 9faf6d22-b80d-4020-ac74-ee40b31ae9d4
title: 輸入範圍和 Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbb46e21a0524f806daa4eed789fde31e285109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195118"
---
# <a name="input-scopes-and-factoids"></a>輸入範圍和 Factoids

輸入範圍是一組已定義的單字、數位、標點符號和語法排序，可在指定的語言模型內使用。 應用程式可以使用輸入範圍，將辨識器所使用的語言模型限制為特定的內容。 例如，的輸入範圍是 \_ 電子郵件 SMTPEMAILADDRESS 會藉 \_ 由指示特定欄位為電子郵件地址，來影響辨識結果。 因此，此欄位可能包含字元（例如 " @" and " \_ "），而且不能包含 " \* " 和空格等字元。

> [!Note]  
> 其他 Microsoft 技術也會使用輸入範圍。 本文著重于使用內容來改善 Tablet PC 應用程式手寫辨識引擎的精確度。

 

舊版 Tablet PC 技術 API 使用 factoids 來定義內容。 針對實際用途，模擬程式與輸入範圍的內容相同。 第一個版本的 Tablet PC SDK 平臺定義了一 [**組智慧標籤物件中**](factoid-constants.md) 的一組模擬值。 使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件進行辨識時，這些值可用來設定內容和影響辨識結果。 針對從 Windows XP Tablet PC Edition 2005 開始的拉丁腳本辨識器，您仍然可以使用 **RecognizerCoNtext** 物件的 [[**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)] 屬性來設定內容，但您應該傳入輸入範圍、片語清單或手寫的正則運算式值，而不是其中一個版本的模擬值。 東亞字元的 Microsoft 辨識器不支援使用輸入範圍的列舉值。 您應該繼續使用適用于東亞字元辨識器的模擬值。

輸入範圍和 factoids 是文字層級替代項的限制;即使設定了 **強制** 旗標，字元替代字元也可能在指定的輸入範圍之外。

當 **強制** 旗標設定了限制性的條件約束時，辨識器可能會產生兩個都符合筆墨的答案，並符合此條件約束。 辨識器的語言不符合筆墨的語言 (例如，美國英文辨識器和中文筆墨字元) 的另一個情況是，辨識器可能不會產生任何滿意的答案。

當手寫辨識器無法辨識指定單字或字元的筆墨時，它可能會傳回空的替代清單或替代清單，其中第一個選擇是以程式碼點 0xffff (未定義的字元) 。 這特別適用于盒裝的指南輸入模式，其中每個具有筆墨的方塊都預期會有非空白的替代清單。 然後，應用程式就可以用它選擇的任何方式來顯示這個未定義的字元 (例如「???」) 。

> [!Note]  
> 針對回溯相容性，模擬程式值會繼續與拉丁腳本的辨識器搭配運作。

 

如需 factoids 的詳細資訊，請參閱 [設定 Ink-Enabled 控制項的內容](setting-context-for-ink-enabled-controls.md)。

如需東亞 factoids 的詳細資訊，請參閱 [第1版所支援的 factoids](supported-factoids-from-version-1.md)。

 

 



