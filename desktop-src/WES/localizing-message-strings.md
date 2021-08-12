---
title: 當地語系化訊息字串
description: 您在資訊清單中指定的每個訊息字串都必須參考資訊清單之當地語系化區段中的字串。
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55b94ea8e8a40de1401cf3aba97488d5531a77b441361e38f1ff98219940afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587896"
---
# <a name="localizing-message-strings"></a>當地語系化訊息字串

您在資訊清單中指定的每個訊息字串都必須參考資訊清單之 **當地語系化** 區段中的字串。 當地語系化區段包含您支援的每個地區設定的字串資料表區段。

下列範例顯示如何定義字串資料表。 您必須指定字串的 **識別碼** 和 **值** 屬性。 您可以使用 **id** 屬性的值來參考資訊清單中的字串。 **Value** 屬性包含當地語系化的字串。


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider" 
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}" 
                symbol="PROVIDER_GUID" 
                resourceFileName="<path to the exe or dll that contains the metadata resources>" 
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.ProviderName)">

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="ProviderName" value="Sample Provider"/>
                <string id="PathNotFound" value="The path %1 was not found."/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```


您應該為每個支援的語言建立多語系使用者介面 (MUI) 檔案，而不是將當地語系化字串加入資訊清單中。 使用訊息文字檔來指定您的當地語系化字串。

下列程式說明如何建立英文和法文的 MUI 檔案。

**若要建立英文和法文的 MUI 檔案**

1.  建立可建立法文訊息字串的訊息文字檔。 如需建立訊息文字檔的詳細資訊，請參閱 [訊息文字檔](/windows/desktop/EventLog/message-text-files)。 您在訊息文字檔中指定的訊息識別碼必須符合訊息編譯器針對資訊清單中的相同字串所產生的資源識別碼。 若要判斷資訊清單中用於字串的資源識別碼，請參閱當您編譯資訊清單時，訊息編譯器所產生的 .h 檔案。
    ```Text
    LanguageNames=(French=0x40C:MSG0040C)

    ; // The following are message definitions.

    MessageId=0x00000065
    SymbolicName=MSG_ProviderName
    Language=French
    <FRENCH STRING GOES HERE>
    .


    MessageId=0x00000066
    SymbolicName=MSG_PathNotFound
    Language=French
    <FRENCH STRING GOES HERE>
    .
    
    ```


2.  執行下列命令，以建立包含當地語系化字串的資源 DLL。 Messages.mc 檔案是您在步驟1中建立的訊息文字檔。
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  在包含您的提供者的資料夾中，針對您支援的每個地區設定建立子資料夾。 子資料夾的名稱必須是該地區設定的語言名稱。 例如，針對0x0409，請使用 en-us 作為資料夾名稱。
4.  建立 rcconfig 檔案，告知 Muirct.exe 工具您要從可執行檔和資源 Dll 分割訊息字串資源。 以下是 rcconfig 檔案的範例。
    ```XML
    <localization>
          <resources>
                <win32Resources fileType="Application">
                      <neutralResources>
                      </neutralResources>
                      <localizedResources>
                            <resourceType typeNameId="#11"/>
                      </localizedResources>
                </win32Resources>
          </resources>
    </localization>
    ```
  

5.  執行下列 Muirct.exe 命令，以將英文字串從提供者可執行檔分割。
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  執行下列 Muirct.exe 命令以將法文字串從資源 DLL 分割。 在建立 MUI 檔案之後，移除 (fr-frmessages.dll) 的中性語言檔案 \\ 。
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  將 provider.exe ln 重新命名為 provider.exe。
