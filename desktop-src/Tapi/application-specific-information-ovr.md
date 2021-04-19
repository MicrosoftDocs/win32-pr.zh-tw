---
description: 應用程式特定的資訊可讓應用程式透過 TAPI 傳遞有關會話的其他資訊。 這項資訊不會由 TAPI 解讀，而且使用方式完全由應用程式定義。
ms.assetid: e72e4164-3578-4e18-aea0-09d47d385b57
title: 應用程式特定資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf4a10413f914eb0bb2da763022f1946811ce12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974730"
---
# <a name="application-specific-information"></a>應用程式特定資訊

應用程式特定的資訊可讓應用程式透過 TAPI 傳遞有關會話的其他資訊。 這項資訊不會由 TAPI 解讀，而且使用方式完全由應用程式定義。

當某個應用程式變更應用程式特定資訊時，TAPI 會以監視器或擁有者許可權在會話上傳送具有「監視」或「擁有者」許可權的所有其他應用程式，該事件表示已發生變更。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (*DwAppSpecific* member Of *lpCallInfo*) ， [**lineSetAppSpecific**](/windows/win32/api/tapi/nf-tapi-linesetappspecific)， [**LINE \_ CALLINFO**](./line-callinfo.md) message (*dwParam1* 設定為 LINECALLINFOSTATE \_ APPSPECIFIC) 。

**TAPI 3.x：** 請參閱 [**APPSPECIFIC \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 [**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)、 [**ITCallInfo：:p CALLINFO \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) (**CIL \_** 成員。

 

 
