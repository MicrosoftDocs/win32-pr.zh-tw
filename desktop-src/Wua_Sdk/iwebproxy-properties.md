---
description: IWebProxy 介面會定義下列屬性。
ms.assetid: 449b19ec-dc95-40f7-87af-84fb7dacb328
title: IWebProxy 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96628e7c799232b741e1834964a3a8ef6f6264c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386094"
---
# <a name="iwebproxy-properties"></a>IWebProxy 屬性

[**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)介面會定義下列屬性。



| 屬性                                                   | 描述                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**位址**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)                       | 取得和設定 proxy 伺服器的位址和小數埠號碼。                                                |
| [**自動**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_autodetect)                 | 取得和設定布林值，這個值會指出 [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) 是否會自動偵測 proxy 設定。 |
| [**BypassList**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypasslist)                 | 取得和設定未使用 proxy 伺服器的位址集合。                                                 |
| [**BypassProxyOnLocal**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypassproxyonlocal) | 取得和設定布林值，指出本機位址是否略過 proxy 伺服器。                             |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_readonly)                     | 取得布林值，指出 [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) 物件是否為唯讀。                        |
| [**使用者**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_username)                     | 取得並設定要提交給 proxy 伺服器進行驗證的使用者名稱。                                             |



 

 

 



