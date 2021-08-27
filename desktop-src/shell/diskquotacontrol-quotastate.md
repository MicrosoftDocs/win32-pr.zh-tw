---
description: 設定或取得磁片區磁片配額的狀態。
title: DiskQuotaControl. QuotaState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: cb2117237cd3072163447ee80895cbbb8bb854d7ad4424da83854b28ffa96196
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090628"
---
# <a name="diskquotacontrolquotastate-property"></a>DiskQuotaControl. QuotaState 屬性

設定或取得磁片區磁片配額的狀態。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a>屬性值

這個屬性可以設定為下列其中一個值。



| 狀態          | 值 | 描述               |
|----------------|-------|---------------------------|
| dqStateDisable | 0     | 磁片配額已停用。 |
| dqStateTrack   | 1     | 磁片配額已停用。 |
| dqStateEnforce | 2     | 強制執行配額限制。      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DiskQuotaControl 物件**](diskquotacontrol-object.md)
</dt> </dl>

 

 




