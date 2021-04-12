---
title: 註冊變更通知
description: 用戶端可以註冊，以接收路由表管理員中儲存之路由資訊變更的通知。 此要求只能在用戶端向路由表管理員註冊之後進行。
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300680"
---
# <a name="registering-for-change-notification"></a>註冊變更通知

用戶端可以註冊，以接收路由表管理員中儲存之路由資訊變更的通知。 此要求只能在用戶端向路由表管理員註冊之後進行。

若要註冊變更通知，用戶端必須呼叫 [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)，並指定用戶端必須接收通知的變更類型。 如果用戶端必須在特定目的地發生變更時收到通知，用戶端會針對每個目的地呼叫 [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) 一次。

用戶端可以藉由呼叫 [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)來停止接收變更通知。

如需示範如何使用這些函數的範例程式碼，請參閱 [註冊變更通知](register-for-change-notification.md)。

 

 




