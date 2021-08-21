---
title: ITsSbSession 網域屬性
description: 抓取使用者的功能變數名稱。
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- 網域屬性遠端桌面服務
- 網域屬性遠端桌面服務、ITsSbSession 介面
- ITsSbSession 介面遠端桌面服務，網域屬性
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52854f719830933c96bc130dbec4f0b15f1264344396382ad59099d4c37cf02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128303"
---
# <a name="itssbsessiondomain-property"></a>ITsSbSession：:D omain 屬性

抓取使用者的功能變數名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a>屬性值

**BSTR** 變數的指標，此變數會接收使用者的功能變數名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





