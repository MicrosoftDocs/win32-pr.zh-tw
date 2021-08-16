---
description: 本主題說明如何建立一般的 MUI 應用程式。
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: 當地語系化資源和建立應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490fde8e0b6d9381b346409efad1501331be71d2d4e958be050274dc0428fe62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788498"
---
# <a name="localizing-resources-and-building-the-application"></a>當地語系化資源和建立應用程式

本主題說明如何建立一般的 MUI 應用程式。 假設您使用 Microsoft Visual Studio 進行程式碼撰寫，並使用 Microsoft Visual Studio 或 Visual Studio 命令列進行建立。 假設您的應用程式使用 .sln 方案檔，並支援資源 .h 檔案來反映基礎語言資源檔。

> [!Note]  
> 如果使用組建的 Visual Studio 命令列，您將使用 **vcbuild** 命令來建立方案檔。

 

應用程式檔會針對每種語言分別建立。 每個組建都會建立相同的語言中性 .exe 以及特定語言的 .exe mui 檔案。 此外，會將不同的其他檔案複製到適當的發行資料夾。

應用程式組建取決於您所使用的資源類型和當地語系化類型。 針對預先組建當地語系化，您有一份針對每個支援語言當地語系化的基礎語言檔案。 針對組建後當地語系化，您可以複製可執行檔和資源模組的組建所產生的 mui 檔案，並將這些複本提供給當地語系化人員。

> [!Note]  
> 下列程式假設 Win32 PE 資源具有一個針對每個語言建立的 Visual Studio 專案。 在 .rc 檔中提供基礎語言資源，並使用 DLL 模組載入。 您可以視需要重複此程式，以建立支援的所有語言。

 

**若要建立應用程式**

1.  設定基礎語言的 Visual Studio 專案。
2.  如果有興趣使用資源設定檔與資源工具，請依照 [準備資源設定檔](preparing-a-resource-configuration-file.md)中所述的方式設定一個。
3.  在專案的屬性頁中，設定 RC 編譯器公用程式所需的參數，[設定屬性] → [資源] → [ **命令列] → [其他選項**]。
4.  執行 RC 編譯器。 此公用程式會使用資源設定資料，將不可當地語系化和可當地語系化的資源編譯並分割成兩個不同的物件檔案。 在這個步驟中，語言中立的資源會連結到 LN 檔。 如需詳細資訊，請參閱 [資源公用程式](resource-utilities.md)中的公用程式描述。
5.  若要將特定語言的資源連結到特定語言的 mui 檔，請在 [設定屬性] → [組建事件] → [ **建立後事件] →命令列** 底下的屬性頁中，為專案設定建立後事件。
6.  設定建立後事件，以將 LN 檔中的總和檢查碼值套用至語言的 mui 檔。 您可以使用 MUIRCT 公用程式進行此步驟。 如需詳細資訊，請參閱 [資源公用程式](resource-utilities.md)中的公用程式描述。
7.  使用後置事件命令列新增命令，以將檔案複製到適當的發行資料夾結構。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用多語系消費者介面](using-multilingual-user-interface.md)
</dt> <dt>

[準備資源設定檔](preparing-a-resource-configuration-file.md)
</dt> <dt>

[資源公用程式](resource-utilities.md)
</dt> </dl>

 

 



