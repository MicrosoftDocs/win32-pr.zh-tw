---
description: 釋放 IeAxiService 介面使用的資源。
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: IeAxiService：：清除方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: de0413c39a4abf47a24913f347ceed0158d0b51aa4e1da0b3005cace1326b53f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908378"
---
# <a name="ieaxiservicecleanup-method"></a>IeAxiService：：清除方法

**清除** 方法會釋放 [**IeAxiService**](ieaxiservice.md)介面所使用的資源。

## <a name="syntax"></a>語法


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](/windows/desktop/SecCrypto/common-hresult-values)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windowsvista Business、Windows vista Enterprise、Windows vista 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService 定義為 E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

