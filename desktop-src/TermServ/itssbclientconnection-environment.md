---
title: ITsSbClientConnection 環境屬性
description: 抓取物件，此物件包含裝載目的電腦之環境的相關資訊。
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- 環境屬性遠端桌面服務
- 環境屬性遠端桌面服務，ITsSbClientConnection 介面
- ITsSbClientConnection 介面遠端桌面服務，環境屬性
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cc1c3c8a13a21135ee834950e8c0a60d2794cd4b1edb618e5e67c0744fe3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072208"
---
# <a name="itssbclientconnectionenvironment-property"></a>ITsSbClientConnection：：環境屬性

抓取物件，此物件包含裝載目的電腦之環境的相關資訊。 例如，在虛擬桌面案例中，此物件會包含裝載虛擬機器之電腦的相關資訊。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a>屬性值

指向 [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) 環境物件指標的指標。

## <a name="error-codes"></a>錯誤碼

如果方法成功，它會傳回 **S \_ OK**。 否則，它會傳回表示錯誤的 **HRESULT** 值。 可能的值包括（但不限於）下列清單中的值。

<dl> <dt>

E \_ 指標
</dt> <dd>

找不到環境。

</dd> </dl>

## <a name="remarks"></a>備註

協調流程外掛程式可以呼叫這個方法，以抓取目標虛擬機器的環境資訊。

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

 

 





