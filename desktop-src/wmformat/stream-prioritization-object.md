---
title: 串流優先順序物件
description: 串流優先順序物件
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows Media Format SDK，資料流程優先順序物件
- Advanced Systems Format (ASF) 、串流優先順序物件
- ASF (Advanced 系統格式) 、串流優先順序物件
- 物件，資料流程優先順序物件
- 串流優先權物件
- 資料流程，資料流程優先順序物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965633"
---
# <a name="stream-prioritization-object"></a>串流優先順序物件

資料流程優先權物件是用來指定設定檔中資料流程的重要性順序。 當完全播放因為位元速率限制而無法完成時，最低優先順序的資料流程將會先卸載。

您可以為設定檔中現有的資料流程優先順序資料建立資料流程優先權物件，或建立空白的資料流程，準備好接收新的資料。 資料流程優先權物件不能獨立存在於設定檔物件中。 若要儲存資料流程優先權物件的內容，您必須呼叫 [**IWMProfile3：： SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)。 若要建立資料流程優先權物件，請使用下列其中一種方法。



| 方法                                                                                          | 描述                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | 建立不含任何資料的資料流程優先權物件。                     |
| [**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | 建立以設定檔中的資料填入的資料流程優先權物件。 |



 

上表中的兩個方法都會設定 **IWMStreamPrioritization** 介面的指標。 這是資料流程優先權物件唯一支援的介面。



| 介面                                                  | 描述                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | 管理資料流程優先權物件內資料流程的清單。 |



 

## <a name="remarks"></a>備註

指定的設定檔只可有一個資料流程優先順序。 如果您為已包含資料流程優先權的設定檔建立新的資料流程優先順序，則會刪除舊的資料流程。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**設定檔物件**](profile-object.md)
</dt> <dt>

[**使用資料流程優先順序**](using-stream-prioritization.md)
</dt> </dl>

 

 




