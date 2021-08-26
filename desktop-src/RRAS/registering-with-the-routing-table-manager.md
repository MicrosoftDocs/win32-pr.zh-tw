---
title: 向路由表管理員註冊
description: 在用戶端可以存取路由表之前，它必須先使用 RtmRegisterEntity 函式向路由表管理員註冊。
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- 路由表管理員第2版 RRAS，註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 088072fac8679d9b2f87729b67a826ac850e77109f18b28fef3c2dc33c433f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028288"
---
# <a name="registering-with-the-routing-table-manager"></a>向路由表管理員註冊

在用戶端可以存取路由表之前，它必須先使用 [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) 函式向路由表管理員註冊。

當用戶端註冊時，它會將 [**RTM \_ 實體 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) 結構傳遞給路由表管理員。 此結構包含可唯一識別用戶端、位址系列，以及用戶端所註冊的路由表管理員實例的資訊。 用戶端也可以建立 [**RTM \_ 事件 \_ 回呼**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) 回呼。 路由表管理員將使用此回呼來通知用戶端事件，例如變更通知和用戶端註冊。

路由表管理員完成其註冊處理，並將控制碼傳回給用戶端。 用戶端必須對 RTMv2 函式的所有後續呼叫使用這個控制碼。

RTMv2 中使用的 [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) 函數類似于 RTMv1 中使用的 [**RtmRegisterClient**](rtmregisterclient.md) 函數。 **RtmRegisterClient** 函式已過時，但使用 IPX 的用戶端除外。

一旦用戶端完成與路由表管理員的互動之後，就必須呼叫 [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity)。 路由表管理員會損毀與用戶端相關聯的控制碼。 為了避免記憶體流失，用戶端必須確保它會在呼叫 **RtmDeregisterEntity** 之前，釋放所有的控制碼並刪除其所擁有的所有路由和下一個躍點。

如需示範如何使用這些函數的範例程式碼，請參閱 [向路由表管理員註冊](register-with-the-routing-table-manager.md) ，並 [使用事件通知回呼](use-the-event-notification-callback.md)。

 

 




