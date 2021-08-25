---
description: 設定或取得預設配額閾值。
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: DiskQuotaControl. DefaultQuotaThreshold 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 46d44f2e2df24c5ee1cbf646643810e09d007eb15ba6c9a352eb492dfb104752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943108"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a>DiskQuotaControl. DefaultQuotaThreshold 屬性

設定或取得預設配額閾值。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a>屬性值

設定為新使用者預設警告臨界值的 **整數** 值（以位元組為單位）。

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

 

 




