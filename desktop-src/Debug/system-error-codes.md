---
description: 提供 Winerror.h .h 標頭檔中所定義之系統錯誤碼的連結，適用于開發人員。
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: 系統錯誤碼
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 4c762b2098531ecb19ad84522f8c9c8272c004397bbc4b32f15a6f6e157c4332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691728"
---
# <a name="system-error-codes"></a>系統錯誤碼

本節適用于正在進行系統錯誤的偵錯工具。 如果您在搜尋其他錯誤時到達此頁面，以下是一些可能有説明的連結：

* [Windows Update 錯誤](https://support.microsoft.com/help/10164/fix-windows-update-errors)-協助解決 Windows Update 的問題。
* [Windows 啟用錯誤](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors)-協助驗證您的 Windows 複本。
* 針對[藍色螢幕錯誤進行疑難排解](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors)-協助找出造成停止錯誤的原因。
* [Microsoft 支援服務](https://support.microsoft.com) -支援 Microsoft 產品。

## <a name="more-ways-to-find-an-error-code"></a>尋找錯誤碼的更多方式

我們已列出本節中的系統錯誤碼，並依編號進行組織。 如果您需要更多協助追蹤特定的錯誤，以下是一些建議：

* 使用 [Microsoft Error Lookup Tool](system-error-code-lookup-tool.md)。
*  安裝 Windows 的偵錯工具、載入記憶體傾印檔案，然後執行 **\! err \<code>** 命令。
* 搜尋 Microsoft 通訊協定網站中的原始文字或錯誤碼。 如需詳細資訊，請參閱[[ERREF]： Windows 錯誤碼](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90)。

## <a name="third-party-error-codes"></a>協力廠商錯誤碼

其他錯誤碼可能是由協力廠商服務或應用程式所產生 (例如， **錯誤碼：-118** 可能會顯示于串流 [遊戲服務](https://support.steampowered.com/kb_cat.php?id=59)) ，而在這些情況下，您會與協力廠商的支援線聯繫。

## <a name="system-error-codes"></a>系統錯誤碼

系統錯誤碼很廣泛：每一個都可能發生在系統中數百個位置的其中一個位置。 因此，這些程式碼的描述不能很明確。 使用這些程式碼需要進行某種程度的調查和分析。 您必須注意發生這些錯誤的程式設計和執行時間內容。 

因為這些程式碼定義于 Winerror.h 中供任何人使用，有時候程式碼會由非系統軟體傳回。 有時候，程式碼是由堆疊中的函式深度所傳回，而且會從處理錯誤的程式碼中移除。

下列主題提供系統錯誤碼的清單。 這些值定義于 Winerror.h .h 標頭檔中。

-   [系統錯誤碼 (0-499)  (0x0-0x1f3) ](system-error-codes--0-499-.md)
-   [系統錯誤碼 (500-999)  (0x1f4-0x3e7) ](system-error-codes--500-999-.md)
-   [系統錯誤碼 (1000-1299)  (0x3e8-0x513) ](system-error-codes--1000-1299-.md)
-   [系統錯誤碼 (1300-1699)  (0x514-0x6a3) ](system-error-codes--1300-1699-.md)
-   [系統錯誤碼 (1700-3999)  (0x6a4-0xf9f) ](system-error-codes--1700-3999-.md)
-   [系統錯誤碼 (4000-5999)  (0xfa0-0x176f) ](system-error-codes--4000-5999-.md)
-   [系統錯誤碼 (6000-8199)  (0x1770-0x2007) ](system-error-codes--6000-8199-.md)
-   [系統錯誤碼 (8200-8999)  (0x2008-0x2327) ](system-error-codes--8200-8999-.md)
-   [系統錯誤碼 (9000-11999)  (0x2328-0x2edf) ](system-error-codes--9000-11999-.md)
-   [系統錯誤碼 (12000-15999)  (0x2ee0-0x3e7f) ](system-error-codes--12000-15999-.md)
