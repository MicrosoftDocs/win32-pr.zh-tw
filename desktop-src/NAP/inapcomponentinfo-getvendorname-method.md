---
title: 'INapComponentInfo GetVendorName 方法 (NapCommon .h) '
description: 是由 NAP 系統用來取得健康情況用戶端的廠商名稱。
ms.assetid: 7083b0b6-38fc-4c24-a5f7-fe0a1ebd5e88
keywords:
- GetVendorName 方法 NAP
- GetVendorName 方法 NAP，INapComponentInfo 介面
- INapComponentInfo 介面 NAP，GetVendorName 方法
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVendorName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d379df4b68ac9aaec42bbe92f02637619b7cf87e0b2cc0d2f1121dec56090baf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799693"
---
# <a name="inapcomponentinfogetvendorname-method"></a>INapComponentInfo：： GetVendorName 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapComponentInfo：： GetVendorName** 回呼方法是由 NAP 系統用來取得健康情況用戶端的廠商名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetVendorName(
  [out] MessageId *vendorName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*vendorName* \[擴展\]
</dt> <dd>

[**MessageId**](nap-datatypes.md)的指標，其中包含廠商名稱的資源識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此作業的結果傳回這些錯誤碼的其中一個。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





