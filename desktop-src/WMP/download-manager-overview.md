---
title: 下載管理員總覽
description: 下載管理員總覽
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player 線上商店，即時下載
- 線上商店，即時下載
- 輸入2個線上商店，即時下載
- Windows Media Player 線上商店，背景下載
- 線上商店，背景下載
- 輸入2個線上商店，背景下載
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
- 即時下載
- 背景下載
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021993"
---
# <a name="download-manager-overview"></a>下載管理員總覽

Microsoft Windows Media Player 提供包含託管瀏覽器視窗的線上商店工作窗格。 透過線上商店，使用者可以在網際網路上與線上商店網頁互動。

Windows Media Player 下載管理員提供的物件模型，可讓您用來處理與從 Microsoft Internet Information Services (IIS) 使用超文字傳輸通訊協定 (HTTP) ，將內容下載到使用者電腦相關聯的工作。 使用下載管理員，您可以：

-   以集合的形式同時管理多個下載。
-   指定檔案的 URL，並使用 HTTP 來開始下載。
-   查詢下載狀態和進度。
-   暫停、繼續或取消下載。
-   指定下載是否會在背景或即時進行。  (背景下載僅適用于 Microsoft Windows XP 作業系統。 ) 查看 [有關背景和即時下載的資訊](#about-background-and-real-time-downloading)。
-   指定內容在文件庫中的顯示方式。 請參閱 [關於程式庫整合](#about-library-integration)。

下載管理員是從裝載的網頁中的腳本下載內容的解決方案。 若要使用 c + + 程式碼下載內容，請使用 Windows XP 背景智慧型傳送服務 (位) 。 如需詳細資訊，請參閱 [BITS](bits.md)。

## <a name="about-background-and-real-time-downloading"></a>關於背景和即時下載

下載管理員提供兩種類型的下載：背景和即時。 您所使用的類型是由您負責，而且也可以讓使用者選取下載類型。 如果您選擇允許使用者選取下載類型，請務必說明這兩種可用類型之間的差異。

即時下載會一次完成。 當使用者開始下載檔案時，會以單一的連續串流將整個檔案傳送至使用者的電腦。 使用者無法暫停或以其他方式中斷下載。 如果使用者選擇在下載完成之前關閉 Windows Media Player，他或她會遺失任何未完成的檔案，而且必須從一開始就下載以取得內容。

即時下載的主要優點是，它可讓使用者更快取得內容，而不是背景下載。 Windows XP 的使用者可以使用即時下載，但這是在 Windows XP 之前的 Windows 作業系統版本上唯一可用的下載類型。

背景下載會以分次方式進行。 當使用者啟動背景下載時，系統會在有可用的處理器時間時，將部分的檔案傳送至使用者的電腦。 您可以暫停並繼續背景下載。 如果使用者選擇在背景下載完成之前關閉 Windows Media Player，則會儲存任何未完成檔案的條件，而且即使在重新開機電腦之後，下載也可以繼續在背景中繼續進行。

背景下載可能需要較長的時間才能下載，因為只有在處理器未執行其他工作時，才會進行下載程式。

只有在使用 Windows XP 時，才可使用背景下載。

## <a name="about-library-integration"></a>關於程式庫整合

Windows Media Player 可以自動組織文件庫中的線上存放區內容。 若要啟用這項程式，您必須為每個數位媒體檔案指定 **WM/ContentDistributor** 屬性的值。 當您將數位媒體檔案新增至程式庫時（當使用下載管理員時自動發生），檔案會自動列在 [已 **購買的音樂** ] 或 [已 **購買** 的影片] 節點中。 例如，如果 **WM/ContentDistributor** 的值是 "Proseware"，而數位媒體檔案包含音樂，則內容會顯示在程式庫中的下列位置：

所有音樂/購買的音樂/Proseware

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**下載管理員**](download-manager.md)
</dt> <dt>

[**DownloadCollection.startDownload**](downloadcollection-startdownload.md)
</dt> </dl>

 

 




