---
title: 自訂範例 Project
description: 自訂範例 Project
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player 線上商店，自訂範例專案
- 線上商店，自訂範例專案
- 輸入2個線上商店，自訂範例專案
- Windows Media Player 線上商店、範例專案
- 線上商店、範例專案
- 類型2線上商店、範例專案
- 自訂範例專案
- 範例，請輸入2個線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdb57327904d81ac85114af0df9037d6c2c054938f16048f6ca72e711063cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902078"
---
# <a name="customizing-the-sample-project"></a>自訂範例 Project

建立您自己的線上商店時，您會想要在名為 Yourproject。的檔案中變更下列方法的實作為：

-   **CYourProject：： allowPlay**。 您可以使用此函式來套用商務規則，以允許播放受保護的內容。
-   **CYourProject：：允許 cdburn.exe**。 您可以使用此函式來套用商務規則，讓使用者可以將受保護的內容複製到 CD。
-   **CYourProject：： allowPDATransfer**。 您可以使用此函式來套用商務規則，讓使用者可以將受保護的內容傳送到可攜式裝置。
-   **CYourProject：： startBackgroundProcessing**。 使用此函式可起始您所需的任何背景處理工作。 例如，您可以使用這種方式來檢查過期的授權。
-   **CYourProject：:D eviceavailable**。 使用此函式可起始與連線裝置相關的任何工作。
-   **CYourProject：:P repareforsync**。 使用此函式可在將數位媒體同步至裝置之前，執行必要的工作。
-   **CYourProject：： serviceEvent**。 您可以使用此函式來開始和結束您要在線上商店為使用中時執行的工作。
-   **CYourProject：： stopBackgroundProcessing**。 使用此函式可在 Windows Media Player 呼叫 **CYourProject：： startBackgroundProcessing** 時，停止您啟動的任何背景處理工作。

## <a name="working-with-media-and-playlist-objects"></a>使用媒體和播放清單物件

**AllowPlay** 方法會提供 **IWMPMedia** 介面的指標作為參數。 此介面是表示媒體物件的 Windows Media Player 介面。 藉由呼叫此介面上的方法，您可以使用個別媒體專案的屬性和屬性。

**AllowCDBurn** 和 **AllowPDATransfer** 方法提供 **IWMPPlaylist** 介面的指標作為參數。 此介面是代表播放清單物件的 Windows Media Player 介面。 藉由呼叫此介面上的方法，您可以使用播放清單的屬性和屬性、將專案新增至播放清單，或從播放清單中移除專案。

若要瞭解如何以程式設計方式從播放清單中移除專案，請參閱 **CAllowBaseDialog <T> ：： OnRemoveMediaFromPlaylist** 的實。 若要深入瞭解如何使用媒體和播放清單物件，請參閱 [指令碼語言的播放程式物件模型](player-object-model-for-scripting-languages.md)。

## <a name="code-that-can-be-removed"></a>可以移除的程式碼

您可能會想要移除開啟對話方塊的程式碼，因為不太可能會想要讓使用者決定哪些媒體專案可以播放或複製。 從 Yourproject。中移除下列程式碼：

-   **CAllowBaseDialog** 的宣告。
-   **CAllowBurnDialog** 的宣告。
-   **CAllowTransferDialog** 的宣告。

從 Yourproject。 .cpp 移除下列程式碼：

-   **CAllowBaseDialog <T> ：： OnInitDialog** 的實作為。
-   **CAllowBaseDialog <T> ：： OnRemoveMediaFromPlaylist** 的實作為。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Type 2 線上商店的外掛程式**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




