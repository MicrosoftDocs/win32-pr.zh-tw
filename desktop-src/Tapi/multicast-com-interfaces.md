---
description: 多播 COM 介面可讓您存取網路功能，以在多播位址上配置、更新和釋放租用。
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: 多播 COM 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01370372e3ea05b27dc789f90918b148075c28f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689443"
---
# <a name="multicast-com-interfaces"></a>多播 COM 介面

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

多播 COM 介面可讓您存取網路的功能，以在多播位址上配置、更新和釋放租用。 它們會封裝一組函數和資料結構定義。 COM 介面讓程式設計師免于理解和操作這些資料結構的負擔。 此外，因為 TAPI 3 本身是以 COM 為基礎，所以這些介面可讓您以與 TAPI 3 所提供的其他功能一致的方式來存取多播位址配置。 使用 Visual Basic、JAVA 或指令碼語言所撰寫的應用程式通常無法直接存取 Windows API，因此能夠使用這些介面。

多播位址配置目前是 IETF 工作群組的主體。 若要存取目前的資訊，請使用任何網際網路搜尋引擎來查詢 "MDHCP" 或 "MADCAP" 和 "Internet draft"。 除了 MADCAP，建議的架構還包含網域內的伺服器對伺服器協調通訊協定，以及用於領域間協調的通訊協定。 雖然此架構目前不斷演進，但用戶端不需要關注此配置的詳細資料。

此元件目前僅支援 IP 第4版位址。

> [!Note]  
> 用於這些介面的通訊協定目前名為 MADCAP。 在先前的版本中，它稱為 MDHCP。

 

多播物件是藉由在 [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)介面上呼叫 **CoCreateInstance** 所建立。 **IMcastAddressAllocation** 介面會公開 [**EnumerateScopes**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes)方法，可讓應用程式取得所有可用多播範圍的清單。

一旦取得工作範圍，就會使用 [**RequestAddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) 方法向伺服器要求多播位址。 如果要求成功，則會傳回 [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) 指標。 然後，您可以使用此介面公開的 [**EnumerateAddresses**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) 方法來取得位址。

與會議相關聯的每個媒體物件都會公開 [**ITConnection**](itconnection.md) 介面。 [**ITConnection：： SetAddressInfo**](itconnection-setaddressinfo.md)方法允許指派取得給會議媒體的多播位址。 您必須為與會議相關聯之每個媒體物件的每個 **ITConnection** 介面設定位址。

 

 



