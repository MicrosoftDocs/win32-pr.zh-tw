---
title: 通知處理常式
description: 非同步 RasDial 呼叫必須指定通知處理常式。
ms.assetid: 6d23d6ac-08ad-4fe2-a4af-021e4d384079
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe735a17de4386bc48648cd20decd218ab102d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932528"
---
# <a name="notification-handlers"></a>通知處理常式

非同步 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫必須指定通知處理常式。 在非同步連接作業期間，「遠端存取」連線管理員會在連線 [狀態](connection-states.md) 變更或發生錯誤時，使用通知處理常式來通知 RAS 用戶端。

通知處理常式所執行的動作可以分為下列類別：

-   [處理錯誤](handling-ras-errors.md)。
-   為使用者提供意見反應，因為連接作業會繼續進行各種連接狀態。 請參閱 [語音總機](informational-notifications.md)。
-   處理 [暫停狀態](paused-states.md)。
-   連接作業完成時，通知 RAS 用戶端應用程式。 查看 [完成通知](completion-notifications.md)。

有三種類型的通知處理常式，每一個都會收到相同的基本資訊：目前的連接狀態，以及只有在發生錯誤時為非零的錯誤碼。



| 值                                | 定義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)   | 回呼函式原型，它只會接收目前的連接狀態和錯誤碼資訊。                                                                                                                                                                                                                                                                                                                                                                                    |
| [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) | 除了基本資訊之外，還會收到 **HRASCONN** 連接控制碼和延伸錯誤資訊的回呼函式原型。 連接控制碼參數讓 [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) 適用于支援多個同時連接作業的用戶端應用程式。 這可讓用戶端為所有作業指定相同的回呼函式，並啟用回呼函式來判斷哪個連接正在變更狀態。 |
| [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) | 類似于 [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)的回呼函數。 不過， [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) 已增強，可支援多重連接連線。                                                                                                                                                                                                                                                                                                                             |
| 視窗控制碼                        | RAS 傳送包含目前連接狀態和錯誤碼資訊之 [**WM \_ RASDIALEVENT**](wm-rasdialevent.md) 訊息的視窗控制碼。 如果您的原始程式碼必須與16位的 Windows 相容，請使用這個方法，因為16位 Windows 不支援其中一個回呼函式。                                                                                                                                                                            |



 

遠端存取連線管理員會暫停連接作業，直到通知處理常式傳回為止。 基於這個理由，除非發生錯誤，否則處理常式應該儘快傳回。

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)函式不應該從通知處理常式內呼叫。 另一個遠端存取函式 ( [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa)、 [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa)、 [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa)、 [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)和 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)) 可從處理常式內呼叫。

 

 




