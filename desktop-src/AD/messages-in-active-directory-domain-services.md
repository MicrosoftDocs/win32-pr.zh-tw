---
title: Active Directory Domain Services 中的訊息
description: Active Directory Domain Services 中的訊息可在 Windows 2000 和 Windows NT 4.0 搭配 Service Pack 6a (SP6a) 和更新版本的 DSClient 中運作。
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory 訊息廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f5a9a5e92048f64cc1b49ea67cae05443eda685d588df0c78bb3f48cf0dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025916"
---
# <a name="messages-in-active-directory-domain-services"></a>Active Directory Domain Services 中的訊息

Active Directory Domain Services 中的訊息可在 Windows 2000 和 Windows NT 4.0 搭配 Service Pack 6a (SP6a) 和更新版本的 DSClient 中運作。 它們也可以在使用 ie 4.01 和更新版本和 DSClient 的 Windows 98/95 工作站中運作。 但是，如果從 shell 啟動了多重選屬性頁，則會 [**\_ 通知 WM ADSPROP \_ 通知 \_ 錯誤**](wm-adsprop-notify-error.md) 訊息及其對應的 helper 函式， [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) 和 [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) 無法正常運作，且不會顯示。 如果在系統管理工具（例如 AD 使用者和電腦）內啟動多重複選屬性頁面，則所有訊息都可以正常運作，並可在多重複選屬性頁面中顯示。

Active Directory Domain Services 使用下列訊息：

-   [**WM \_ ADSPROP \_ 通知 \_ 申請**](wm-adsprop-notify-apply.md)
-   [**WM \_ ADSPROP \_ 通知 \_ 變更**](wm-adsprop-notify-change.md)
-   [**WM \_ ADSPROP \_ 通知 \_ 錯誤**](wm-adsprop-notify-error.md)
-   [**WM \_ ADSPROP \_ 通知 \_ 結束**](wm-adsprop-notify-exit.md)
-   [**WM \_ ADSPROP \_ 通知 \_ 前景**](wm-adsprop-notify-foreground.md)
-   [**WM \_ ADSPROP \_ 通知 \_ PAGEHWND**](wm-adsprop-notify-pagehwnd.md)
-   [**WM \_ ADSPROP \_ 通知 \_ PAGEINIT**](wm-adsprop-notify-pageinit.md)
-   [**WM \_ ADSPROP \_ 通知 \_ SETFOCUS**](wm-adsprop-notify-setfocus.md)
-   [**WM \_ ADSPROP \_ 工作表 \_ 建立**](wm-adsprop-sheet-create.md)
-   [**WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知**](wm-dsa-sheet-close-notify.md)
-   [**WM \_ DSA \_ 工作表 \_ 建立 \_ 通知**](wm-dsa-sheet-create-notify.md)

 

 




