---
title: 'INapSoHProcessor GetNumberOfAttributes 方法 (NapProtocol .h) '
description: 捕獲 SoH 中的屬性總數。
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- GetNumberOfAttributes 方法 NAP
- GetNumberOfAttributes 方法 NAP，INapSoHProcessor 介面
- INapSoHProcessor 介面 NAP，GetNumberOfAttributes 方法
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55805d85cc6a809a915f3998ab1b3dd218bd35a10b3b0044ff7c78130a72d97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621169"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a>INapSoHProcessor：： GetNumberOfAttributes 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSoHProcessor：： GetNumberOfAttributes** 方法會抓取 SoH 中的屬性總數。

## <a name="syntax"></a>語法


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*attributeCount* \[擴展\]
</dt> <dd>

傳回之屬性計數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>NapProtocol。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





