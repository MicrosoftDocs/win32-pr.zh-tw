---
description: MSFT \_ 提供者類別和 wmi 疑難排解類別是與 wmi 提供者事件結合的 msft 事件類別群組。
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: 提供者設定和疑難排解類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d37443047e9bbde709fc1c7367f0691d16215eff62e39196987b466aea0830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050496"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a>提供者設定和疑難排解類別

[**Msft \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)類別和 wmi 疑難排解類別是與 wmi 提供者事件結合的 [msft 事件類別](msft-classes.md)群組。

[**MSFT \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)類別包含提供者的設定資訊，而且包含下列方法，可讓您載入和卸載提供者，或暫停和繼續提供者作業：

-   [**MSFT \_ 提供者類別的 Load 方法**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [**MSFT \_ 提供者類別的 UnLoad 方法**](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [**MSFT \_ 提供者類別的 Resume 方法**](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [**MSFT 提供者類別的暫止方法 \_**](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

[WMI 疑難排解類別](wmi-troubleshooting-classes.md)的命名為，指出事件是否要在提供者事件之前或之後引發。 例如，在呼叫提供者的 **IWbemEventSecurity：： AccessCheck 的** 之前，會立即產生 [**msft \_ 的 wmiprovider \_ AccessCheck \_ 前置**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre)物件，而會立即呼叫 [**msft \_ 的 wmiprovider \_ AccessCheck \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post)物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

[WMI 疑難排解類別](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
