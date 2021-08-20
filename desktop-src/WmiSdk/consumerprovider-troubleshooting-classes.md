---
description: 下表列出事件取用者提供者作業所產生的疑難排解事件類別。
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: ConsumerProvider 疑難排解類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c74b82aaf143be5ea1d9144b396a06213940a54073e162bec318264e3fc0a4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925609"
---
# <a name="consumerprovider-troubleshooting-classes"></a>ConsumerProvider 疑難排解類別

下表列出事件取用者 [*提供*](gloss-e.md) 者作業所產生的疑難排解事件類別。

您可以訂閱抽象基類的 [**MSFT \_ ProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) 通知，以取得下列所有事件。



| 事件                                                                                                | 描述                                                                                |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSFT \_ WmiProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | 所有取用者提供者事件的父類別。                                  |
| [**MSFT \_ WmiConsumerProviderLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | 定義成功啟用事件取用者提供者 COM 物件。    |
| [**MSFT \_ WmiConsumerProviderUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | 定義成功停用事件取用者提供者 COM 物件。  |
| [**MSFT \_ WmiConsumerProviderSinkLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | 定義成功啟用事件取用者提供者接收物件。   |
| [**MSFT \_ WmiConsumerProviderSinkUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | 定義成功停用事件取用者提供者接收物件。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

WMI 疑難排解
</dt> <dt>

[接收 WMI 事件](receiving-a-wmi-event.md)
</dt> </dl>

 

 
