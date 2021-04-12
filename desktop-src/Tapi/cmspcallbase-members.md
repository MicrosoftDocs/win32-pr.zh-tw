---
description: 下列清單包含 CMSPCAllBase 成員。
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: CMSPCallBase 成員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192928"
---
# <a name="cmspcallbase-members"></a>CMSPCallBase 成員



| 成員類型                   | Name             | 描述                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                      | \*m \_ pFTM        | 無限制執行緒封送處理器的指標。                                                                                                                                                                                                                                                                                                          |
| CMSPAddress\*                 | \*m \_ pMSPAddress | MSP 位址物件的指標。 如果應用程式未選取任何值，則會使用它來取得預設的終端機。 它也會透過 [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)攜帶 refcount (，而不是 AddRef) ，如此一來，當通話仍在運作時，匯總的位址就不會消失，但 TAPI 3 的位址不會 AddRef'ed。 |
| MSP \_ 控制碼                   | \*m \_ htCall      | TAPI3's 呼叫的控制碼。 用來引發呼叫事件。                                                                                                                                                                                                                                                                                             |
| DWORD                         | m \_ dwMediaType   | 此呼叫之媒體類型的位元遮罩。                                                                                                                                                                                                                                                                                                          |
| CMSPArray <ITStream \*> | m \_ 資料流程       | 呼叫中的資料流程物件清單。                                                                                                                                                                                                                                                                                                           |
| CMSPCritSection               | m \_ 鎖定          | 保護資料流程清單的鎖定。                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



