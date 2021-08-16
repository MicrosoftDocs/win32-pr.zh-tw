---
title: RAS 安全性 DLL 驗證交易
description: Windows NT/Windows 2000 RAS 伺服器會呼叫安全性 DLL 的 RasSecurityDialogBegin 函式，以開始驗證遠端使用者。
ms.assetid: e6549812-d906-4163-b9c8-86f8f1cb1ad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea463c56d96cad13fb55a2b6e0bbdfc154518ba012e4c71c6ab8bdd3213cd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789474"
---
# <a name="ras-security-dll-authentication-transaction"></a>RAS 安全性 DLL 驗證交易

Windows NT/Windows 2000 RAS 伺服器會呼叫安全性 DLL 的 [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin)函式，以開始驗證遠端使用者。 RAS 伺服器被封鎖，而且在 **RasSecurityDialogBegin** 傳回之前無法接受任何其他呼叫。 基於這個理由， **RasSecurityDialogBegin** 應該複製輸入參數、建立執行緒以執行驗證，並儘快傳回。

安全性 DLL 所建立的執行緒會使用 [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) 和 [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) 函數來與遠端電腦通訊。 這些函數無法從任何程式庫進行靜態匯入。 相反地，安全性 DLL 必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式，以動態方式連結至 RASMAN.DLL 中的這些函數。

在驗證交易期間，遠端電腦上的 RAS 連接管理員會顯示終端機視窗。 安全性 DLL 的執行緒會呼叫 [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) ，以傳送要在終端機視窗中顯示的訊息。 執行緒接著會呼叫 [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) ，以接收遠端使用者在終端機視窗中輸入的輸入。 執行緒可以進行任何數目的 **RasSecurityDialogSend** 呼叫，每次呼叫後接著 **RasSecurityDialogReceive** 呼叫。 每次呼叫 **RasSecurityDialogReceive** 之後，執行緒必須呼叫其中一個等候函式（例如 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)），以等候非同步傳送和接收作業完成。 當接收作業完成或經過選擇性的逾時間隔時，RAS 伺服器會通知事件物件。

當執行緒完成遠端使用者的驗證時，它會呼叫 [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) 函數。 此呼叫會將包含驗證交易結果的 [**安全性 \_ 訊息**](/windows/desktop/api/Rasshost/ns-rasshost-security_message) 結構傳遞到 RAS 伺服器。 然後 RAS 伺服器會執行清除順序，其中包含對 DLL [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) 函式的呼叫。 這讓安全性 DLL 有機會執行任何必要的清除。

安全性 DLL 可以呼叫 [**RasSecurityDialogGetInfo**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialoggetinfo) 函數，以抓取與驗證交易相關聯之埠的相關資訊。 **RasSecurityDialogGetInfo** 會填入 [**RAS \_ 安全性 \_ 資訊**](/windows/desktop/api/Rasshost/ns-rasshost-ras_security_info) 結構，指出埠的最後一個 [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) 呼叫的狀態。

 

 