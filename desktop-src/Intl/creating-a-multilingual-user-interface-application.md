---
description: 本教學課程示範如何取得單一語言應用程式，並讓它成為世界級的應用程式。 此應用程式是以 Microsoft Visual Studio 內建的完整方案形式。
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: 將多語系消費者介面支援新增至應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851828"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a>將多語系消費者介面支援新增至應用程式

本教學課程示範如何取得單一語言應用程式，並讓它成為世界級的應用程式。 此應用程式是以 Microsoft Visual Studio 內建的完整方案形式。

-   [概觀](#splitting-the-various-language-resource-modules-an-overview)
    -   [Hello MUI 背後的構想](#the-idea-behind-hello-mui)
-   [設定 Hello MUI 方案](#setting-up-the-hello-mui-solution)
    -   [平臺需求](#platform-requirements)
    -   [先決條件](#prerequisites)
-   [步驟0：建立硬式編碼的 Hello MUI](#step-0-creating-the-hard-coded-hello-mui)
-   [步驟1：執行基本資源模組](#step-1-implementing-the-basic-resource-module)
-   [步驟2：建立基本資源模組](#step-2-building-the-basic-resource-module)
    -   [分割各種語言資源模組：總覽](#splitting-the-various-language-resource-modules-an-overview)
    -   [分割不同的語言資源模組：建立檔案](#splitting-the-various-language-resource-modules-creating-the-files)
-   [步驟3：建立 Resource-Savvy "Hello MUI"](#step-3-creating-a-resource-savvy-hello-mui)
-   [步驟4：全球化「Hello MUI」](#step-4-globalizing-hello-mui)
-   [步驟5：自訂 "Hello MUI"](#step-5-customizing-hello-mui)
-   [MUI 的其他考慮](#additional-considerations-for-mui)
    -   [主控台應用程式的支援](#support-for-console-applications)
    -   [判斷在執行時間支援的語言](#determination-of-languages-to-support-at-run-time)
    -   [Windows Vista 之前版本中的複雜字集支援](#complex-script-support-in-versions-prior-to-windows-vista)
-   [總結](#summary)

## <a name="overview"></a>概觀

從 Windows Vista 開始，Windows 作業系統本身的建立是多語系平臺，可讓您建立使用 Windows MUI 資源模型的多語系應用程式，並提供額外的支援。

本教學課程說明這項新的多語系應用程式支援，包括下列層面：

-   使用改良的 MUI 平臺支援，輕鬆地啟用多語系應用程式。
-   擴充多語系應用程式，在 Windows Vista 之前的 Windows 版本上執行。
-   請考慮開發專用的多語系應用程式（例如主控台應用程式）所需的其他考慮。

這些連結可協助您快速複習國際化與 MUI 的概念：

-   [國際化簡介](understanding-internationalization.md)。
-   [MUI 概念](understanding-mui.md)。
-   [使用 MUI 開發 Win32 應用程式](using-multilingual-user-interface.md)。

### <a name="the-idea-behind-hello-mui"></a>Hello MUI 背後的構想

您可能已經熟悉傳統的 Hello World 應用程式，其中說明基本的程式設計概念。 本教學課程採用類似的方法來說明如何使用 MUI 資源模型來更新單一語言應用程式，以建立名為 Hello MUI 的多國語言版本。

> [!Note]  
> 本教學課程中的工作會在詳細步驟中說明，因為這些活動必須執行的有效位數，以及對這些工作沒有經驗的開發人員說明詳細資料的需要。

 

## <a name="setting-up-the-hello-mui-solution"></a>設定 Hello MUI 方案

這些步驟概述如何準備建立 Hello MUI 方案。

### <a name="platform-requirements"></a>平台需求

您必須使用適用于 Windows 7 的 Windows 軟體開發套件 (SDK) 和 Visual Studio 2008，在本教學課程中編譯器代碼範例。 Windows 7 SDK 會安裝在 Windows XP、Windows Vista 和 Windows 7 上，而範例解決方案可以建立在這些作業系統版本上。

本教學課程中的所有程式碼範例都是設計來在 x86 和 x64 版本的 Windows XP、Windows Vista 和 Windows 7 上執行。 在適當的情況下，將不會在 Windows XP 上運作的特定部分會被呼叫。

### <a name="prerequisites"></a>必要條件

1.  安裝 Visual Studio 2008。

    如需詳細資訊，請參閱 [Visual Studio 開發人員中心](https://msdn.microsoft.com/vstudio/default.aspx)。

2.  安裝適用于 Windows 7 的 Windows SDK。

    您可以從 [Windows 開發人員中心](https://msdn.microsoft.com/windowsserver/bb980924.aspx)的 [Windows SDK] 頁面進行安裝。 SDK 包含從 Windows XP 到最新版本的作業系統版本開發應用程式的公用程式。

    > [!Note]  
    > 如果您未將套件安裝到預設位置，或者您不是在系統磁片磁碟機（通常是 C 磁片磁碟機）上安裝，請記下安裝路徑。

     

3.  設定 Visual Studio 命令列參數。

    1.  開啟 Visual Studio 的命令視窗。
    2.  輸入 **集路徑**。
    3.  確認 path 變數包含 Windows 7 SDK 的 bin 資料夾路徑： .。。Microsoft Sdk \\ Windows \\ 7.0 版 \\

4.  安裝 Microsoft NLS 下層 Api 附加元件套件。
    > [!Note]  
    > 在本教學課程的內容中，只有當您要自訂應用程式，才能在 windows Vista 之前的 Windows 版本上執行時，才需要此套件。 請參閱 [步驟5：自訂 HELLO MUI](#step-5-customizing-hello-mui)。

     

    1.  從其 [下載網站](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en)下載並安裝套件。
    2.  如同 Windows SDK，如果您未將套件安裝到預設位置，或者您不是安裝在系統磁片磁碟機（通常是 C 磁片磁碟機），請記下安裝路徑。
    3.  如果您的開發平臺是 Windows XP 或 Windows Server 2003，請確認已正確安裝及註冊 Nlsdl.dll。

        1.  流覽至安裝路徑位置下的「可轉散發套件」資料夾。
        2.  執行適當的可轉散發套件 \* Nlsdl。exe，例如 nlsdl.x86.exe。 此步驟會安裝並註冊 Nlsdl.dll。

    > [!Note]  
    > 如果您開發的應用程式使用 MUI，而且必須在 windows Vista 之前的 Windows 版本上執行，則 Nlsdl.dll 必須存在於目的地 Windows 平臺上。 在大部分的情況下，這表示應用程式必須執行可轉散發 Nlsdl 安裝程式 (，而不只是複製 Nlsdl.dll 本身) 。

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a>步驟0：建立硬式編碼的 Hello MUI

本教學課程的開頭是 Hello MUI 應用程式的單一語言版本。 應用程式會假設使用 c + + 程式設計語言、寬字元字串和 [**>messageboxw**](/windows/win32/api/winuser/nf-winuser-messagebox) 函式進行輸出。

首先，建立初始 GuiStep \_ 0 應用程式以及 HelloMUI 方案，其中包含本教學課程中的所有應用程式。

1.  在 Visual Studio 2008 中，建立新專案。 使用下列設定和值：

    1.  專案類型：在 Visual C++ 選取 [Win32]，然後在 [Visual Studio 安裝的範本] 底下選取 [Win32 專案]。
    2.  名稱： GuiStep \_ 0。
    3.  位置： *ProjectRootDirectory* (稍後的步驟會參考此目錄) 。
    4.  解決方案名稱： HelloMUI。
    5.  選取 [為方案建立目錄]。
    6.  在 Win32 應用程式精靈中，選取預設的應用程式類型： Windows 應用程式。

2.  設定專案執行緒模型：

    1.  在方案總管中，以滑鼠右鍵按一下專案 GuiStep \_ 0，然後選取 [屬性]。
    2.  在 [專案屬性頁] 對話方塊中：

        1.  在左上方的下拉式清單中，將 [設定] 設定為 [所有設定]。
        2.  在 [設定屬性] 下展開 [C/c + +]，選取 [程式碼產生]，並設定執行時間程式庫：多執行緒的 Debug () /MTd

3.  \_以下列程式碼取代 GuiStep 0 .cpp 的內容：
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  建置並執行應用程式。

上述直接原始程式碼可讓您以簡單的方式設計選項來進行硬式編碼或內嵌，讓使用者看到的所有輸出（在此案例中為文字 "Hello MUI"）。 這項選擇會限制無法辨識英文文字 "Hello" 之使用者的應用程式公用程式。 因為 MUI 是以技術為基礎的英文縮寫，所以在本教學課程中會假設它是所有語言的字串「MUI」。

## <a name="step-1-implementing-the-basic-resource-module"></a>步驟1：執行基本資源模組

Microsoft Win32 有很長的功能，可讓應用程式開發人員將其 UI 資源資料與應用程式原始程式碼分開。 這種分隔會以 Win32 資源模型的形式呈現，在此模式中，會將字串、點陣圖、圖示、訊息和其他通常顯示給使用者的專案封裝到可執行檔的相異區段中，並與可執行程式碼分開。

為了說明可執行程式碼與資源資料封裝之間的分隔，在此步驟中，教學課程會將先前硬式編碼的 "Hello" 字串放 ("en-us" 資源) 至 HelloModule \_ en us 專案中 DLL 模組的資源區段 \_ 。

此 Win32 DLL 也可以包含程式庫類型可執行檔功能 (因為任何其他 DLL 可能) 。 但為了協助您專注于 Win32 資源相關層面，我們會將執行時間 DLL 程式碼 stub 在 dllmain 中。 本教學課程的後續章節會使用此處建立的 HelloModule 資源資料，也會顯示適當的執行時間程式碼。

若要建立 Win32 資源模組，請從建立具有 stub out dllmain 的 DLL 開始：

1.  將新專案新增至 HelloMUI 方案：

    1.  在 [檔案] 功能表中，選取 [加入]，然後選取 [新增專案]。
    2.  專案類型： Win32 專案。
    3.  名稱： HelloModule \_ en \_ us。
    4.  位置： *ProjectRootDirectory* \\ HelloMUI。
    5.  在 [Win32 應用程式] 中，選取 [應用程式類型： DLL]。

2.  設定此專案的執行緒模型：

    1.  在 [方案總管中，以滑鼠右鍵按一下 HelloModule 的專案， \_ \_ 然後選取 [屬性]。
    2.  在專案的 [屬性頁] 對話方塊中：

        1.  在左上方的下拉式清單中，將 [設定] 設定為 [所有設定]。
        2.  在 [設定屬性] 下展開 [C/c + +]，選取 [程式碼產生]，並設定執行時間程式庫：多執行緒的 Debug () /MTd

3.  檢查 dllmain .cpp。  (您可能會想要將未參考的 \_ 參數宏新增至產生的程式碼（如我們在此所示），讓它能夠在警告層級4進行編譯。 ) 
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  將 HelloModule 的資源定義檔新增至專案：

    1.  在 [專案] \_ HelloModule \_ 中，以滑鼠右鍵按一下 [資源檔] 資料夾，然後選取 [加入]，再選取 [新增專案]。
    2.  在 [加入新專案] 對話方塊中，選擇下列專案：

        1.  類別：在 Visual C++ 選取資源] 底下，然後在 [Visual Studio 安裝的範本] 下，選取 [資源檔] ( .rc) 。
        2.  名稱： HelloModule。
        3.  位置：接受預設值。
        4.  按一下 [新增]。

    3.  指定要將新的 HelloModule .rc 檔儲存為 Unicode：

        1.  在方案總管中，以滑鼠右鍵按一下 HelloModule，然後選取 [視圖程式碼]。
        2.  如果您看到一則訊息，告訴您檔案已開啟，並詢問您是否要關閉它，請按一下 [是]。
        3.  當檔案顯示為文字時，請選取功能表選取檔案，然後選取 [Advanced Save Options]。
        4.  在 [編碼] 下，指定 [Unicode-字碼頁 1200]。
        5.  按一下 [確定]。
        6.  儲存並關閉 HelloModule .rc。

    4.  新增包含 "Hello" 字串的字串資料表：

        1.  在資源檢視中，以滑鼠右鍵按一下 HelloModule，然後選取 [新增資源]。
        2.  選取 [字串資料表]。
        3.  按一下 \[新增\]。
        4.  將字串新增至字串資料表：

            1.  識別碼： HELLO \_ MUI \_ STR \_ 0。
            2.  值：0。
            3.  標題： Hello。

        如果您立即以文字形式來查看 HelloModule，您會看到各種資源專屬的原始程式碼。 其中一個最重要的是描述 "Hello" 字串的區段：

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        這個 "Hello" 字串是需要當地語系化的資源 (也就是，轉譯) 為應用程式希望支援的所有語言。 例如， \_ \_ 您將在下一個步驟中建立的 project (中的 HelloModule ta) 將會包含其專屬的 HelloModule .rc 版本（適用于 "TA-in"）：

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  建立 HelloModule \_ en \_ us 專案，以確定沒有任何錯誤。

5.  在 HelloMUI 方案中建立六個以上的專案 (或您想要的多個專案，) 為其他語言建立額外六個資源 Dll。 使用下表中的值：

    | 專案名稱        | .Rc 檔的名稱 | 字串識別碼          | 字串值 | 字串標題 |
    |---------------------|------------------|--------------------|--------------|----------------|
    | HelloModule \_ de \_ | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | 喂          |
    | HelloModule \_ es \_ es | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | 你好           |
    | HelloModule \_ fr \_ fr | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | 你好        |
    | HelloModule \_ 嗨 \_ | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | नमस्           |
    | HelloModule \_ ru \_ ru | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | Здравствуйте   |
    | HelloModule \_ ta \_ | HelloModule      | HELLO \_ MUI \_ STR \_ 0 | 0            | வணக்கம்        |

    

     

如需 .rc 檔結構和語法的詳細資訊，請參閱 [關於資源檔](../menurc/about-resource-files.md)。

## <a name="step-2-building-the-basic-resource-module"></a>步驟2：建立基本資源模組

使用先前的資源模型，建立七個 HelloModule 專案中的任一個，會產生七個不同的 Dll。 每個 DLL 都會包含一個資源區段，並將單一字串當地語系化成適當的語言。 雖然適用于歷史的 Win32 資源模型，但這項設計不會利用 MUI。

在 Windows Vista SDK 和更新版本中，MUI 提供將可執行檔分割為原始程式碼和可當地語系化內容模組的功能。 使用步驟5稍後所涵蓋的其他自訂，可以讓應用程式在 Windows Vista 之前的版本上執行多語言支援。

從 Windows Vista 開始，可從可執行程式碼分割資源的主要機制如下：

-   使用 rc.exe (RC 編譯器) 的特定參數，或
-   使用名為 muirct.exe 的建立後樣式分割工具。

如需詳細資訊，請參閱 [資源公用程式](resource-utilities.md) 。

為了簡單起見，本教學課程會使用 muirct.exe 來分割 "Hello MUI" 可執行檔。

### <a name="splitting-the-various-language-resource-modules-an-overview"></a>分割各種語言資源模組：總覽

多部分進程牽涉到將 Dll 分割成一個可執行檔 HelloModule.dll，再加上此教學課程中支援的七種語言的 HelloModule.dll。 本總覽說明所需的步驟;下一節會顯示執行這些步驟的命令檔。

首先，使用下列命令來分割僅限英文的 HelloModule.dll 模組：


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



上述命令列使用設定檔 DoReverseMuiLoc. rcconfig。 muirct.exe 通常會使用這種類型的設定檔來分割非語言相關 (LN) DLL 和與語言相關的 mui 檔案之間的資源。 在此情況下，下一節中所列的 DoReverseMuiLoc. rcconfig (xml 檔案) 表示許多資源類型，但全都落在 "localizedResources" 或 mui 檔案類別中，而且沒有語言中立類別中的資源。 如需如何準備資源設定檔的詳細資訊，請參閱 [準備資源設定檔](preparing-a-resource-configuration-file.md)。

除了建立包含英文字串 "Hello" 的 HelloModule.dll mui 檔案，muirct.exe 也會在分割期間將 MUI 資源內嵌到 HelloModule.dll 模組。 為了在執行時間適當地從特定語言的 HelloModule.dll mui 模組載入適當的資源，每個 mui 檔案都必須修正其總和檢查碼，以符合基準語言中性之 LN 模組中的總和檢查碼。 這是透過下列命令來完成：


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



同樣地，也會叫用 muirct.exe，為每個其他語言建立 HelloModule.dll 的 mui 檔。 不過，在這些情況下，會捨棄非語言相關 DLL，因為只需要第一個建立的 DLL。 處理西班牙文和法文資源的命令看起來像這樣：


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



上述 muirct.exe 命令列中最重要的一件事，就是使用-x 旗標來指定目標語言識別項。 針對每個語言特定的 HelloModule.dll 模組，提供給 muirct.exe 的值不同。 這個語言值是 central，可供 muirct.exe 在分割期間適當地標記 mui 檔。 不正確的值會在執行時間為該特定的 mui 檔案產生資源載入失敗。 如需將語言名稱對應至 LCID 的詳細資訊，請參閱 [語言識別項常數和字串](language-identifier-constants-and-strings.md) 。

每個分割的 mui 檔案最後都會放置在與語言中立的 HelloModule.dll 所在的目錄之下，與其語言名稱相對應的目錄。 如需有關 mui 檔案放置的詳細資訊，請參閱 [應用程式部署](application-deployment.md)。

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a>分割不同的語言資源模組：建立檔案

在本教學課程中，您會建立一個命令檔，其中包含用來分割各種 Dll 的命令，而且您會以手動方式叫用它。 請注意，在實際的開發工作中，您可以在 HelloMUI 方案中將這些命令納入預先建立或後置事件，以降低組建錯誤的可能性，但這已超出本教學課程的範圍。

建立偵錯工具組建的檔案：

1.  建立包含下列命令的命令檔 DoReverseMuiLoc：
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  建立包含下列幾行的 xml 檔案 DoReverseMuiLoc rcconfig：
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  將 DoReverseMuiLoc 和 DoReverseMuiLoc 複製到 *ProjectRootDirectory* \\ HelloMUI \\ Debug。
4.  開啟 Visual Studio 2008 命令提示字元，然後流覽至 Debug 目錄。
5.  執行 DoReverseMuiLoc .cmd。

當您建立發行組建時，會將相同的 DoReverseMuiLoc 和 DoReverseMuiLoc. rcconfig 檔案複製到發行目錄，然後在該處執行命令檔。

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a>步驟3：建立 Resource-Savvy "Hello MUI"

根據上述的初始硬式編碼 GuiStep \_0.exe 範例，您可以選擇納入 Win32 資源模型，將應用程式的範圍延伸至多個語言使用者。 此步驟中所提供的新執行時間程式碼包括模組載入 ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) 和字串抓取 ([**loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa)) 邏輯。

1.  將新專案加入至 HelloMUI 方案 (使用功能表選取檔案、加入，以及使用下列設定和值的新專案) ：

    1.  專案類型： Win32 專案。
    2.  名稱： GuiStep \_ 1。
    3.  位置：接受預設值。
    4.  在 Win32 應用程式精靈中，選取預設的應用程式類型： Windows 應用程式。

2.  將這個專案設定為從 Visual Studio 中執行，並設定其執行緒模型：

    1.  在方案總管中，以滑鼠右鍵按一下專案 GuiStep \_ 1，然後選取 [設定為啟始專案]。
    2.  再以滑鼠右鍵按一下它，然後選取 [屬性]。
    3.  在專案的 [屬性頁] 對話方塊中：

        1.  在左上方的下拉式清單中，將 [設定] 設定為 [所有設定]。
        2.  在 [設定屬性] 下展開 [C/c + +]，選取 [程式碼產生]，並設定執行時間程式庫：多執行緒的 Debug () /MTd

3.  將 GuiStep 1 .cpp 的內容取代為 \_ 下列程式碼：
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  建置並執行應用程式。 輸出將會以目前設定為電腦顯示語言的語言來顯示 (前提是這是我們建立) 的七種語言之一。

## <a name="step-4-globalizing-hello-mui"></a>步驟4：全球化「Hello MUI」

雖然先前的範例能夠以不同的語言顯示其輸出，但在許多方面都很短。 最明顯的是，應用程式只在與 Windows 作業系統本身相較之下，只有一小部分的語言才能使用。 例如，如果上一個 \_ 步驟中的 GuiStep 1 應用程式是安裝在日文版的 Windows 上，則可能會發生資源位置失敗。

若要解決這種情況，您有兩個主要選項：

-   確定已包含預先決定的終極回溯語言中的資源。
-   提供一種方式，讓終端使用者從應用程式特別支援的語言子集設定其語言喜好設定。

在這些選項中，強烈建議使用提供終極回溯語言的方法，並藉由將-g 旗標傳遞給 muirct.exe （如上所示），在本教學課程中執行此動作。 此旗標會指示 muirct.exe 將特定語言 (de/0x0407) 與語言中立的 dll 模組相關聯的最終回溯語言 (HelloModule.dll) 。 在執行時間，此參數是用來產生要對使用者顯示之文字的最後手段。 如果找不到終極的回溯語言，而且語言中立的二進位檔中沒有適當的資源，載入資源將會失敗。 因此，您應該仔細判斷應用程式可能會遇到的案例，並據以規劃最終的回溯語言。

另一個可讓您根據此使用者定義階層進行可設定的語言喜好設定和載入資源的選項，可以大幅提升客戶滿意度。 可惜的是，它也會使應用程式內所需的功能變得更複雜。

本教學課程的這個步驟使用簡化的文字檔機制來啟用自訂使用者語言設定。 應用程式會在執行時間剖析文字檔，並且使用剖析和驗證的語言清單來建立自訂的回溯清單。 建立自訂的回溯清單之後，Windows Api 會根據此清單中所述的語言優先順序來載入資源。 程式碼的其餘部分類似于上一個步驟中找到的程式碼。

1.  將新專案加入至 HelloMUI 方案 (使用功能表選取檔案、加入，以及使用下列設定和值的新專案) ：

    1.  專案類型： Win32 專案。
    2.  名稱： GuiStep \_ 2。
    3.  位置：接受預設值。
    4.  在 Win32 應用程式精靈中，選取預設的應用程式類型： Windows 應用程式。

2.  將這個專案設定為從 Visual Studio 中執行，並設定其執行緒模型：

    1.  在方案總管中，以滑鼠右鍵按一下專案 GuiStep \_ 2，然後選取 [設定為啟始專案]。
    2.  再以滑鼠右鍵按一下它，然後選取 [屬性]。
    3.  在專案的 [屬性頁] 對話方塊中：

        1.  在左上方的下拉式清單中，將 [設定] 設定為 [所有設定]。
        2.  在 [設定屬性] 下展開 [C/c + +]，選取 [程式碼產生]，並設定執行時間程式庫：多執行緒的 Debug () /MTd

3.  以下列程式碼取代 GuiStep 2 的內容 \_ ：
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  建立包含下列這一行的 Unicode 文字檔 langs.txt：

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > 務必將檔案儲存為 Unicode。

     

    將 langs.txt 複製到程式執行所在的目錄：

    -   如果從 Visual Studio 內執行，請將它複製到 *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2。
    -   如果從 Windows 檔案總管執行，請將它複製到 GuiStep2.exe 的相同目錄中 \_ 。

5.  建置並執行專案。 嘗試編輯 langs.txt，讓不同的語言出現在清單前端。

## <a name="step-5-customizing-hello-mui"></a>步驟5：自訂 "Hello MUI"

在本教學課程中，到目前為止提到的一些執行時間功能，僅適用于 Windows Vista 和更新版本。 您可以讓應用程式在舊版 Windows 作業系統版本（例如 Windows XP）上運作，以重複使用投資于當地語系化和分割資源的工作。 此程式牽涉到調整上述兩個主要區域中的範例：

-   Windows Vista 之前的資源載入函式 (例如 [**loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa)、 [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)、 [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa)、 [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)和其他) 為非 MUI 感知的功能。 分割資源 (LN 和 mui 檔中隨附的應用程式) 必須使用下列兩個函式的其中一個來載入資源模組：

    -   如果應用程式只在 Windows Vista 和更新版本上執行，則應該使用 [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)載入資源模組。
    -   如果應用程式是在 Windows Vista 之前的版本，以及 Windows Vista 或更新版本上執行，則必須使用 [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)，這是 WINDOWS 7 SDK 中提供的特定舊版功能。

-   在 windows vista 之前版本的 Windows 作業系統中，提供的語言管理和語言回溯順序支援與 Windows Vista 和更新版本中的功能有很大的差異。 基於這個理由，允許使用者設定之語言回復的應用程式必須調整其語言管理作法：

    -   如果應用程式只在 Windows Vista 和更新版本上執行，使用 [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) 設定語言清單就已足夠。
    -   如果應用程式要在所有 Windows 版本上執行，則必須將程式碼結構化，以在舊版平臺上執行，以逐一查看使用者設定的語言清單，並探查所需的資源模組。 這可以在此步驟稍後提供的第1c 節和第2節中看到。

建立可在任何版本的 Windows 上使用當地語系化資源模組的專案：

1.  將新專案加入至 HelloMUI 方案 (使用功能表選取檔案、加入，以及使用下列設定和值的新專案) ：

    1.  專案類型： Win32 專案。
    2.  名稱： GuiStep \_ 3。
    3.  位置：接受預設值。
    4.  在 Win32 應用程式精靈中，選取預設的應用程式類型： Windows 應用程式。

2.  將這個專案設定為從 Visual Studio 中執行，並設定其執行緒模型。 此外，請將它設定為新增必要的標頭和程式庫。

    > [!Note]  
    > 本教學課程中使用的路徑假設 Windows 7 SDK 和 Microsoft NLS 下層 Api 封裝已安裝在其預設目錄中。 如果不是這種情況，請適當地修改路徑。

     

    1.  在方案總管中，以滑鼠右鍵按一下專案 GuiStep \_ 3，然後選取 [設定為啟始專案]。
    2.  再以滑鼠右鍵按一下它，然後選取 [屬性]。
    3.  在專案的 [屬性頁] 對話方塊中：

        1.  在左上方的下拉式清單中，將 [設定] 設定為 [所有設定]。
        2.  在 [設定屬性] 下展開 [C/c + +]，選取 [程式碼產生]，並設定執行時間程式庫：多執行緒的 Debug () /MTd
        3.  選取 [一般]，並新增至其他 Include 目錄：

            -   "C： \\ MICROSOFT NLS 下層 api \\ 包含"。

        4.  選取 Language 並將 wchar \_ t 視為內建類型： No (/zc： wchar \_ t-) 。
        5.  選取 Advanced 和 set 呼叫慣例： \_ stdcall (/Gz) 。
        6.  在 [設定屬性] 下展開 [連結器]，選取 [輸入]，然後新增至其他相依性

            -   "C： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ lib \\ MUILoad .lib"。
            -   "C： \\ MICROSOFT NLS 下層 api \\ Lib \\ x86 \\ Nlsdl .lib"。

3.  以下列程式碼取代 GuiStep 3 的內容 \_ ：
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  將 langs.txt 建立或複製到適當的目錄，如先前 [步驟4：全球化 "HELLO MUI"](#step-4-globalizing-hello-mui)所述。
5.  建置並執行專案。

> [!Note]  
> 如果應用程式應該在 windows Vista 之前的 Windows 版本上執行，請務必閱讀 [MICROSOFT NLS 下層 api](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) 套件隨附的檔，以瞭解如何轉散發 Nlsdl.dll。

 

## <a name="additional-considerations-for-mui"></a>MUI 的其他考慮

### <a name="support-for-console-applications"></a>主控台應用程式的支援

本教學課程中所涵蓋的技巧也可以用於主控台應用程式。 但是，與大部分的標準 GUI 控制項不同的是，Windows 命令視窗無法顯示所有語言的字元。 基於這個理由，多語系主控台應用程式需要特別注意。

使用特定篩選旗標呼叫 Api [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) 或 [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) ，會導致資源載入函式移除在命令視窗中通常不會顯示的特定語言的語言資源探查。 設定這些旗標之後，語言設定演算法只允許在 [命令] 視窗中正確顯示的語言為 [回復清單]。

如需有關使用這些 Api 建立多語系主控台應用程式的詳細資訊，請參閱 [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) 和 [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)的備註章節。

### <a name="determination-of-languages-to-support-at-run-time"></a>在 Run-Time 上判斷支援的語言

您可以採用下列其中一個設計建議，判斷您的應用程式在執行時間應該支援的語言：

-   **在安裝期間，讓終端使用者從支援的語言清單中選取慣用語言**

-   **從設定檔讀取語言清單**

    本教學課程中的部分專案包含用來剖析 langs.txt 設定檔的函式，其中包含語言清單。

    因為此函式會接受外部輸入，所以請驗證提供作為輸入的語言。 如需執行該驗證的詳細資訊，請參閱 [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) 或 [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) 函數。

-   **查詢作業系統以判斷已安裝的語言**

    這種方法可協助應用程式使用與作業系統相同的語言。 雖然這不需要使用者提示，但如果您選擇此選項，請留意作業系統語言可以隨時新增或移除，而且可以在使用者安裝應用程式之後變更。 此外，請注意，在某些情況下，作業系統會以有限的語言支援進行安裝，而如果支援作業系統不支援的語言，則應用程式會提供更多的價值。

    如需如何判斷作業系統中目前已安裝之語言的詳細資訊，請參閱 [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) 函數。

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a>Windows Vista 之前版本中的複雜字集支援

當支援特定複雜字集的應用程式在 Windows Vista 之前的 Windows 版本上執行時，該腳本中的文字可能無法在 GUI 元件中正確顯示。 例如，在本教學課程中的舊版專案中，如果處理複雜字集和缺少相關字型的問題，則不會在訊息方塊中顯示 hi 和 ta 腳本。 一般來說，這個本質的問題會以 GUI 元件的方塊呈現。

如需如何啟用複雜字集處理的詳細資訊，請參閱 [Windows 中的腳本和字型支援](https://msdn.microsoft.com/goglobal/bb688099.aspx)。

## <a name="summary"></a>總結

本教學課程全球化單一語言應用程式，並示範下列最佳做法。

-   設計應用程式以利用 Win32 資源模型。
-   使用 MUI 將資源分割成 ( mui 檔) 的附屬二進位檔。
-   請確定當地語系化程式會更新 mui 檔案中的資源，以適用于目的語言。
-   確定封裝和部署應用程式、相關聯的 mui 檔案和設定內容都已正確完成，以允許資源載入 Api 尋找當地語系化的內容。
-   為終端使用者提供調整應用程式語言設定的機制。
-   調整執行時間程式碼以利用語言設定，讓應用程式更能回應使用者的需求。

 

 
