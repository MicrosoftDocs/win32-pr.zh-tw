---
title: RAS 伺服器安全性驗證
description: 當 Windows NT/Windows 2000 RAS 伺服器收到呼叫時，它會叫用已註冊的 ras 安全性 DLL 的 RasSecurityDialogBegin 函式（如果有的話）。
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532bda51d6e9ee0ea90c900fa974827e1840e7e633caf48fbadec5fe6a701a22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028738"
---
# <a name="ras-server-security-authentication"></a>RAS 伺服器安全性驗證

當 Windows NT/Windows 2000 RAS 伺服器收到呼叫時，它會叫用已註冊的 ras 安全性 DLL 的 [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin)函式（如果有的話）。 此呼叫會通知安全性 DLL 開始其遠端使用者的驗證。 RAS 伺服器會先呼叫 **RasSecurityDialogBegin** ，然後再執行其 PPP 或 RAS 驗證。

[**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin)呼叫會將下列資訊傳遞給安全性 DLL：

-   用來識別連接的通訊埠控制碼。
-   與遠端使用者通訊時所要使用之緩衝區的指標。
-   完成驗證時要呼叫之 [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) 函數的指標。

埠控制碼和緩衝區指標都有效，直到安全性 DLL 呼叫 [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) 終止驗證交易為止。

[**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete)會向 RAS 伺服器通知遠端使用者的安全性 DLL 驗證結果。 如果安全性 DLL 報告成功，RAS 伺服器會繼續進行其 PPP 和遠端使用者的 RAS 驗證。 如果安全性 DLL 報告遠端使用者驗證失敗，或發生錯誤，RAS 伺服器將會停止回應，並在事件記錄檔中記錄錯誤或驗證失敗。

 

 




