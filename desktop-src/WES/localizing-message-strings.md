---
title: 當地語系化訊息字串
description: 您在資訊清單中指定的每個訊息字串都必須參考資訊清單之當地語系化區段中的字串。
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7812aed8bf376994a2cbecfa5997737d9740ec1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023777"
---
# <a name="localizing-message-strings"></a><span data-ttu-id="3cf6c-103">當地語系化訊息字串</span><span class="sxs-lookup"><span data-stu-id="3cf6c-103">Localizing Message Strings</span></span>

<span data-ttu-id="3cf6c-104">您在資訊清單中指定的每個訊息字串都必須參考資訊清單之 **當地語系化** 區段中的字串。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-104">Each message string that you specify in the manifest must reference a string in the **localization** section of the manifest.</span></span> <span data-ttu-id="3cf6c-105">當地語系化區段包含您支援的每個地區設定的字串資料表區段。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-105">The localization section contains a string table section for each locale that you support.</span></span>

<span data-ttu-id="3cf6c-106">下列範例顯示如何定義字串資料表。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-106">The following example shows how to define a string table.</span></span> <span data-ttu-id="3cf6c-107">您必須指定字串的 **識別碼** 和 **值** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-107">You must specify the string's **id** and **value** attributes.</span></span> <span data-ttu-id="3cf6c-108">您可以使用 **id** 屬性的值來參考資訊清單中的字串。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-108">You use the value of the **id** attribute to reference the string in your manifest.</span></span> <span data-ttu-id="3cf6c-109">**Value** 屬性包含當地語系化的字串。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-109">The **value** attribute contains the localized string.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
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


<span data-ttu-id="3cf6c-110">您應該為每個支援的語言建立多語系使用者介面 (MUI) 檔案，而不是將當地語系化字串加入資訊清單中。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-110">Instead of adding localized strings to the manifest, you should create a multilingual user interface (MUI) file for each language that you support.</span></span> <span data-ttu-id="3cf6c-111">使用訊息文字檔來指定您的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-111">Use a message text file to specify your localized strings.</span></span>

<span data-ttu-id="3cf6c-112">下列程式說明如何建立英文和法文的 MUI 檔案。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-112">The following procedure describes how to create a MUI file for English and French.</span></span>

<span data-ttu-id="3cf6c-113">**若要建立英文和法文的 MUI 檔案**</span><span class="sxs-lookup"><span data-stu-id="3cf6c-113">**To create a MUI file for English and French**</span></span>

1.  <span data-ttu-id="3cf6c-114">建立可建立法文訊息字串的訊息文字檔。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-114">Create a message text file that creates the French message strings.</span></span> <span data-ttu-id="3cf6c-115">如需建立訊息文字檔的詳細資訊，請參閱 [訊息文字檔](/windows/desktop/EventLog/message-text-files)。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-115">For details on creating a message text file, see [Message Text Files](/windows/desktop/EventLog/message-text-files).</span></span> <span data-ttu-id="3cf6c-116">您在訊息文字檔中指定的訊息識別碼必須符合訊息編譯器針對資訊清單中的相同字串所產生的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-116">The message identifiers that you specify in the message text file must match the resource identifiers that the message compiler generated for the same strings in the manifest.</span></span> <span data-ttu-id="3cf6c-117">若要判斷資訊清單中用於字串的資源識別碼，請參閱當您編譯資訊清單時，訊息編譯器所產生的 .h 檔案。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-117">To determine the resource identifiers used for the strings in the manifest, see the .h file that the message compiler generated when you compiled the manifest.</span></span>
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


2.  <span data-ttu-id="3cf6c-118">執行下列命令，以建立包含當地語系化字串的資源 DLL。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-118">Run the following commands to create the resource DLL that contains your localized strings.</span></span> <span data-ttu-id="3cf6c-119">Messages.mc 檔案是您在步驟1中建立的訊息文字檔。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-119">The messages.mc file is the message text file that you created in step 1.</span></span>
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  <span data-ttu-id="3cf6c-120">在包含您的提供者的資料夾中，針對您支援的每個地區設定建立子資料夾。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-120">In the folder that contains your provider, create a subfolder for each locale that you support.</span></span> <span data-ttu-id="3cf6c-121">子資料夾的名稱必須是該地區設定的語言名稱。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-121">The name of the subfolder must be the language name for that locale.</span></span> <span data-ttu-id="3cf6c-122">例如，針對0x0409，請使用 en-us 作為資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-122">For example, for 0x0409, use en-US as the folder name.</span></span>
4.  <span data-ttu-id="3cf6c-123">建立 rcconfig 檔案，告知 Muirct.exe 工具您要從可執行檔和資源 Dll 分割訊息字串資源。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-123">Create a .rcconfig file that tells the Muirct.exe tool that you want to split the message string resources from the executable and the resource DLLs.</span></span> <span data-ttu-id="3cf6c-124">以下是 rcconfig 檔案的範例。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-124">The following is an example .rcconfig file.</span></span>
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
  

5.  <span data-ttu-id="3cf6c-125">執行下列 Muirct.exe 命令，以將英文字串從提供者可執行檔分割。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-125">Run the following Muirct.exe commands to split the English strings from the provider executable file.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  <span data-ttu-id="3cf6c-126">執行下列 Muirct.exe 命令以將法文字串從資源 DLL 分割。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-126">Run the following Muirct.exe commands to split the French strings from the resource DLL.</span></span> <span data-ttu-id="3cf6c-127">在建立 MUI 檔案之後，移除 (fr-frmessages.dll) 的中性語言檔案 \\ 。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-127">Remove the language neutral file (fr-FR\\messages.dll) after the MUI file is created.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  <span data-ttu-id="3cf6c-128">將 provider.exe ln 重新命名為 provider.exe。</span><span class="sxs-lookup"><span data-stu-id="3cf6c-128">Rename provider.exe.ln to provider.exe.</span></span>