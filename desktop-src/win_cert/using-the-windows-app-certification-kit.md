---
title: 使用 Windows 應用程式認證套件
description: 為了讓您的傳統型應用程式在提交認證並在 Windows 存放區中列出之前，先在電腦上進行認證、驗證及測試，是很好的機會。
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8692e87f8bd152b730129c0d8684bc7ec2ca91964ecd6c25e98eb3db3e0fce44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118708746"
---
# <a name="using-the-windows-app-certification-kit"></a>使用 Windows 應用程式認證套件

為了讓您的傳統型應用程式在提交認證並在 Windows 存放區中列出之前，先在電腦上進行認證、驗證及測試，是很好的機會。 若要認證您的應用程式，您必須安裝並執行[Windows 應用程式認證套件](/previous-versions//mt637081(v=vs.85))。 如需套件內特定測試的詳細資訊，請參閱[Windows 應用程式認證套件測試](windows-app-certification-kit-tests.md)。

如需深入瞭解認證程式，以及此工具的使用方式，請參閱 [認證您的桌面應用程式](windows-certification-portal.md)。

目前版本的 Windows ACK 有14種語言版本， (捷克文、英文、法文、德文、義大利文、日文、韓文、波蘭文、葡萄牙文 (巴西) 、俄文、簡體中文、西班牙文、繁體中文和土耳其文) 。

## <a name="prerequisites"></a>必要條件

安裝 Windows ACK 之前，您必須先安裝並執行作業系統。

1. 安裝並執行您要開發應用程式的作業系統。

-   如果您要開發 Windows 7 的應用程式，您可以安裝並執行 Windows 7、Windows 8 或 Windows 8.1。
-   如果您要開發 Windows 8 傳統型應用程式或 Windows 8 桌面裝置應用程式，您可以安裝並執行 Windows 8 或 Windows 8.1。
-   如果您要開發 Windows 8.1 desktop 應用程式或 Windows 8 桌面裝置應用程式，請安裝 Windows 8.1。

2. 安裝[Windows 應用程式認證套件 3.3](/previous-versions//mt637081(v=vs.85))，其包含在適用于 Windows 8.1 的 Windows 軟體開發套件 (SDK) 中。

**注意：** 當您在電腦上安裝 Windows 應用程式認證套件3.3 或更高版本時，會取代任何先前安裝的套件版本。

## <a name="instructions-to-run-windows-app-certification-kit-33"></a>執行 Windows 應用程式認證套件3.3 的指示

**以互動方式使用 Windows 應用程式認證套件3.3 來驗證您的桌面應用程式**

1.  在 [開始] 功能表中，搜尋 Windows 應用程式憑證套件。
2.  在 [Windows 應用程式認證套件中，按一下您要執行的測試驗證類別目錄。 如果您要驗證傳統型應用程式，請選取 [ **驗證桌面應用程式**]。
3.  在下一個畫面中，流覽至您要驗證的桌面應用程式的安裝檔案。
    -   **注意：** 如有必要，您可以使用 [命令列步驟](#commandlinesteps) 來包含選項或安裝參數。
4.  指出應用程式的使用類型，然後按 **[下一步]**。 Windows 應用程式認證套件開始使用安裝程式檔案來安裝傳統型應用程式，以便驗證安裝。
5.  如果系統要求您重新開機系統以完成安裝程式，請選擇 [ **否**]。 如果您的應用程式需要安裝數個元件或外部相依性，請仔細選取應用程式的名稱。 如果您的應用程式列在 Windows 存放區中，則您在此處選擇的名稱就是您的應用程式所提供的名稱。 驗證完成時，請以您在步驟6中為應用程式提供的名稱來儲存報表。 Windows 應用程式認證套件會建立 XML 報表檔案並加以儲存。
6.  流覽至您儲存報表的資料夾，然後開啟該資料夾以查看測試的結果。 如果您的測試失敗，且您有資格獲得棄權，您需要提交的資訊會列在此處。 您必須針對每個可能的棄權要求提交詳細的描述。

**從命令列使用 Windows 應用程式認證套件3.3 來驗證您的 Windows desktop 應用程式**

1.  流覽至您儲存報表的資料夾，然後開啟該資料夾以查看測試的結果。 此處會列出可能具有棄權要求的失敗測試。 您必須針對每個可能的棄權要求提交詳細的描述。
2.  從包含 Windows 應用程式認證套件的資料夾中，依下列順序輸入下列命令：

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    其中： `[report file name]` 是套件將建立以包含測試報表之 XML 檔案的完整檔案名。

3.  測試完成之後，請開啟名為 [報表檔案名] 的報表檔案 \[ \] ，並查看測試結果。

    **注意：** 如需 Windows 應用程式認證套件命令列的詳細資訊，請輸入命令 appcert.exe/？

    Windows 應用程式認證套件必須在作用中使用者會話的內容中執行，但是您無法在非互動式會話中啟動應用程式。 套件處理權杖以使用或不使用系統管理許可權來執行測試的方式，也取決於此使用者會話內容。 您可以從服務執行套件，但是服務必須能夠在使用中的使用者會話中產生套件進程。

**使用 Windows 應用程式認證套件來驗證您的 Windows 7 應用程式**

-   Windows 應用程式認證套件取代 Windows 軟體標誌套件。 如果您想要應用程式的 Windows 7 標誌，請使用 Windows 應用程式認證套件進行驗證測試和報告。 套件可以偵測正在執行的作業系統，並自動啟動 Windows 7 應用程式。 遵循相同的程式來驗證 Windows 7 應用程式。

**提交認證**

-   驗證您的應用程式之後，您就可以 [透過入口網站提交](https://www.microsoft.com/?ref=go)程式來提交認證。

## <a name="reference-documents"></a>參考檔

-   [Windows 桌面應用程式的認證需求](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [應用程式認證技術白皮書](https://www.microsoft.com/download/details.aspx?id=27414)
-   [Windows桌面應用程式的商店上線](/previous-versions//dn322034(v=vs.85))
-   [Windows 7 桌面應用程式認證需求](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a>Windows 應用程式認證套件測試

我們已變更套件，讓 Windows 的[ACK 測試](windows-app-certification-kit-tests.md)更容易使用。 套件現在具有：

-   全新的簡化使用者介面
-   已改善多使用者測試，因此您不再需要設定第二個使用者帳戶

 

 