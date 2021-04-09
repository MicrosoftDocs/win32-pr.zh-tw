---
description: WMI 提供一組疑難排解類別，可讓腳本和應用程式在 WMI 核心和提供者作業期間，用來取得 WMI 內部狀態的相關資訊。
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: WMI 疑難排解類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945291"
---
# <a name="wmi-troubleshooting-classes"></a>WMI 疑難排解類別

WMI 提供一組疑難排解類別，可讓腳本和應用程式在 WMI 核心和提供者作業期間，用來取得 WMI 內部狀態的相關資訊。 如需 WMI 疑難排解的詳細資訊，請參閱 [Wmi 疑難排解](wmi-troubleshooting.md) 和 [提供者設定和疑難排解類別](provider-configuration-and-troubleshooting-classes.md)。

WMI 有幾個基本的疑難排解類別，適用于 WMI 核心和提供者作業：

-   [**MSFT \_ 的 wmiprovider \_ 計數器**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    每個電腦系統上只會找到其中一個類別。 它會提供該系統上各種類型的提供者作業計數。

-   [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    事件疑難排解類別衍生自 [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)。 此類別的查詢會傳回事件類別的實例，例如 [**msft \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) 或 [**msft \_ 的 wmiprovider \_ CreateInstanceEnumAsyncEvent \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post)。

    下列清單提供衍生自 [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)之事件類別的不同類別連結：

    -   [提供者事件疑難排解類別](provider-event-troubleshooting-classes.md)
    -   [ConsumerProvider 疑難排解類別](consumerprovider-troubleshooting-classes.md)
    -   [WMI 服務事件疑難排解類別](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

[接收 WMI 事件](receiving-a-wmi-event.md)
</dt> </dl>

 

 
