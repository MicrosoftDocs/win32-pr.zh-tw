---
title: 設定持續性
description: 設定持續性
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media Format SDK，持續性
- Windows Media Format SDK，設定持續性
- Advanced Systems Format (ASF) ，持續性
- ASF (Advanced Systems Format) ，持續性
- Advanced Systems Format (ASF) 、設定持續性
- ASF (Advanced Systems Format) ，設定持續性
- 設定持續性
- 保存性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374554"
---
# <a name="configuration-persistence"></a>設定持續性

這份檔中所述的任何可寫入屬性都不是由 Windows Media SDK 儲存。 使用 SDK 的每個應用程式都必須視需要提供自己的持續性程式，並在每個 SDK 實例上叫用適當的 set 方法。 如此一來，某個應用程式所做的設定變更不會影響另一個應用程式。 例如，在一個播放程式中變更緩衝時間並不會影響另一個玩家。

這項規則的唯一例外是認證資訊。 如果應用程式在從 **AcquireCredentials** 呼叫傳回時，必須保存使用者識別碼和密碼資訊，SDK 就會儲存這項資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行網路功能**](implementing-network-functionality.md)
</dt> <dt>

[**IWMCredentialCallback 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




