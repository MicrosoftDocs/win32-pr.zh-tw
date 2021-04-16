---
description: 當使用者以滑鼠右鍵按一下 Shell 物件（例如檔案）時，Shell 會顯示快捷方式 (內容) 功能表。
ms.assetid: 4f46b8c3-1e12-447c-87f4-bbe2c305f77a
title: 動詞和檔案關聯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b398b168afe66c3ddd1abe4c78863fbf67ffcbd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550995"
---
# <a name="verbs-and-file-associations"></a>動詞和檔案關聯

當使用者以滑鼠右鍵按一下 Shell 物件（例如檔案）時，Shell 會顯示快捷方式 (內容) 功能表。 此功能表包含使用者可以選取的命令清單，以對專案執行各種動作。 這些命令也稱為快捷方式功能表項目或動詞。 您可以自訂快捷方式功能表。

本主題的組織方式如下：

-   [檔案系統物件的快捷方式功能表簡介](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [將命令新增至快捷方式功能表](#add-commands-to-a-shortcut-menu)
-   [快速鍵功能表動詞](#shortcut-menu-verbs)
-   [串流非檔案系統專案和 OpenSearch 結果。](#stream-non-file-system-items-and-opensearch-results)
-   [註冊應用程式以處理任意檔案類型](#register-an-application-to-handle-arbitrary-file-types)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a>檔案系統物件的快捷方式功能表簡介

因為快捷方式功能表通常用於檔案管理，所以 Shell 會提供一組預設的命令（例如 **剪** 下和 **複製**），這些命令會出現在任何檔案系統物件（例如檔案或資料夾）的快捷方式功能表上。

下列範例說明以滑鼠右鍵按一下 **MyFile.xyz-ms** 所顯示的預設快捷方式功能表。

![預設快捷方式功能表的螢幕擷取畫面](images/context-menu/context-filesystemobjects.png)

預設快捷方式功能表出現 **MyFile.xyz 毫秒** 的原因是因為 **xyz-ms** 不是已註冊檔案類型的成員。 相反地， **.txt** 是已註冊的檔案類型。 如果您以滑鼠右鍵按一下 **.txt** 檔案，就會在上方區段中看到包含三個額外命令的快捷方式功能表： [ **列印**]、[ **編輯** ] 和 [ **開啟檔案**]。

![具有已註冊之檔案類型之檔案的快捷方式功能表的螢幕擷取畫面](images/context-menu/context-registeredfiletype.png)

若要擴充檔案類型的快捷方式功能表，您必須為每個命令建立一個登錄專案。 更複雜的方法是執行 (動詞) 處理常式的快捷方式功能表，可讓您以檔案為基礎，擴充檔案類型的快捷方式功能表。 如需詳細資訊，請參閱 [建立內容功能表處理常式](context-menu-handlers.md)和 [內容功能表參考](context-menu-reference.md)。

### <a name="add-commands-to-a-shortcut-menu"></a>將命令新增至快捷方式功能表

快捷方式功能表處理常式是一種檔案類型處理常式，會將命令新增至現有的快捷方式功能表。 快速鍵功能表處理常式會與檔案類型相關聯，並且在每次顯示類別成員的快捷方式功能表時呼叫。 Shell 會檢查登錄，以查看檔案類型是否與任何快捷方式功能表處理常式相關聯。 如果是，Shell 會查詢其他快捷方式功能表項目的處理常式。

## <a name="shortcut-menu-verbs"></a>快速鍵功能表動詞

快速鍵功能表上的每個命令都是由其動詞命令在登錄中識別。 這些動詞與 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 在以程式設計方式啟動應用程式時所使用的相同。

動詞是簡單的文字字串，可供 Shell 用來識別相關聯的命令。 每個動詞命令都對應至用來在主控台視窗或 batch ( .bat) 檔中啟動命令的命令字串。

例如，open 動詞通常會啟動程式來開啟檔案。 命令字串通常如下所示：


```
"My Program.exe" "%1"
```



如果命令字串的任何元素包含或可能包含空格，則必須以引號括住。 否則，如果元素包含空格，將無法正確剖析。 比方說，「 **我的 Program.exe** 」會正確啟動應用程式。 如果您使用 **我的 Program.exe** 沒有引號，系統就會嘗試以 **Program.exe** 作為第一個命令列引數來啟動 **my** 。 您應該一律使用引號，其中包含引數（例如 **"%1**"），並由 Shell 擴充為字串，因為您無法確定字串不會包含空格。

動詞也可以有相關聯的顯示名稱，這會顯示在快捷方式功能表上，而不是動詞字串本身。 例如，openas 的顯示字串會 **以開啟**。 就像一般的功能表字串一樣，在顯示字串中包含連字號字元，也可以選擇使用鍵盤來選取命令。

## <a name="stream-non-file-system-items-and-opensearch-results"></a>串流非檔案系統專案和 OpenSearch 結果。

在 Windows 7 （含）以後版本中，支援透過 [ [OpenSearch](http://www.opensearch.org/) ] 通訊協定，將外部來源連接到 Windows 用戶端。 這可讓使用者搜尋遠端資料存放區，並從 Windows 檔案總管內查看結果。 OpenSearch v1.1 標準定義了簡單的檔案格式，可用來描述用戶端應該如何查詢資料存放區的 web 服務，以及服務應該如何傳回結果以供用戶端轉譯。

您可能需要串流處理非檔案系統專案，以避免在 [OpenSearch](http://www.opensearch.org/) 結果時下載專案。 同盟搜尋功能可讓您從支援 OpenSearch 的非檔案系統位置（例如 SharePoint 和其他 web 服務支援的網站）搜尋專案。 在這些專案上叫用動詞時，系統會下載專案的暫存版本，並將其傳遞至動詞執行。 建議使用動詞實作者，藉由註冊動詞支援的 URL 架構集合來串流專案，以避免下載檔案。 動詞命令是使用 **SupportedProtocols** 登錄機碼。

## <a name="register-an-application-to-handle-arbitrary-file-types"></a>註冊應用程式以處理任意檔案類型

定義特定檔案類型的快捷方式功能表項目，可讓您指定相關聯的應用程式如何開啟檔案類型的成員。 不過，當使用者嘗試使用應用程式開啟與應用程式沒有關聯的檔案類型時，應用程式也可以註冊個別的預設程式。 您註冊預設程式的方式，與註冊快捷方式功能表項目的方式大致相同。 如需定義快捷方式功能表項目的詳細資訊，請參閱 [建立內容功能表處理常式](context-menu.md)。

預設程式有兩個基本用途。 其中一個方法是指定應該如何叫用應用程式，以開啟任意檔案類型。 比方說，您可以使用命令列旗標來指出正在開啟未知的檔案類型。 另一個用途是定義檔案類型的各種特性，例如快捷方式功能表項目和圖示。 如果使用者將您的應用程式與其他檔案類型產生關聯，該類別將具有這些特性。 如果其他檔案類型先前與另一個應用程式相關聯，這些特性將會取代原始的。

若要註冊預設程式，請將您為應用程式 ProgID 建立的登錄機碼放在 **HKEY \_ 類別 \_ 根 \\ 應用** 程式的應用程式子機碼下。 您也可以包含 **FriendlyAppName** 值，為系統提供易記的應用程式名稱。 應用程式的易記名稱也可以從它的可執行檔中解壓縮，但只有在 FriendlyAppName 值不存在時。

下列範例登錄專案說明定義易記名稱和數個快捷方式功能表項目的 **MyProgram.exe** 預設程式。 命令字串包含 **/a** 旗標，以通知應用程式它正在開啟任意檔案類型。 如果您包含 **DefaultIcon** 子機碼，則應該使用一般圖示。

```
HKEY_CLASSES_ROOT
   MyProgram.exe
      shell
         open
            command
               (Default) = C:\MyDir\MyProgram.exe /a "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2"
```

## <a name="additional-resources"></a>其他資源

-   如需其他背景，請參閱檔案 [關聯簡介](fa-intro.md)。
-   如需有關使用檔案類型處理常式來擴充 Shell 的概念資訊，請參閱 [建立 Shell 擴充處理常式](handlers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速鍵功能表處理常式和多重選取動詞的最佳作法](verbs-best-practices.md)
</dt> <dt>

[為快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)
</dt> <dt>

[建立快捷方式功能表處理常式](context-menu-handlers.md)
</dt> <dt>

[使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[快捷方式 (內容) 功能表和快捷方式功能表處理常式](context-menu.md)
</dt> <dt>

[快速鍵功能表參考](context-menu-reference.md)
</dt> </dl>

 

 



