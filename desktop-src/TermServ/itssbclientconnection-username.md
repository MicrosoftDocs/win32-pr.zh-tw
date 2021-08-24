---
title: ITsSbClientConnection UserName 屬性
description: 抓取值，指出起始連接的使用者名稱。
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- UserName 屬性遠端桌面服務
- UserName 屬性遠端桌面服務，ITsSbClientConnection 介面
- ITsSbClientConnection 介面遠端桌面服務，使用者名稱屬性
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec6961e6c911b24df2e6c3adbea14b31a2ce8e5a66a9be9082357db957e646a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511328"
---
# <a name="itssbclientconnectionusername-property"></a>ITsSbClientConnection：： UserName 屬性

抓取值，指出起始連接的使用者名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>屬性值

使用者名稱的指標。 當您完成使用此字串時，請呼叫 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 函式來釋放它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

