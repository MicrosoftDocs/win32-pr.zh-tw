---
title: WinRM 最佳作法
description: 本主題說明使用 WinRM API 各項功能的一些最佳作法。
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933291"
---
# <a name="winrm-best-practices"></a>WinRM 最佳作法

本主題說明使用 WinRM API 各項功能的一些最佳作法。

## <a name="quotas"></a>配額

當達到配額時，WinRM 服務會將錯誤傳回給用戶端。 因此，用戶端邏輯必須根據傳回的錯誤明確地重試作業。

## <a name="event-subscriptions"></a>事件訂閱

使用收集器起始的訂用帳戶時，請將遠端電腦的數目限制為500，並將 [Windows 事件收集器](/windows/desktop/WEC/windows-event-collector) 服務 (wecsvc) 隔離在個別的主機進程中。

連接錯誤會保留執行緒，直到超時為止。大量的同時連線錯誤可能會導致執行緒集區耗盡，而導致伺服器沒有回應。

 

 