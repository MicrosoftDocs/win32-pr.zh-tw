---
description: IUpdateDownloader 介面會定義下列屬性。
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: IUpdateDownloader 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf66fbdad678ef6a78d0fa049ecb59c34be2ca9d08c873e24e82c35c9d1eb1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738287"
---
# <a name="iupdatedownloader-properties"></a>IUpdateDownloader 屬性

[**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)介面會定義下列屬性。



| 屬性                                                             | 描述                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | 取得和設定目前的用戶端應用程式。                                                                                                                              |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | 取得和設定布林值，指出 Windows Update 代理程式 (WUA) 是否會強制下載已安裝或無法安裝的更新。 |
| [**優先順序**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | 取得和設定下載的優先權層級。                                                                                                                          |
| [**更新**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | 取得和設定介面，其中包含指定要下載之更新的唯讀集合。                                                            |



 

 

 



