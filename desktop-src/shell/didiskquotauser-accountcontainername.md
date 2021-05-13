---
description: 取得使用者帳戶容器的名稱。
title: DIDiskQuotaUser. AccountContainerName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: 1cb709ccc4fa0afcb56314bd097b1b0120b8b59a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843349"
---
# <a name="didiskquotauseraccountcontainername-property"></a>DIDiskQuotaUser. AccountContainerName 屬性

取得使用者帳戶容器的名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a>屬性值

設定為使用者帳戶容器名稱的字串值。

## <a name="remarks"></a>備註

針對沒有目錄服務資訊的帳戶，此屬性包含功能變數名稱。 若為具有目錄服務資訊的帳戶，此屬性會包含已移除終止物件名稱的正式名稱。

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

 

 




