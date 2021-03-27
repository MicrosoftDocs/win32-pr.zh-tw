---
description: 取得可唯一識別使用者的識別碼。
title: DIDiskQuotaUser.ID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.ID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5cf2610e-fbd2-4e87-a323-f024283db546
ms.openlocfilehash: 8e699eeab552e8020f2875799fe3280036957733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971993"
---
# <a name="didiskquotauserid-property"></a>DIDiskQuotaUser.ID 屬性

取得可唯一識別使用者的識別碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
iID = DIDiskQuotaUser.ID
```



## <a name="property-value"></a>屬性值

**整數** 值，可在特定 [**DiskQuotaControl**](diskquotacontrol-object.md)進程內唯一識別使用者的 [**DIDiskQuotaUser**](didiskquotauser-object.md)物件。

## <a name="remarks"></a>備註

這個屬性是供不支援指標的語言（例如 Microsoft Visual Basic）使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




