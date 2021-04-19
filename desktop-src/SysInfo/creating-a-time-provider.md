---
description: 時間提供者會實作為 DLL。 每個 DLL 都可以支援多個時間提供者。 每個提供者都必須負責自己的設定和同步處理。
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: 建立時間提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001769"
---
# <a name="creating-a-time-provider"></a>建立時間提供者

時間提供者會實作為 DLL。 每個 DLL 都可以支援多個時間提供者。 每個提供者都必須負責自己的設定和同步處理。

時間提供者必須執行下列回呼函數：

-   [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

載入提供者 DLL 之後，時間提供者管理員會呼叫 [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)，並將提供者的名稱和指標傳遞至下列函式：

-   [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

這些函數可供時間提供者使用。 時間提供者會使用 [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) ，來傳回時間提供者管理員在傳送命令給時間提供者時所使用的提供者控制碼。 控制碼值是由時間提供者所定義，而且主要是用來區分在相同 DLL 中執行的不同提供者。 時間提供者可以使用 [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)記錄重要的事件。

時間提供者管理員會使用 [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) 將命令傳送給時間提供者。 當時間提供者需要通知時間提供者管理員有可用的時間範例時，它會呼叫 [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)。 時間提供者管理員接著會使用 TPC \_ GetSamples 命令來呼叫 TimeProvCommand，以取出時間範例。 時間提供者管理員最多可能需要16秒鐘的時間來要求範例。 因此，應用程式不應該等待要求。

為確保精確度，時間提供者應該使用 [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)來取出所有時間相關資訊。

當您關閉時間提供者時，時間提供者管理員會呼叫 [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)。

 

 



