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
ms.openlocfilehash: 7ce336c84d086c4e4be369278a77e40e59474bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847789"
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

 

 




