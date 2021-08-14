---
title: 正在抓取變更
description: 一旦用戶端註冊了特定變更的通知，且發生一或多個這些變更，用戶端就會收到來自路由表管理員的通知。
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea0de478a1f46e2281b18644026c2d8db44d113679f4f4f9bd5b18a1123e9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788168"
---
# <a name="retrieving-changes"></a>正在抓取變更

一旦用戶端註冊了特定變更的通知，且發生一或多個這些變更，用戶端就會收到來自路由表管理員的通知。 路由表管理員會使用先前呼叫 [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)所提供的 [**RTM \_ 事件 \_ 回呼**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback)回呼。 路由表管理員指出 \_ \_ 已發生 RTM 變更通知事件。

如需示範如何使用這些函數的範例程式碼，請參閱 [使用事件通知回呼](use-the-event-notification-callback.md)。

 

 




