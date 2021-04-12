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
ms.openlocfilehash: fa1d62c22acf778430bfc2f9dc0e969887c7b306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509457"
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



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





