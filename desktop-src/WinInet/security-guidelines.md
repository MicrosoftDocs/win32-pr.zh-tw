---
title: 安全性指導方針
description: 請務必讓使用者知道可能的安全性問題。
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0870ecb13e195b226fbbd6e69c3c81fec256d7b35edcf2304167877e154a1dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386138"
---
# <a name="security-guideline"></a>安全性指導方針

請務必讓使用者知道可能的安全性問題。

## <a name="notify-the-user-of-security-related-events"></a>通知使用者 Security-Related 事件

一律通知使用者任何安全性變更、是否為與安全性相關的錯誤（例如憑證失敗），或基礎通訊協定安全性變更（例如從 HTTPS 網站變更為 HTTP 網站）。

## <a name="notify-the-user-of-security-related-errors"></a>通知使用者 Security-Related 錯誤

當您的應用程式收到可能指出安全性問題的錯誤訊息時， **InternetErrorDlg** 函式會提供標準、熟悉的介面，在大部分情況下通知使用者。

屬於此類別的錯誤包括：

**\_ \_ \_ \_ \_ REDIR 上的網際網路 HTTP 至 \_ HTTPS 時發生錯誤**

**\_網際網路 \_ 不正確 \_ CA 錯誤**

**錯誤 \_ 網際網路 \_ POST \_ 為 \_ 非 \_ 安全的**

**\_INTERNET \_ SEC \_ CERT \_ 錯誤**

**\_INTERNET \_ SEC \_ CERT \_ CN \_ 不正確錯誤**

**錯誤 \_ 網際網路 \_ SEC \_ 憑證 \_ 日期 \_ 無效**

若無法通知使用者發生這類錯誤，可能會讓使用者暴露于各種不同的安全性漏洞，包括詐騙攻擊或非自願資訊洩漏。

## <a name="notify-the-user-when-connection-security-changes"></a>在連接安全性變更時通知使用者

當連線的安全性變更時（例如從 HTTPS 至 HTTP），一律會通知使用者。 否則，除非使用者明確選擇不收到這類變更的通知，否則您會隱藏非自願資訊洩漏的風險。

在連接安全性中報告這類變更的函式中， **InternetStatusCallback** 回呼函式和 **InternetConfirmZoneCrossing** 函式。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 