---
description: 取得布林值，這個值會指出磁片區的配額檔案是否已完成。
ms.assetid: 25eb7df4-ba6c-4c6c-b611-e32b673a4d18
title: DiskQuotaControl. QuotaFileIncomplete 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileIncomplete
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9556b6a2cca3aa2ab040a3cfb81b29c8578d4d544c8d51af6ad70a0d601d63cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032776"
---
# <a name="diskquotacontrolquotafileincomplete-property"></a>DiskQuotaControl. QuotaFileIncomplete 屬性

取得布林值，這個值會指出磁片區的配額檔案是否已完成。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
bQuotaFileIncomplete = DiskQuotaControl.QuotaFileIncomplete
```



## <a name="property-value"></a>屬性值

如果配額檔案不完整，這個屬性會設定為 **TRUE** ，否則會設為 **FALSE** 。

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

 

 




