---
description: 開機事件收集器 WMI 提供者可讓您存取 Windows Server 上的設定和開機事件集合功能的連接和設定資訊。
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: 開機事件收集器 WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846976"
---
# <a name="boot-event-collector-wmi-provider"></a>開機事件收集器 WMI 提供者

## <a name="purpose"></a>目的

開機事件收集器 WMI 提供者可讓您存取 Windows Server 上的設定和開機事件集合功能的連接和設定資訊。 這可讓您查看目前的連接清單，以及收集器伺服器與其目的電腦之間的連接歷程記錄。 此外，此提供者可讓您管理收集器伺服器的設定。

> [!Note]  
> 開機事件收集器 WMI 提供者會在 BEvtCol.exe 中執行。

 

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**TargetForwarding**](targetforwarding.md)
</dt> <dd>

從目的電腦抓取轉送資料。

</dd> <dt>

[**TargetForwardingDestination**](targetforwardingdestination.md)
</dt> <dd>

包含所收集資料的已知目的地。 只有在收集器在啟用狀態記錄檔的情況下才可使用。

</dd> <dt>

[**TargetForwardingHistory**](targetforwardinghistory.md)
</dt> <dd>

目的電腦轉送資料變更的最近歷程記錄。

</dd> <dt>

[**控制**](control.md)
</dt> <dd>

收集器實例的控制權。 需要系統管理員 (BA) 許可權。

</dd> </dl>

 

 



