---
description: 取得布林值，指出目前是否正在重建磁片區的配額檔案。
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: DiskQuotaControl. QuotaFileRebuilding 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972124"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>DiskQuotaControl. QuotaFileRebuilding 屬性

取得布林值，指出目前是否正在重建磁片區的配額檔案。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>屬性值

如果正在重建配額檔案，這個屬性會設定為 **TRUE** ，否則會設為 **FALSE** 。

## <a name="remarks"></a>備註

當系統上已啟用配額，或有一或多個使用者專案標記為刪除時，就會自動重建配額檔案。

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

 

 




