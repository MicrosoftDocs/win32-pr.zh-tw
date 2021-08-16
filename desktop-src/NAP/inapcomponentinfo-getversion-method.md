---
title: 'INapComponentInfo GetVersion 方法 (NapCommon .h) '
description: NAP 系統會使用它來取得健全狀況用戶端的版本。
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- GetVersion 方法 NAP
- GetVersion 方法 NAP，INapComponentInfo 介面
- INapComponentInfo 介面 NAP，GetVersion 方法
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e815c7d92ba9a33c07ba4d8d68c588ed0014019d0d173e0304c4a10204d4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368372"
---
# <a name="inapcomponentinfogetversion-method"></a>INapComponentInfo：： GetVersion 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapComponentInfo：： GetVersion** 回呼方法是由 NAP 系統用來取得健全狀況用戶端的版本。

## <a name="syntax"></a>語法


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*版本* \[擴展\]
</dt> <dd>

[**MessageId**](nap-datatypes.md)的指標，其中包含版本的資源識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此作業的結果傳回這些錯誤碼的其中一個。



| 傳回碼                                                                                     | 描述                                                        |
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

 

 





