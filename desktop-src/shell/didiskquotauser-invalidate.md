---
description: 清除物件的快取使用者資訊。
title: DIDiskQuotaUser 方法無效
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: c0c7235031b20749a1aecd647c49a66fb3af1d108f7b09aaf7f02166dba9428e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050728"
---
# <a name="didiskquotauserinvalidate-method"></a>DIDiskQuotaUser 方法無效

清除物件的快取使用者資訊。

## <a name="syntax"></a>語法


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會清除儲存在物件快取中的使用者資訊。 下次對配額相關資訊提出要求時，物件會從 NTFS 磁片區抓取資訊並重新整理快取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DIDiskQuotaUser 物件**](didiskquotauser-object.md)
</dt> </dl>

 

 




