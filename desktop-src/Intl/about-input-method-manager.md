---
description: 使用 IME 感知應用程式中的 IMM 功能，可讓使用者不需要記住所有可能的字元值。
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: 關於輸入方法管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987229"
---
# <a name="about-input-method-manager"></a>關於輸入方法管理員

使用 IME 感知應用程式中的 IMM 功能，可讓使用者不需要記住所有可能的字元值。 相反地，它會允許 IME 監視使用者的按鍵，並預期使用者可能想要的字元，並提供可供選擇的候選字元清單。

> [!Note]  
> 在與文字服務通訊的應用程式所使用的 [文字服務架構](../tsf/text-services-framework.md)中，IMM 會執行類似的作業。

 

根據預設，IMM 會提供 IME 視窗，使用者可透過此視窗輸入按鍵和流覽並選取候選項目。 應用程式可以使用 IMM 函式和訊息來建立和管理自己的 IME 視窗，並在使用 IME 的轉換功能時提供自訂介面。

只有在東亞 (中文、日文、韓文) 當地語系化的 Windows 作業系統上，才會啟用 IMM。 在這些系統中，應用程式會使用 SM DBCSENABLED 呼叫 [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) ， \_ 以判斷是否已啟用 IMM。

**Windows 2000：** 所有當地語系化的語言版本都提供完整功能的 IMM 支援。 不過，只有在安裝了亞洲語言套件時，才會啟用 IMM。 IME 感知的應用程式可以使用 SM IMMENABLED 呼叫 [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \_ ，以判斷是否已啟用 IMM。

本主題包含下列各節。

-   [候選清單](candidate-lists.md)
-   [組合字元串](composition-string.md)
-   [HexToUnicode IME](hextounicode-ime.md)
-   [快速鍵](hot-keys.md)
-   [輸入法訊息](ime-messages.md)
-   [IME 視窗類別](ime-window-class.md)
-   [輸入內容](input-context.md)
-   [狀態、撰寫和候選視窗](status--composition--and-candidates-windows.md)

 

 
