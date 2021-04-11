---
title: 列舉已註冊的實體
description: 在用戶端註冊之後，用戶端可以取得已向路由表管理員註冊的所有其他用戶端清單。 如果偵測到特定類型的用戶端存在，某些用戶端必須執行某些作業。
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021499"
---
# <a name="enumerating-registered-entities"></a>列舉已註冊的實體

在用戶端註冊之後，用戶端可以取得已向路由表管理員註冊的所有其他用戶端清單。 如果偵測到特定類型的用戶端存在，某些用戶端必須執行某些作業。

用戶端可以呼叫 [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) 函數。 傳回 [**RTM \_ 實體 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) 結構的緩衝區。 在用戶端處理這項資訊之後，用戶端應該呼叫 [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) ，以釋放 **RTM \_ 實體 \_ 資訊** 結構中的控制碼。

如果路由表管理員用戶端在呼叫 [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)時提供了回呼函式，當任何其他用戶端註冊或取消註冊時，就會通知用戶端。

如需示範如何使用這些函數的範例程式碼，請參閱 [列舉已註冊的實體](enumerate-the-registered-entities.md) 並 [使用事件通知回呼](use-the-event-notification-callback.md)。

 

 




