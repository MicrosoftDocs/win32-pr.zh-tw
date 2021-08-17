---
description: 以文字字串形式取得使用者的目前磁片使用量。
title: DIDiskQuotaUser. QuotaUsedText 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: 40fca179fd415ca548bdb8b07c16696fde54f165bfde7d373087ec1a763e787c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050671"
---
# <a name="didiskquotauserquotausedtext-property"></a>DIDiskQuotaUser. QuotaUsedText 屬性

以文字字串形式取得使用者的目前磁片使用量。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a>屬性值

字串值，設定為目前使用中的磁碟空間量。 如果 NTFS 檔案壓縮已啟用，此屬性會反映資料在未壓縮狀態中所需的磁碟空間量。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DIDiskQuotaUser 物件**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimitText**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[**QuotaUsed**](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




