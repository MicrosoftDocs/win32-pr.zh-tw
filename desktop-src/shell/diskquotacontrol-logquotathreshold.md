---
description: 設定或取得布林值，這個值會指出當使用者超過其指派的配額閾值時，是否要建立系統事件記錄檔專案。
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: DiskQuotaControl. LogQuotaThreshold 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bb2a2073a791fcbb8e5bb6db83480f0fcea52b35e0380c20be730265d5bb34ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090638"
---
# <a name="diskquotacontrollogquotathreshold-property"></a>DiskQuotaControl. LogQuotaThreshold 屬性

設定或取得布林值，這個值會指出當使用者超過其指派的配額閾值時，是否要建立系統事件記錄檔專案。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a>屬性值

如果使用者超過其配額警告臨界值，則此屬性會設定為 TRUE，否則會設為 **TRUE** ，否則為 **FALSE** 。

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

[**DiskQuotaControl 物件**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




