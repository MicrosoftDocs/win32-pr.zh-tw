---
description: 設定或取得布林值，這個值會指出當使用者超過其指派的配額限制時，是否要建立系統事件記錄檔專案。
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: DiskQuotaControl. LogQuotaLimit 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f10710c5a16feb946caa78394d5e57e5d7d4884a50d45dc3e37291f40e7d283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455878"
---
# <a name="diskquotacontrollogquotalimit-property"></a>DiskQuotaControl. LogQuotaLimit 屬性

設定或取得布林值，這個值會指出當使用者超過其指派的配額限制時，是否要建立系統事件記錄檔專案。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a>屬性值

如果使用者超過配額限制，則會將此屬性設定為 **TRUE** ，否則為 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DiskQuotaControl 物件**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




