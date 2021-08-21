---
title: 'INapComponentInfo GetIcon 方法 (NapCommon .h) '
description: NAP 系統會使用它來取得健全狀況用戶端的圖示。
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- GetIcon 方法 NAP
- GetIcon 方法 NAP，INapComponentInfo 介面
- INapComponentInfo 介面 NAP，GetIcon 方法
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1711c186d107418d95ccaf19e2a1440b0cecfc0e32fc8c425754d2d9fc19a9d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134432"
---
# <a name="inapcomponentinfogeticon-method"></a>INapComponentInfo：： GetIcon 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapComponentInfo：： GetIcon** 回呼方法是由 NAP 系統用來取得健全狀況用戶端的圖示。

## <a name="syntax"></a>語法


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dllFilePath* \[擴展\]
</dt> <dd>

指向 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) 指標的指標，用來傳回包含圖示之 DLL 的檔案路徑。

</dd> <dt>

*iconResourceId* \[擴展\]
</dt> <dd>

值的指標，用來傳回要使用之圖示的資源識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此作業的結果傳回這些錯誤碼的其中一個。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

您應該根據呼叫端的語言識別項來當地語系化圖示。

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

 

 





