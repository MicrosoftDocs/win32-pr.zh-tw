---
title: MCI 函數宏和訊息
description: MCI 函數宏和訊息
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- MCI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade9ac3ea5c2a3c74f94bab899305cdae7ec51c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682281"
---
# <a name="mci-functions-macros-and-messages"></a>MCI 函數宏和訊息

大部分的 MCI 應用程式會使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 和 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函數數十次。 MCI 提供一些其他有用的功能，讓您的應用程式不會經常使用。

大部分 MCI 命令所需的裝置識別碼，通常是在 [**open**](open.md) ([**mci \_ open**](mci-open.md)) 命令的呼叫中取出。 如果您需要裝置識別碼，但不想要開啟裝置，例如，如果您想要查詢裝置的功能再採取任何其他動作，您可以呼叫 [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) 函式。

[**MciGetCreatorTask**](/previous-versions//dd757155(v=vs.85))函式可讓您的應用程式使用裝置識別碼，來取得建立該識別碼之工作的控制碼。

您可以使用 [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) 和 [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) 函式來指派和取出與 "wait" (MCI wait) 旗標相關聯的回呼函式位址 \_ 。

[**MciGetErrorString**](/previous-versions//dd757158(v=vs.85))函式會捕獲描述 MCI 錯誤值的字串。 MCI 傳回的每個字串（不論是資料還是錯誤描述）最多為128個字元。 小於128個字元的對話方塊欄位將截斷 MCI 傳回的較長字串。 如需這些字串的詳細資訊，請參閱 [MCIERR 傳回值](mcierr-return-values.md)。

MCI 宏是您可用來建立和分解指定時間格式之值的工具。 這些時間格式用於許多 MCI 命令中。 宏所處理的格式為小時/分鐘/秒 (HMS) 、分鐘/秒/畫面格 (MSF) ，以及追蹤/分/秒/畫面格 (TMSF) 。 下表列出宏及其描述。



| 巨集                                        | Description                                        |
|----------------------------------------------|----------------------------------------------------|
| [**MCI \_ HMS \_ HOUR**](mci-hms-hour.md)       | 從 HMS 值抓取小時元件。   |
| [**MCI \_ HMS \_ 分鐘**](mci-hms-minute.md)   | 從 HMS 值抓取分鐘元件。 |
| [**MCI \_ HMS \_ SECOND**](mci-hms-second.md)   | 從 HMS 值抓取秒鐘元件。 |
| [**MCI \_ 製作 \_ HMS**](mci-make-hms.md)       | 建立 HMS 值。                              |
| [**MCI \_ 讓 \_ MSF**](mci-make-msf.md)       | 建立 MSF 值。                              |
| [**MCI \_ 製作 \_ TMSF**](mci-make-tmsf.md)     | 建立 TMSF 值。                              |
| [**MCI \_ MSF \_ 框架**](/previous-versions//dd743438(v=vs.85))     | 從 MSF 值抓取畫面格元件。  |
| [**MCI \_ MSF \_ 分鐘**](mci-msf-minute.md)   | 從 MSF 值抓取分鐘元件。 |
| [**MCI \_ MSF \_ SECOND**](mci-msf-second.md)   | 從 MSF 值抓取秒鐘元件。 |
| [**MCI \_ TMSF \_ 框架**](mci-tmsf-frame.md)   | 從 TMSF 值抓取畫面格元件。  |
| [**MCI \_ TMSF \_ 分鐘**](mci-tmsf-minute.md) | 從 TMSF 值抓取分鐘元件。 |
| [**MCI \_ TMSF \_ SECOND**](mci-tmsf-second.md) | 從 TMSF 值抓取秒鐘元件。 |
| [**MCI \_ TMSF \_ TRACK**](mci-tmsf-track.md)   | 從 TMSF 值抓取追蹤元件。  |



 

MCI 也提供兩個訊息： [**MM \_ MCINOTIFY**](mm-mcinotify.md) 和 [**mm \_ MCISIGNAL**](mm-mcisignal.md)。 \_只要命令指定「通知」 (mci 通知) 旗標，MM MCINOTIFY 訊息就會通知應用程式是否有 mci 命令的結果 \_ 。 MM \_ MCISIGNAL 訊息是數位視訊裝置的特定訊息; 當達到指定的位置時，就會通知應用程式。

 

 