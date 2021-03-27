---
description: 設定或取得預設配額限制。
title: DiskQuotaControl. DefaultQuotaLimit 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7d123bff-5dae-4430-be22-a822e231e43e
ms.openlocfilehash: fdfea60e58659b483a6b17c2dc89d313e3c81305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971972"
---
# <a name="diskquotacontroldefaultquotalimit-property"></a>DiskQuotaControl. DefaultQuotaLimit 屬性

設定或取得預設配額限制。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
iDefaultQuotaLimit = DiskQuotaControl.DefaultQuotaLimit
DiskQuotaControl.DefaultQuotaLimit = iDefaultQuotaLimit
```



## <a name="property-value"></a>屬性值

指定或接收新使用者之預設配額限制的 **整數** 值（以位元組為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)
</dt> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




