---
description: 時間提供者會使用下列函數。
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: 時間提供者函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c0647574aaa807788e9cf510ce9293460c0394bcdaa794e243009ad6710bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884813"
---
# <a name="time-provider-functions"></a>時間提供者函數

時間提供者會使用下列函數。



| 函式                                                               | 描述                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | 通知系統有新的範例可用。                                              |
| [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | 捕獲系統時間狀態資訊。                                                           |
| [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | 將時間提供者事件記錄在事件記錄檔中。                                                           |
| [**SetProviderStatusFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | 設定時間提供者的狀態資訊。                                                           |
| [**SetProviderStatusInfoFreeFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | 釋放 [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) 結構。                          |
| [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | 時間提供者管理員呼叫的回呼函式，用來關閉時間提供者。        |
| [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | 由時間提供者管理員呼叫的回呼函式，用來將命令傳送給時間提供者。 |
| [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | 載入時間提供者 DLL 時，由時間提供者管理員呼叫的回呼函數。  |



 

 

 



