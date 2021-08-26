---
title: 相互排除物件
description: 相互排除物件
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows媒體格式 SDK，相互排除物件
- Advanced Systems Format (ASF) ，相互排除物件
- ASF (Advanced Systems Format) ，相互排除物件
- 物件，相互排除物件
- 相互排除，物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d7e780ac18dcad7ef04f9bb50d3a7389851156866980b21fbe0c231bcb057d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929928"
---
# <a name="mutual-exclusion-object"></a>相互排除物件

互斥物件是用來指定多個資料流程，一次只能傳遞一個。 這可以透過數種方式來使用，例如以數種語言提供音訊串流作為一個影片串流的聲段。

相互排除是設定檔的選擇性部分。 您可以針對設定檔中現有的相互排除資訊建立相互排除物件，或建立空白，準備接收新資料。 相互排除物件不能獨立存在於設定檔物件中。 若要儲存相互排除物件的內容，您必須呼叫 [**IWMProfile：： AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)。

若要建立相互排除物件，請使用下列其中一種方法。



| 方法                                                                              | 描述                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | 建立相互排除的物件，而不包含任何資料。                                                                                                         |
| [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | 建立從設定檔填入資料的相互排除物件。 使用互斥索引來識別所需的相互排除資訊。 |



 

上表中的兩個方法都會設定 **IWMMutualExclusion** 介面的指標。 **IWMMutualExclusion** 會繼承 **IWMStreamList** 介面，且永遠不需要直接存取。 您可以藉由呼叫 **QueryInterface** 方法來取得相互排除物件的另一個介面。

每個相互排除物件都支援下列介面。



| 介面                                          | 描述                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | 設定並抓取要使用的互斥類型。                                                                                            |
| [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | 將資料流程組織成記錄，這些記錄可用來建立複雜的互斥案例。 繼承 **IWMMutualExclusion** 的所有方法。 |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | 管理互斥資料流程的清單。                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**互斥**](mutual-exclusion.md)
</dt> <dt>

[**物件**](objects.md)
</dt> <dt>

[**設定檔管理員物件**](profile-manager-object.md)
</dt> </dl>

 

 




