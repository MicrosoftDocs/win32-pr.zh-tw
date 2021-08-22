---
title: 轉換程式設計語言的 COM 物件語法
description: 轉換程式設計語言的 COM 物件語法
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6871046a80537dd39b4c9b502d945e28e46e719e637c4e6a629179dd3c6454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500078"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a>轉換程式設計語言的 COM 物件語法

若要從以程式設計語言撰寫的應用程式呼叫 COM 物件，而非用來寫入 COM 物件的應用程式，您必須先將物件的語法轉譯為程式設計語言。 您可以使用下列步驟來完成此動作：

1.  以程式設計語言的語法來查看 COM 物件的類型程式庫。 這樣做會以您所使用的語言語法，提供物件的類別、介面、方法、屬性和事件的描述。

    Microsoft 開發人員產品提供數個工具，可協助您流覽和轉換型別程式庫。 如需詳細資訊，請參閱 [類型程式庫檢視器和轉換工具](type-library-viewers-and-conversion-tools.md) ，以及 [開發人員工具使用類型程式庫的方式](how-developer-tools-use-type-libraries.md)。

    一旦您可以用慣用的程式設計語言來查看物件的類型程式庫，您就可以在物件的檔中比較其語法。 如果物件是以您所使用的程式設計語言所記載，則資料類型和語法可能會不同，但參數、傳回值和物件功能的描述應該相同。

2.  將翻譯成您的程式設計語言的任何特殊考慮納入考慮。

    因為每種程式設計語言都定義了在其他語言中可能沒有對等的概念，所以某些物件的功能可能會以不同的方式運作，或完全無法使用。 例如，Visual Basic 程式設計語言無法辨識 c + + 不帶正負號的資料類型，例如 **unsignedÂ long**。 以 Visual Basic 撰寫的應用程式無法使用接受或傳回未簽署資料類型變數的 COM 方法。

3.  將 COM 物件的已編譯器代碼加入至您的專案。 已編譯的程式碼通常包含在 .dll 或 .ocx 檔案中。 編譯器必須要有這個步驟，才能辨識 COM 物件的類別。 新增 COM 物件之後，您的應用程式可以使用其類別和介面。

下列主題描述如何以各種程式設計語言轉譯和使用 COM 物件：

-   [轉換成 c + +](translating-to-c--.md)
-   [翻譯為 Visual Basic](translating-to-visual-basic.md)
-   [轉換成 JAVA](translating-to-java.md)

這些主題說明 Microsoft developer 產品所提供的轉換工具和流程。 如需有關如何使用其他公司所建立的開發工具來撰寫 COM 物件的指示，請參閱這些開發工具的檔。

 

 




