---
title: Windows Media Player SDK) 註冊應用程式相依性 (
description: 瞭解如何向 Windows Media Player SDK 所提供之 api 的執行時間元件註冊您的應用程式。
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player，應用程式相依性登錄設定
- Windows Media Player，相依性登錄設定
- Windows Media Player，登錄
- 登錄，應用程式相依性設定
- 登錄，相依性設定
- 登錄，Windows Media Player 的設定
- 相依性登錄設定
- 應用程式相依性登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa210debc4045326eb3bbae1e4fc137db5fb5a5dec6b89e493aedd54f110f82f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861548"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a>Windows Media Player SDK) 註冊應用程式相依性 (

使用 Windows Media Player SDK 或 Windows 媒體格式 SDK 所提供之 api 的應用程式，會根據這些技術的執行時間元件而定。 您可以在應用程式設定中註冊應用程式，使其相依于這些元件。

當您註冊應用程式時，您可以選擇兩個相依性層級的其中一個：封鎖或相依。 當一個或多個應用程式在其中一個執行時間元件的封鎖相依性註冊時，元件將會遭到封鎖而無法回復為先前的版本。 未註冊為封鎖的相依應用程式不會封鎖復原。 相反地，在執行復原之前，使用者會看到一則訊息，指出應用程式相依于元件。

若要註冊您的應用程式，您必須在登錄中設定用來識別應用程式的值。 要設定的登錄值取決於您的應用程式相依的元件。 您也可以為每個相依性設定兩個額外的值，以提供應用程式的額外資訊。

下列登錄值會用來註冊 Windows Media Player SDK 執行時間的相依性：

-   HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ *REF \_ TYPE* \\ App，"*app*"，"*應用程式 \_ 字串*"
-   HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ *REF \_ TYPE* \\ 描述元，"*APP*"，"*REF \_ 描述* 元"
-   HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ *REF \_ TYPE* \\ Version，"*APP*"，"*WMP \_ version*"

下列登錄值會用來註冊 Windows 媒體格式 SDK 執行時間的相依性：

-   HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *REF \_ TYPE* \\ App，"*app*"，"*應用程式 \_ 字串*"
-   HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *REF \_ TYPE* \\ 描述元，"*APP*"，"*REF \_ 描述* 元"
-   HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *REF \_ TYPE* \\ Version，"*APP*"，"*WMF \_ Version*"

下列變數會用於上述的登錄值：

*REF \_ 類型*

取代為封鎖相依性的 BlockingRefCounts，或針對非封鎖相依性使用 DependentRefCounts 取代。

*APP*

應用程式的名稱或簡短描述項。 此字串不會用於使用者顯示的訊息。 此值是與每個執行時間元件相關聯的三個登錄值所使用的識別碼。

*應用程式 \_ 字串*

應用程式的描述項。 這個字串可用於顯示給使用者的訊息。

*參考 \_ 描述元*

應用程式如何使用元件的描述。 此值最多可包含256個字元。

*WMP \_ 版本*

應用程式所需的 Windows Media Player 版本。 如果未指定任何版本，則會假設預設值為9.0.0.0。

*WMF \_ 版本*

應用程式所需的 Windows 媒體格式 SDK 版本。

下列三個範例登錄值示範如何設定應用程式的值：

-   HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ App，"SouthridgeVideo"，"Southridge 影片播放程式"
-   HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ 描述項 "SouthridgeVideo"，"Southridge Video Player 使用 Windows 媒體格式 SDK 來播放影片檔案。"
-   HKEY \_ 類別 \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Version，"SouthridgeVideo"，"9.0.0.2600"

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**登錄設定**](registry-settings.md)
</dt> </dl>

 

 




