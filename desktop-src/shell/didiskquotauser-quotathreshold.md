---
description: 設定或取得使用者的警告臨界值（以位元組為單位）。
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: DIDiskQuotaUser. QuotaThreshold 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 38caa5ef5ded6ed40708314c6063fba13a74cbbe506465aed55e8504898a9307
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032786"
---
# <a name="didiskquotauserquotathreshold-property"></a>DIDiskQuotaUser. QuotaThreshold 屬性

設定或取得使用者的警告臨界值（以位元組為單位）。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a>屬性值

指定或接收使用者之警告臨界值的 **整數** 值。 如果使用者的磁片使用量超過此值，且 [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) 屬性設定為 **TRUE**，則系統會產生事件記錄檔專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




