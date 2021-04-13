---
title: 頻寬共用物件
description: 頻寬共用物件
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows Media Format SDK，頻寬共用物件
- Advanced Systems Format (ASF) 、頻寬共用物件
- ASF (Advanced 系統格式) 、頻寬共用物件
- 物件，頻寬共用物件
- 頻寬共用、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374494"
---
# <a name="bandwidth-sharing-object"></a>頻寬共用物件

頻寬共用物件是用來指出兩個或多個資料流程（不論其個別的位元速率為何）永遠不會在兩者之間使用超過指定的頻寬量。 這是純粹的參考物件;此 SDK 的任何物件不會以程式設計的方式強制執行在其中設定的位速度。

頻寬共用資訊是設定檔的選擇性部分。 您可以為設定檔中現有的頻寬共用資訊建立頻寬共用物件，也可以建立空的，準備好接收新的資料。 設定檔物件不能獨立存在頻寬共用物件。 若要儲存頻寬共用物件的內容，您必須呼叫 [**IWMProfile3：： AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)。

若要建立頻寬共用物件，請呼叫下列其中一種方法。



| 方法                                                                                  | 描述                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | 建立不含任何資料的頻寬共用物件。                                                                                                           |
| [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | 建立以設定檔中的資料填入的頻寬共用物件。 使用頻寬共用索引來識別所需的頻寬共用資訊。 |



 

上表中的兩個方法都會設定 **IWMBandwidthSharing** 介面的指標。 **IWMBandwidthSharing** 會繼承 **IWMStreamList** 介面，因此不需要使用這個物件來呼叫 **QueryInterface** 。

每個頻寬共用物件都支援下列介面。



| 介面                                          | 描述                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | 管理將共用頻寬之資料流程群組的屬性。 |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | 管理將共用頻寬的資料流程清單。                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**頻寬共用**](bandwidth-sharing.md)
</dt> <dt>

[**設定檔管理員物件**](profile-manager-object.md)
</dt> <dt>

[**設定檔物件**](profile-object.md)
</dt> </dl>

 

 




