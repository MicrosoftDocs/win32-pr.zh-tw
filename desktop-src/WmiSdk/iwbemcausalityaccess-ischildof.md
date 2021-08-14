---
description: IsChildOf 方法會判斷要求是否為指定要求 (pId) 的子系。
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess：： IsChildOf 方法 (Wbemint .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 509508d5e1a273dc681cf3c9f645ead1037408d6ecfe5ed666186ba6e2a2c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318290"
---
# <a name="iwbemcausalityaccessischildof-method"></a>IWbemCausalityAccess：： IsChildOf 方法

**IsChildOf** 方法會判斷要求是否為指定要求 (pId) 的子系。 父要求可以有多個子要求。 每個要求都是由全域唯一識別碼 (GUID) 來識別，而且可以有父要求或可能是最上層要求。 GUID 是唯一的128位數位。

## <a name="syntax"></a>語法


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pId* \[在\]
</dt> <dd>

可唯一識別要求的 GUID 值。 例如，5b2fc63a-8af4-44cb-960c-aefdced908d6。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果指定的要求是呼叫 **IsChildOf** 方法之要求的子系，則會傳回成功。

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

 

 




