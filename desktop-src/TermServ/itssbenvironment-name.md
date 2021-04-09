---
title: ITsSbEnvironment Name 屬性
description: 抓取值，指出主控目的電腦之環境的名稱。
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Name 屬性遠端桌面服務
- Name 屬性遠端桌面服務，ITsSbEnvironment 介面
- ITsSbEnvironment 介面遠端桌面服務，Name 屬性
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934118"
---
# <a name="itssbenvironmentname-property"></a>ITsSbEnvironment：： Name 屬性

抓取值，指出主控目的電腦之環境的名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>屬性值

包含環境名稱之 **BSTR** 變數的指標。

## <a name="remarks"></a>備註

這個方法會傳回遠端桌面連線代理人 (RD 連線代理人) 未直接使用的字串。 RD 連線代理人將此字串傳遞給資源外掛程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





