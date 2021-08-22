---
description: Windows 10 可協助您的應用程式在行動裝置上執行時，將耗電量優化。
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: 電源管理的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ac6ba320a98fce339f5bfacfe2d9b4a259be5a8150b2bcaabcac41179869e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143191"
---
# <a name="whats-new-in-power-management"></a>電源管理的新功能

Windows 10 可協助您的應用程式在行動裝置上執行時，將耗電量優化。

## <a name="battery-saver"></a>省電模式

在此版本中，當省電模式開啟或關閉時，您的應用程式可以收到通知。 藉由回應不斷變化的電源，您的應用程式可以與省電模式協同合作，以節省能源並協助延長電池壽命。 如需有關省電模式的一般資訊，請參閱 [硬體元件指導方針中的省電模式 () ](/windows-hardware/design/component-guidelines/battery-saver)。

-   [**GUID \_省 \_ 電 \_ 狀態**](power-setting-guids.md) ：當省電模式開啟或關閉時，請使用這個新的 GUID 搭配 [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) 函式來通知。

-   [**系統 \_電源 \_ 狀態**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) ：已更新此結構以支援省電模式。 第四個成員 **SystemStatusFlag** (先前命名為 **Reserved1**) ，現在指出省電模式是否已參與。 您可以使用 [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) 函式來取得此結構的指標。

 

 
