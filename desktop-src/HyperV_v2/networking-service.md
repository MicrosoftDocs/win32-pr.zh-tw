---
description: 網路設定檔說明用來設定系統以允許虛擬機器透過網路進行通訊的物件。
ms.assetid: A5C4866B-0F65-47B5-8FC4-B92943842B86
title: 網路服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc85b7a5121a3e7e42f333f829816184b57bd8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972843"
---
# <a name="networking-service"></a>網路服務

網路設定檔說明用來設定系統以允許虛擬機器透過網路進行通訊的物件。 用來在管理作業系統中設定網路交換器的全域網路物件，包括 [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)、 [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)和 [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) 類別。 虛擬機器網路物件，用來設定虛擬機器中 (NIC) 的網路介面卡，包括 [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md)、 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md)和 [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) 類別。

全域網路設定檔的根目錄是 [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) 類別。 此類別代表管理作業系統中的虛擬交換器裝置。 **Msvm \_VirtualEthernetSwitch** 與 Msvm 的同等級器 [**類別 \_**](https://www.bing.com/search?q=**Msvm\_SwitchPort**) 的實例相關聯，代表虛擬交換器上的埠。 **Msvm \_ VirtualEthernetSwitch** 和 [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)類別的實例是透過 [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)類別來建立、刪除和連接， (不會在前面的) 所示。

虛擬交換器管理服務 (VSMS) 代表單一 Hyper-v 主機上的網路服務，並包含 [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) 的方法，可用來控制全域網路資源的定義、修改和終結，例如虛擬交換器、交換器埠和內部乙太網路埠。

虛擬機器中 Ethernet NIC 裝置的表示方式與任何其他裝置的表示類似，如 [**虛擬系統管理服務**](virtual-system-management-service.md)中所述。 [**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md)和 [**Msvm \_ SyntheticEthernetPort**](msvm-syntheticethernetport.md)類別代表虛擬 NIC 裝置，並透過相關聯的 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (RASD) 實例來設定。 此標記法的唯一不尋常特性是，當虛擬機器具現化並接著建立 **Msvm \_ EmulatedEthernetPort** 和 **Msvm \_ SyntheticEthernetPort** 裝置時，它也會為虛擬 NIC 建立相關聯的 [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) 實例。 同樣地，當虛擬機器儲存或關閉，且 **Msvm \_ EmulatedEthernetPort** 和 **Msvm \_ SyntheticEthernetPort** 實例損毀時，相關聯的 [**Msvm \_ VmLANEndpoint**](https://www.bing.com/search?q=**Msvm\_VmLANEndpoint**) 實例也會終結。 **Msvm \_ LANEndpoint** 的目的是做為連接兩個網路埠的橋樑。 在此情況下，它是用來將虛擬 NIC 連線到虛擬交換器裝置上的埠。 換句話說，它會將虛擬機器上的 **Msvm \_ EmulatedEthernetPort** 和 **Msvm \_ SyntheticEthernetPort** 實例連接至虛擬交換器上的特定 [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) 實例。 若要將交換器連接到外部，您必須透過 [**BindExternalEthernetPort**](https://www.bing.com/search?q=**BindExternalEthernetPort**)將實體乙太網路埠系結至 [**Msvm \_ VirtualSwitch**](https://www.bing.com/search?q=**Msvm\_VirtualSwitch**) 。 相反地，當您將交換器連接到主機網路堆疊或內部 NIC 時，請使用 ConnectInternal 讓虛擬機器與主機通訊，而不是在外界。 [**Msvm \_ActiveConnection**](msvm-activeconnection.md) 會將交換器埠連接到在 hyper-v 內連線埠的 [**Msvm \_ SwitchLANEndpoint**](https://www.bing.com/search?q=**Msvm\_SwitchLANEndpoint**) 。 此物件的存在表示交換器埠和 **Msvm \_ SwitchLANEndpoint** 會主動連線，而且與 **Msvm \_ LANEndpoint** 相關聯的乙太網路埠可透過交換器埠與網路通訊。

 

 



