---
title: 翻譯為 Visual Basic
description: 翻譯為 Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9aa8a163141c6361df464a22ce873770c8385607bdf8f84d333d204c55a327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550612"
---
# <a name="translating-to-visual-basic"></a>翻譯為 Visual Basic

您可以將 COM 物件新增至 Visual Basic 專案中，做為參考或元件。 將物件加入至專案之後，您的應用程式就可以存取其類別和介面。 然後，您可以使用 Visual Basic 的物件瀏覽器，以 Visual Basic 語法來查看物件的型別程式庫資訊。

通常會將控制項新增至專案做為元件，並將 noncontrols 新增為參考。 當 COM 物件加入為元件時，它會出現在 Visual Basic 的 [工具箱] 中。 將物件圖示從 [工具箱] 拖曳至 Visual Basic 表單或其他類型的容器，即可建立該物件的新實例。 加入做為參考的 COM 物件的新實例會使用 **new** 關鍵字來建立。

使用類別做為參考與元件的差異很微妙，但很重要。 當您加入物件做為參考時，您只能使用控制項所提供的類型程式庫，或使用「原始」類型程式庫。

如果您將控制項加入為元件，Visual Basic 會合並以控制項類型程式庫內嵌控制項的表單的擴充項屬性和方法，藉此提供類型程式庫的包裝擴充版本。 使用這個版本的類型程式庫時，您可以使用擴充項屬性（例如 Top 和 Left），如同它們是控制項的一部分，而不是控制項的容器。

Visual Basic 目前不支援內建在單一 .dll 檔案中的多個類型程式庫。 如果您遇到合併多個類型程式庫的 DLL，您應該從提供物件的來源取得類型程式庫的獨立複本，以便搭配 Visual Basic 使用物件。

如需詳細資訊，請參閱下列主題：

-   [從 c + + 翻譯為 Visual Basic](translating-to-visual-basic-from-c--.md)
-   [從 JAVA 轉譯為 Visual Basic](translating-to-visual-basic-from-java.md)
-   [將元件新增至 Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
-   [新增 Visual Basic Project 的參考](adding-a-reference-to-a-visual-basic-project.md)
-   [Visual Basic物件瀏覽器](visual-basic-object-browser.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換成 c + +](translating-to-c--.md)
</dt> <dt>

[轉換成 JAVA](translating-to-java.md)
</dt> </dl>

 

 




