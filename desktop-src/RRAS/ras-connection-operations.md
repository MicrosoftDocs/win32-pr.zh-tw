---
title: RAS 連接作業
description: Windows NT 和更新版本會提供 RasPhonebookDlg 和 RasDialDlg 函式，以顯示用來啟動 RAS 連接作業的內建使用者介面。
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- 連接作業，RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e86ddf1586ce11f43e6b34ef15b89cb2d382b28911968f0b0f08dabd086a86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868458"
---
# <a name="ras-connection-operations"></a>RAS 連接作業

Windows NT 和更新版本會提供 [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga)和 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)函式，以顯示用來啟動 RAS 連接作業的內建使用者介面。 對於大部分的應用程式而言，這是啟動 RAS 連線作業的慣用方式。 Windows 95 目前不支援這些功能。

本節的其餘部分將說明啟動 RAS 連接的低層級功能。 這些函式可在 bothWindows NT 4.0 (和更新版本) 和 Windows 95 上取得。

RAS 用戶端應用程式會使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 功能來建立與 RAS 伺服器的連線。 **RasDial** 函式會啟動連接作業，然後遠端存取連線管理員會執行此作業。

遠端存取連線管理員是一項服務，可處理建立遠端伺服器連線的詳細資料。 此服務也會在連接作業期間提供用戶端狀態資訊。 當應用程式載入 RASAPI32.DLL 時，會自動啟動遠端存取連線管理員。

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫會在啟動連接作業時指定下列資訊：

-   遠端存取連線管理員建立連接所需的 [連接資訊](phone-book-files-and-connection-information.md) 。
-   選擇性的 [通知處理常式，此處理程式](notification-handlers.md) 會在連接操作期間接收進度通知。 如果 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫指定通知處理常式，則呼叫是 [非同步](asynchronous-operations.md)的;否則，它是 [同步](synchronous-operations.md)的。
-   選擇性的 [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) 結構，可啟用或停用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 作業的延伸模組。 擴充功能可讓 RAS 用戶端直接啟用某些數據機設定，以控制 RAS 是否使用電話簿專案中的前置詞和尾碼，以及支援連接作業期間的 [暫停狀態](paused-states.md) 。

 

 