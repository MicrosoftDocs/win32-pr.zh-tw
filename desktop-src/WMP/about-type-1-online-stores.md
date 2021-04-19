---
title: 關於類型1線上商店
description: 關於類型1線上商店
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player 線上商店，請輸入1個線上商店
- 線上商店，請輸入1個線上商店
- 輸入1個線上商店，關於
- Windows Media Player，請輸入1個線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106968083"
---
# <a name="about-type-1-online-stores"></a>關於類型1線上商店

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

Microsoft Windows Media Player 11 支援兩種線上商店：類型1和類型2。 類型1存放區比類型2存放區更深層整合至 Windows Media Player。 Type 1 線上商店提供可下載的音樂類別目錄，讓 Windows Media Player 可以將商店的內容提供給使用者，就像內容是在使用者的本機媒體文件庫中一樣。

類型1線上商店必須提供可實 [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) 介面的外掛程式。 當使用者流覽 Windows Media Player 使用者介面時，播放程式會呼叫外掛程式，讓線上商店可以藉由提供顯示在播放程式中的網頁來增強使用者的體驗。

類型1線上商店的功能，可與類型2存放區區別，包括下列各項：

-   **便於使用。** 使用者可以使用他們目前用來管理個人文件庫的相同、熟悉的 Windows Media Player 使用者介面，從線上商店瀏覽目錄音樂。 在任何特定時間，使用者都只能在流覽功能中查看單一線上商店目錄。
-   **方便。** 使用者無須從流覽功能切換到 Windows Media Player 使用者介面的另一個部分，就可以取樣或購買音樂。
-   **豐富的功能。** 因為線上商店目錄的儲存方式類似于使用者的程式庫，所以許多 Windows Media Player 程式庫功能都可以套用至目錄。 例如，使用者可以使用流覽功能的單字滾輪來篩選線上商店目錄。

在線上商店提供者中，提供類型1存放區的優點，而不是類型2存放區的優點包括下列各項：

-   Windows Media Player 程式庫樹狀結構中的高度可見自訂節點。
-   針對音樂購買所設計的系統。
-   改進玩家流程的連接。
-   更好、更容易使用的下載管理員。
-   可以在播放 (中的各種功能之間進行流覽，包括) 開啟特定的程式庫樹狀節點。
-   訂用帳戶內容的授權到期通知。
-   使用連線的便攜音樂播放機的通知。

下列各節提供類型1線上商店的總覽資訊。



| 區段                                                                                              | 描述                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [音樂類別目錄](music-catalog.md)                                                                   | 描述線上商店所提供的音樂目錄。 說明 Microsoft 所提供的目錄編譯器。                                                                     |
| [內容容器](content-containers.md)                                                         | 描述 ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)) 的內容容器介面，此介面可用來代表要購買或下載的媒體專案集合。 |
| [程式庫整合](library-integration.md)                                                       | 描述線上商店的音樂目錄如何整合到播放程式的程式庫視圖中。                                                                                        |
| [探索頁面](discovery-pages.md)                                                               | 描述線上商店所提供 Windows Media Player 與網頁之間的互動。                                                                                   |
| [快顯功能表](context-menus.md)                                                                   | 描述當使用者導覽播放程式的使用者介面時，線上商店如何提供內容功能表。                                                                         |
| [音訊串流](audio-streams.md)                                                                   | 描述線上商店如何以串流處理音訊內容的 URL 來提供 Windows Media Player。                                                                              |
| [類型1線上商店的 ServiceInfo 檔](serviceinfo-document-for-a-type-1-online-store.md) | 描述類型1線上商店所提供的 ServiceInfo XML 檔。                                                                                                           |
| [輸入1線上商店外掛程式](type-1-online-store-plug-in.md)                                       | 描述類型1線上商店必須提供的外掛程式。                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**輸入1個線上商店**](type-1-online-stores.md)
</dt> </dl>

 

 




