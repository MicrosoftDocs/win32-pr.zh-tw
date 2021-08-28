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
ms.openlocfilehash: dc780ec299c3249006085d348d983f8dab5b76a462c991a2d3665fed7d18f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733798"
---
# <a name="winrm-best-practices"></a>WinRM 最佳作法

本主題說明使用 WinRM API 各項功能的一些最佳作法。

## <a name="quotas"></a>配額

當達到配額時，WinRM 服務會將錯誤傳回給用戶端。 因此，用戶端邏輯必須根據傳回的錯誤明確地重試作業。

## <a name="event-subscriptions"></a>事件訂閱

使用收集器起始的訂用帳戶時，請將遠端電腦的數目限制為500，並在個別的主機進程中找出[Windows 的事件收集器](/windows/desktop/WEC/windows-event-collector)服務 (wecsvc) 。

連接錯誤會保留執行緒，直到超時為止。大量的同時連線錯誤可能會導致執行緒集區耗盡，而導致伺服器沒有回應。

 

 