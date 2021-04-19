---
description: 下表列出事件取用者提供者作業所產生的疑難排解事件類別。
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: ConsumerProvider 疑難排解類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536c23fb35ca6a4d2146cf87782768c51f37a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980561"
---
# <a name="consumerprovider-troubleshooting-classes"></a>ConsumerProvider 疑難排解類別

下表列出事件取用者 [*提供*](gloss-e.md) 者作業所產生的疑難排解事件類別。

您可以訂閱抽象基類的 [**MSFT \_ ProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) 通知，以取得下列所有事件。



|                                                                                                 |                                                                                 |
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

 

 
