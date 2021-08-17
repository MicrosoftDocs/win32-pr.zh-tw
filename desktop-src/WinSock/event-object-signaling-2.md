---
description: WSPEventSelect 的行為與 WSPAsyncSelect 完全相同，不同之處在于，它不會在發生任何指定的 FD \_ XXX 網路事件時（例如，fd 讀取、fd 寫入 ) 等）傳送 Windows 訊息， (例如， \_ \_ 設定指定的事件物件。
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: 事件物件信號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eed237db696298a2f8053fb61cb0009d9d25d7f37497e0a19d58044d27d8dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132620"
---
# <a name="event-object-signaling"></a>事件物件信號

[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))的行為與 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))完全相同，不同之處在于，它不會在發生任何指定的 FD \_ XXX 網路事件時（例如，fd 讀取、fd 寫入 ) 等）傳送 Windows 訊息， (例如， \_ \_ 設定指定的事件物件。

此外， \_ 服務提供者還會記住特定的 FD XXX 網路事件。 這是必要的，因為出現任何和所有提名的網路事件，將導致單一事件物件變成信號。 呼叫 [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) 會導致網路事件記憶體的目前內容複寫到用戶端提供的緩衝區，以及要清除的網路事件記憶體。 用戶端也可以指定要以不可部分完成的方式，連同網路事件記憶體一起清除的特定事件物件。

 

 
