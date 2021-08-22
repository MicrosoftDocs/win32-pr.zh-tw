---
title: 自動播放
description: 自動播放
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- MCIWndCreate 宏
- MCIWndPlay 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1c05041bade08f47505a2cf1207739777c5af825ea9f5f300b343b87efe3c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691968"
---
# <a name="automating-playback"></a>自動播放

您可以使用 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 和 [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) 宏，以及 [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) 或 [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) 宏，將應用程式中的播放自動化。 若要自動播放，請 \_ \_ 在 **MCIWndCreate**_dwStyle_ 參數中指定 MCIWNDF NOPLAYBAR 和 MCIWNDF NOTIFYMODE 樣式。 指定 MCIWNDF \_ NOPLAYBAR 樣式來隱藏工具列，以及使用 MCIWNDF \_ NOTIFYMODE 樣式，在裝置停止播放時發出適當的通知訊息。

您可以使用 **MCIWndPlay** 來播放在 **MCIWndCreate** 中指定的裝置或檔案。 MCIWndPlay 宏會開始播放其目前播放位置的內容，並繼續結束。

您可以使用 [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) 或 [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) 宏來摧毀或關閉 MCIWnd 視窗。 **MCIWndDestroy** 宏會關閉裝置或檔案，並藉由使其控制碼失效來終結 MCIWnd 視窗。 如果您的應用程式可以重複使用 MCIWnd 視窗，請使用 **MCIWndClose** 來關閉裝置，而不會終結視窗。

您的應用程式可以偵測到裝置何時停止播放，並自動關閉視窗。 若要這樣做，請 \_ 為 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)的 *dwStyle* 參數指定 MCIWNDF NOTIFYMODE 樣式。 這會導致裝置在每次變更模式時傳送 [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) 訊息。 您的應用程式可以陷阱此訊息，以判斷裝置是否已停止播放。 當裝置停止播放時，應用程式會關閉視窗。

 

 




