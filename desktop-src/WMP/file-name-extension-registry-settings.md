---
title: 副檔名登錄設定
description: 副檔名登錄設定
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player，登錄
- Windows Media Player、副檔名
- 登錄、副檔名
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674835"
---
# <a name="file-name-extension-registry-settings"></a>副檔名登錄設定

如果您的數位媒體檔案有自訂格式，您可以在使用者電腦的登錄中放入專案，以提供有關自訂格式的資訊 Windows Media Player。 Windows Media Player 會檢查您的登錄專案，以判斷它應該如何處理您的檔案。 下列清單顯示您可以藉由建立與自訂媒體檔案格式相關的登錄專案來執行的一些動作。

-   授與播放機播放、複製或轉碼檔案的許可權。
-   指定播放機用來播放檔案的基礎技術。
-   指定播放程式在文件庫視圖中顯示檔案的位置。
-   指定播放機應用來將您的檔案轉換成標準格式的外掛程式。
-   指定媒體傳輸通訊協定 (MTP) 格式的程式碼，讓播放程式可以用來判斷特定的可攜式裝置是否支援您的檔案格式。

您提供的大部分專案都會在與自訂副檔名相關聯的子機碼下。 您可以在 HKEY \_ 本機 \_ 電腦子樹和 [HKEY \_ 目前 \_ 使用者] 子樹中建立該子機碼。 Windows Media Player 會先在 HKEY \_ 本機 \_ 電腦子樹中尋找。 如果它在該處找不到它所需的內容，則會在 [HKEY \_ 目前 \_ 使用者] 子樹中尋找。 請注意，嘗試寫入使用者電腦上登錄的任何程式碼， \_ \_ 只有在目前的使用者具有系統管理許可權時，才可以寫入至 HKEY 本機電腦子樹。

若要將自訂檔案格式的相關資訊寫入 HKEY \_ 本機 \_ 電腦子樹，請建立下列子機碼。

**HKEY \_本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 多媒體 \\ WMPlayer \\ 延伸 \\** 模組 *customExtension*

其中 *customExtension* 是副檔名，包括點 (. ) 分隔符號。 例如，如果您自訂檔案格式的副檔名是 .xyz，請建立下列子機碼。

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 多媒體 \\ WMPlayer \\ 擴充功能 \\ 。 xyz**

若要將自訂檔案格式的相關資訊寫入 HKEY \_ CURRENT \_ USER 子樹，請建立下列子機碼。

**HKEY \_目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\** *customExtension*

您可以在 *customExtension* 子機碼中寫入下列一或多個專案。

-   **權限**
-   **執行階段**
-   **FormatCode**

若要指定您自訂媒體檔案格式的轉換外掛程式，請在 *customExtension* 子機碼中建立 **ConvertPluginCLSID** 子機碼。

若要指定 Windows Media Player 應該在其程式庫視圖中顯示檔案的位置，請在下列子機碼中寫入代表您自訂檔案格式的專案。

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

下列主題描述的登錄子機碼和專案可提供 Windows Media Player 有關自訂媒體檔案格式的資訊。

-   [許可權登錄專案](permissions-registry-entry.md)
-   [執行時間登錄專案](runtime-registry-entry.md)
-   [FormatCode 登錄專案](formatcode-registry-entry.md)
-   [程式庫分類登錄專案](library-classification-registry-entries.md)
-   [ConvertPluginCLSID 子機碼](convertpluginclsid-subkey.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**登錄設定**](registry-settings.md)
</dt> <dt>

[**Windows Media Player 轉換外掛程式**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




