---
description: GetRequestId 方法會傳回要求 (GUID) 值的全域唯一識別碼。 GUID 是唯一的128位數位。
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess：： GetRequestId 方法 (Wbemint .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 20b7a70358364aed281015a86498d0a1a2af76347773d7bedf23bbd5c69861b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818866"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a>IWbemCausalityAccess：： GetRequestId 方法

**GetRequestId** 方法會傳回要求 (GUID) 值的全域唯一識別碼。 GUID 是唯一的128位數位。

## <a name="syntax"></a>語法


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pId* \[擴展\]
</dt> <dd>

可唯一識別要求的 GUID 值。 例如，5b2fc63a-8af4-44cb-960c-aefdced908d6。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Wbemint。h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWbemCausalityAccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 




