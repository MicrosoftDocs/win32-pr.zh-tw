---
description: 資源虛擬化設定檔提供了一種方法，讓用戶端可以探索虛擬化系統所支援的虛擬資源。
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: 資源管理服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c405cac60df719195466da6ea0c7aadb7bf0d765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027365"
---
# <a name="resource-management-service"></a>資源管理服務

資源虛擬化設定檔提供了一種方法，讓用戶端可以探索虛擬化系統所支援的虛擬資源。 它也會描述每種虛擬資源類型支援的容量（或配置數量）。 下圖顯示資源虛擬化設定檔。

![資源虛擬化設定檔](images/resourcemanagement.png)

資源虛擬化設定檔會定義兩個不同類別的虛擬資源：

-   共用資源：代表主機的資源，也就是能夠在多部虛擬機器之間共用的資源。 [**Msvm \_處理器**](msvm-processor.md) 是共用資源的範例。
-   綜合資源：代表沒有對應主機資源的虛擬資源。 [**Msvm \_EmulatedEthernetPort**](msvm-emulatedethernetport.md) 是綜合資源的範例。

資源集區可用來收集主機資源的類別，以便在中央位置描述其功能和設定時可以輕鬆地找到。 「基本」或「高階」的實作為所收集資源的執行方式沒有任何限制。

從資源集區中，用戶端可以存取 (AC) 的相關聯配置功能。 此類別說明此資源集區所描述之資源的功能。 例如，它可能會指出此資源集區所代表的 [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) 是否支援 (vlan) 或篩選器的虛擬 lan。

AC 設定檔會定義用戶端可以探索指定虛擬資源之有效範圍和預設設定的方式。 AC 物件與每個資源集區相關聯。 四個資源配置設定資料 (RASD) 物件與 AC 物件相關聯，以描述所指定資源配置的最小值、最大值、預設值和增量值。 這些類別一起描述支援功能的整體範圍。 [**Msvm \_ AllocationCapabilities**](msvm-allocationcapabilities.md)實例提供一組 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md)實例的錨點，這些實例會指定虛擬資源的預設和有效的設定範圍。 [**Msvm \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md) association 類別提供了虛擬化平臺所支援之資源的 AC 實例與最小值、最大值、增量和預設設定之間的連結。

 

 



