---
title: 通知旗標
description: 通知旗標
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- MCI_NOTIFY 旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375233"
---
# <a name="the-notify-flag"></a>通知旗標

「通知」 (MCI \_ 通知) 旗標會指示裝置在裝置完成動作時張貼 a [**MM MCINOTIFY**](mm-mcinotify.md) 的訊息。 您的應用程式必須有一個視窗程式來處理 MM \_ MCINOTIFY 訊息，通知才會有任何作用。 MM \_ MCINOTIFY 訊息表示命令的處理已完成，但不會指出命令已順利完成、失敗或被取代或中止。

應用程式會在發出命令時，指定訊息的目的地視窗控制碼。 在命令字串介面中，這個控制碼是 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式的最後一個參數。 在命令訊息介面中，控制碼是以命令訊息所傳送之結構的 **dwCallBack** 成員的低序位字組來指定。  (與命令訊息相關聯的每個結構都包含這個成員。 ) 

 

 