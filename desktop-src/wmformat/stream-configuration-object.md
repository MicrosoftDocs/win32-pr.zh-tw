---
title: 串流設定物件
description: 串流設定物件
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Media 格式 SDK、串流設定物件
- Advanced Systems Format (ASF) ，stream configuration 物件
- ASF (Advanced Systems Format) ，stream configuration objects
- 物件，資料流程設定物件
- 串流設定物件
- 串流，串流設定物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104092585"
---
# <a name="stream-configuration-object"></a>串流設定物件

資料流程設定物件是用來在 ASF 檔案中指定媒體資料流程的屬性。 您可以為設定檔中的現有資料流程建立串流設定物件，也可以建立空的串流設定物件，準備好接收新的資料。 資料流程設定物件不能獨立存在於設定檔物件中。 若要儲存資料流程設定物件的內容，您必須呼叫 [**IWMProfile：： AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) 來加入新的資料流程或 [**IWMProfile：： ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) ，以儲存對現有資料流程所做的變更。

若要建立串流設定物件，請使用下列其中一種方法。



| 方法                                                                | 描述                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | 建立不含任何資料的資料流程設定物件。                                                                          |
| [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | 建立以設定檔中的資料填入的資料流程設定物件。 使用資料流程索引來識別所需的資料流程。  |
| [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | 建立以設定檔中的資料填入的資料流程設定物件。 使用資料流程號碼來識別所需的資料流程。 |



 

上表中的所有方法都會設定 **IWMStreamConfig** 介面的指標。 您可以藉由呼叫 **QueryInterface** 方法來取得資料流程設定物件的其他介面。

Stream configuration 物件支援下列介面。



| 介面                                        | 描述                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | 設定和抓取資料流程的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構。                                    |
| [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | 設定及抓取所有資料流程都不需要的屬性，例如變數位元速率 (VBR) 設定。                  |
| [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | 設定和抓取資料流程的所有基本資訊。                                                              |
| [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | 設定與資料流程相關聯的資料單位延伸模組類型。 繼承 **IWMStreamConfig** 的所有方法。 |
| [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | 設定和捕獲資料流程的語言。 繼承 **IWMStreamConfig** 和 **IWMStreamConfig2** 的所有方法。 |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | 管理影片資料流程的屬性。 這是選擇性的介面，只適用于影片串流。            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> <dt>

[**物件**](objects.md)
</dt> <dt>

[**設定檔管理員物件**](profile-manager-object.md)
</dt> </dl>

 

 




