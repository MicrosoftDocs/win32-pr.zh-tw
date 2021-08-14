---
title: 註冊變更通知
description: 用戶端可以註冊，以接收路由表管理員中儲存之路由資訊變更的通知。 此要求只能在用戶端向路由表管理員註冊之後進行。
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7049478a5be834b08b7bb17ad9ebfb0fdf70736837f27d53e7900bf7bfdc88dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788617"
---
# <a name="registering-for-change-notification"></a>註冊變更通知

用戶端可以註冊，以接收路由表管理員中儲存之路由資訊變更的通知。 此要求只能在用戶端向路由表管理員註冊之後進行。

若要註冊變更通知，用戶端必須呼叫 [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification)，並指定用戶端必須接收通知的變更類型。 如果用戶端必須在特定目的地發生變更時收到通知，用戶端會針對每個目的地呼叫 [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) 一次。

用戶端可以藉由呼叫 [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification)來停止接收變更通知。

如需示範如何使用這些函數的範例程式碼，請參閱 [註冊變更通知](register-for-change-notification.md)。

 

 




