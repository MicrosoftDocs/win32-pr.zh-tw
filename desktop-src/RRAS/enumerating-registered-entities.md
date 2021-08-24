---
title: 列舉已註冊的實體
description: 在用戶端註冊之後，用戶端可以取得已向路由表管理員註冊的所有其他用戶端清單。 如果偵測到特定類型的用戶端存在，某些用戶端必須執行某些作業。
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1d67a810806c1bc29f8f18c4cdea9f3a36e5b5a95922e8f66a943a99923ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674158"
---
# <a name="enumerating-registered-entities"></a>列舉已註冊的實體

在用戶端註冊之後，用戶端可以取得已向路由表管理員註冊的所有其他用戶端清單。 如果偵測到特定類型的用戶端存在，某些用戶端必須執行某些作業。

用戶端可以呼叫 [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) 函數。 傳回 [**RTM \_ 實體 \_ 資訊**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) 結構的緩衝區。 在用戶端處理這項資訊之後，用戶端應該呼叫 [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) ，以釋放 **RTM \_ 實體 \_ 資訊** 結構中的控制碼。

如果路由表管理員用戶端在呼叫 [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity)時提供了回呼函式，當任何其他用戶端註冊或取消註冊時，就會通知用戶端。

如需示範如何使用這些函數的範例程式碼，請參閱 [列舉已註冊的實體](enumerate-the-registered-entities.md) 並 [使用事件通知回呼](use-the-event-notification-callback.md)。

 

 




