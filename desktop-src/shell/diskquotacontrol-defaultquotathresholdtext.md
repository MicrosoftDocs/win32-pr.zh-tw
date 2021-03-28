---
description: 取得預設配額閾值做為文字字串。
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: DiskQuotaControl. DefaultQuotaThresholdText 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112324"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a>DiskQuotaControl. DefaultQuotaThresholdText 屬性

取得預設配額閾值做為文字字串。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a>屬性值

包含磁片區預設配額閾值的字串值。

## <a name="remarks"></a>備註

預設配額閾值會自動套用到磁片區的新使用者。 如果使用者的磁片使用量超過此值，且 [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) 屬性設定為 **TRUE**，則系統會產生事件記錄檔專案。 例如，如果預設閾值為 10.0 MB，則屬性的值為 "10.0 MB"。 如果磁片區沒有預設閾值，屬性會設定為「沒有限制」或當地語系化的對等專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




