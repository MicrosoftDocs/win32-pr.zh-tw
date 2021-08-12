---
title: 'INapComponentInfo ConvertErrorCodeToMessageId 方法 (NapCommon .h) '
description: NAP 系統會使用它來要求健康情況用戶端將 HRESULT 錯誤碼轉換成訊息識別碼。
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- ConvertErrorCodeToMessageId 方法 NAP
- ConvertErrorCodeToMessageId 方法 NAP，INapComponentInfo 介面
- INapComponentInfo 介面 NAP，ConvertErrorCodeToMessageId 方法
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c670585674713d114f6505a0c3211d599663545f6b06a40669f7fba8b7eddf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621727"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a>INapComponentInfo：： ConvertErrorCodeToMessageId 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapComponentInfo：： ConvertErrorCodeToMessageId** 回呼方法是由 NAP 系統用來要求健康情況用戶端將 HRESULT 錯誤碼轉換成訊息識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*errorCode* \[在\]
</dt> <dd>

從 NAP 系統轉換成 **MessageId** 的 [**錯誤碼**](nap-error-constants.md)。

</dd> <dt>

*msgId* \[擴展\]
</dt> <dd>

[**MessageId**](nap-datatypes.md)的指標，其中包含對應之當地語系化字串的資源識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此作業的結果傳回這些錯誤碼的其中一個。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

NAP 系統會使用傳回的 **MessageId** 來取出當地語系化的字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





