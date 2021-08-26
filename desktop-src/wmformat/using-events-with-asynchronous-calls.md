---
title: 使用非同步呼叫的事件
description: 使用非同步呼叫的事件
ms.assetid: 98c24176-a632-400e-b23b-5e13f1bd9a27
keywords:
- Windows媒體格式 SDK，使用非同步呼叫的事件
- Windows媒體格式 SDK，非同步呼叫事件
- 事件，非同步呼叫
- 非同步呼叫事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd315b56570419afd81aa3300cfa3ee1dd907e22310aba79432e4533f99a82db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929128"
---
# <a name="using-events-with-asynchronous-calls"></a>使用非同步呼叫的事件

通常，使用以非同步方式呼叫的方法時，您會想要停止進一步處理應用程式，直到方法完成處理為止。 您可以實行任何您想要的技術來處理這種情況。 本節說明如何使用事件來等候呼叫執行緒中的非同步呼叫。 這項技術經常搭配 Windows 媒體格式 SDK 使用，並會在一些範例應用程式中示範。

下列清單摘要說明如何使用事件來等候非同步呼叫。

1.  藉由呼叫 Platform SDK 的 **CreateEvent** 函式，建立與您的應用程式搭配使用的事件。
2.  為您的應用程式執行適當的回呼時，請將需要等候的訊息設為陷阱。 在所需訊息的訊息處理邏輯中，藉由呼叫 Platform SDK 的 **SetEvent** 函式來發出事件的信號。
3.  在您的應用程式中進行非同步事件的呼叫之後，請透過呼叫 Platform SDK 的 **WaitForSingleObject** 函式，等候事件發出信號。 如果您要設計 Windows 的應用程式，您應該建立一個迴圈來檢查 Windows 的訊息，並將 **WaitForSingleObject** 的呼叫包含在迴圈中的短暫等候時間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用回呼方法**](using-the-callback-methods.md)
</dt> </dl>

 

 




