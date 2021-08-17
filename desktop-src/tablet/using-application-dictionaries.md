---
description: 根據預設，辨識器會使用系統字典，其中包含所有常用的語言文字。
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: 使用應用程式字典
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c83013f704fe28b5754ab89fd95ed730e16d1cda5ab257d4fb411d0e7293347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449230"
---
# <a name="using-application-dictionaries"></a>使用應用程式字典

根據預設，辨識器會使用系統字典，其中包含所有常用的語言文字。 此外，辨識器具有使用者字典，其中包含使用者已新增至字典的單字。 使用者可以透過 [Tablet PC 輸入面板]，透過 [Tablet PC 輸入面板]，透過 [Tablet PC 輸入面板] 將

-   寫入) 時 (替代清單。
-   語音工具功能表 (說話) 。

如果您要設計應用程式，讓使用者能夠撰寫在系統字典或使用者字典中找不到的單字，請建立應用程式字典。 應用程式字典提供辨識器額外的自訂字詞清單，可能會以手寫形式輸入到應用程式中，藉此提升辨識準確度。

您可以使用 [**單詞表**](inkwordlist-class.md) 物件來建立應用程式字典。 後續的應用程式字典藉由提供辨識器與預期的單字清單來增加辨識精確度。 例如，包含醫學術語的應用程式字典會在針對醫療產業開發的應用程式中增加辨識精確度，而該應用程式可能會撰寫詞彙。

另一個例子是，當您設計表單以訂購音樂器材時，請建立一個包含最常見檢測製造商名稱的 [**單詞表**](inkwordlist-class.md) 物件。 將 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件的 [[**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)] 屬性設定為您所建立的 **單詞表** 物件。 然後， **RecognizerCoNtext** 物件會將這份單字清單傳遞給辨識器。 應用程式字典會在應用程式中的欄位寫入這些名稱時，增加辨識精確度。

下列主題描述如何使用應用程式字典。

-   [瞭解單字清單、辨識器內容和 Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [使用應用程式字典搭配 Tablet PC 平臺 Api](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [建立手寫辨識的自訂字典](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



