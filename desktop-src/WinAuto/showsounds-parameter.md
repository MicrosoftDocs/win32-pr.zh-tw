---
title: '顯示聲音 (和音訊描述旗標) '
description: 本主題包含參數的相關資訊，指出當應用程式使用音效傳達重要資訊時，是否應提供視覺效果警示或提示。
ms.assetid: 7b316892-76ff-48b3-bf67-34dea2e63936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf32dfacdf1dc0b8ed3bc51c986ae572e43300263565254ad6b3a48a981beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734318"
---
# <a name="show-sounds-and-audio-description-flag"></a>顯示聲音 (和音訊描述旗標) 

本主題包含參數的相關資訊，指出當應用程式使用音效傳達重要資訊時，是否應提供視覺效果警示或提示。 它也會提供旗標的相關資訊，指出應用程式是否應該提供視覺元素的音訊描述。

## <a name="show-sounds-parameter"></a>顯示音效參數

[顯示音效] 參數表示使用者是否希望應用程式以視覺化形式呈現所有重要資訊。

使用者可以使用主控台中的輕鬆存取中心來控制顯示音效參數的設定，或使用其他應用程式來自訂環境。 應用程式會使用 **spi \_ GETSHOWSOUNDS** 和 **spi \_ SETSHOWSOUNDS** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來取得和設定顯示音效參數。 或者，應用程式可以使用 **SM \_** 音效旗標搭配 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函式來判斷顯示音效參數的狀態。

只有通常只會以音效呈現重要資訊的應用程式，才需要決定顯示音效參數的狀態。 如果應用程式使用音效，請使用下列其中一種方式來提供顯示音效支援：

-   傳達對應用程式作業而言很重要的資訊。
-   以視覺化方式向使用者顯示重要資訊。 如果是這種情況，即使資訊以視覺化方式呈現，音效還有其他功能可以吸引使用者的注意力。

適當的視覺效果意見反應表單可讓軟體的功能更適合無法單獨依賴音效的使用者。 視覺效果意見反應的設計是應用程式專屬的，而且取決於將呈現給使用者的資訊。 例如，若要在新的電子郵件送達時吸引使用者的注意，應用程式可能會將視窗閃爍，甚至是在整個畫面上閃爍。 如果應用程式通常會讓音效指出使用者嘗試執行不合法的作業，它也可能會在其狀態行上顯示適當的訊息，或使用 [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) 函式來顯示特定的錯誤訊息。 如果應用程式通常是設計來播放帶有意義的音訊剪輯，例如數位化語音，則也可能會顯示具有相同文字的標題視窗。

已顯示可重複使用的已聽見和視覺效果警示，以提高軟體應用程式的可用性。 顯示音效參數是視覺效果的要求，但它的使用不會限制應用程式以視覺化方式呈現資訊。 無論使用者是否也想要有聲音的意見反應，使用者都應該能夠要求視覺效果的意見反應。

## <a name="audio-description-flag"></a>音訊描述旗標

應用程式會使用 **spi \_ GETAUDIODESCRIPTION** 和 **spi \_ SETAUDIODESCRIPTION** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來啟用或停用音訊描述。 雖然視力受損的使用者可以聽到影片內容中的音訊，但影片中有許多動作沒有對應的音訊。 影片中所發生內容的特定音訊描述可協助這些使用者更瞭解內容。 這個旗標可讓您以提供的語言來啟用或停用音訊描述。

 

 