---
description: 描述構成電源配置的電源原則設定。
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: 電源原則設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f8c0dbd4c7f2a27b6e6b96528c689c6609c175eded58a1de625af71e965f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674308"
---
# <a name="power-policy-settings"></a>電源原則設定

電源計劃和方案包含喜好設定和原則設定。

電源計劃是由一組電源設定喜好設定所組成。 這些喜好設定包含每個電源設定的 AC 和 DC 值。 每個電源計劃都是透過唯一的 **GUID** 和易記名稱來識別。 WindowsVista 有三個預設的電源計劃：省電、平衡和高效能。 您可以自訂這些計畫，也可以建立其他方案。 所有電源計劃都有一個特質屬性，指出方案的整體電源節省行為。

下表顯示三個電源計劃特質。 

| 顯示名稱     | 描述                                                                   | **GUID**                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| 節能程式      | 提供降低的效能，可能會增加省電量。                | a1841308-3541-4fab-bc81-f71556f20b4a |
| 平衡         | 根據需求自動平衡效能和耗電量。 | 381b4222-f694-41f0-9685-ff5bb260df2e |
| 高效能 | 以較高的耗電量來提供最高的效能。      | 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c |



 

> [!Note]  
> 支援 [新式待命](/windows-hardware/design/device-experiences/modern-standby) 模式的裝置只允許 **平衡** 的電源計劃。 **新式待命** 是電源設定管理的較新且更簡化的解決方案。

 

每部電腦都有一個主動式電源計劃。 根據預設，未具許可權使用者可以存取系統電源設定。 您可以透過 [電源設定] 上的 Acl 或群組原則，來控制所有或個別電源設定的存取權。 應用程式應該呼叫 [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) ，以判斷使用者是否具有電源設定的存取權。

每個電源設定都是由唯一的 **GUID** 來識別，並包含好記的名稱、描述、允許的值，以及 AC 和 DC 的預設值。 您可以使用 [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) 函式來建立自訂電源設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[電源配置](power-schemes.md)
</dt> </dl>

 

 
