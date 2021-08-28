---
description: DVDAdm. ConfirmPassword 方法會測試指定的密碼是否符合先前儲存的密碼。
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: 'ConfirmPassword 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f14b3a40a37828bc978b5dd302a14b4f65053d982ac0da68d43284fe2ac3f3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954217"
---
# <a name="confirmpassword-method"></a>ConfirmPassword 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`DVDAdm.ConfirmPassword`方法會測試指定的密碼是否符合先前儲存的密碼。

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

將使用者的名稱指定為字串。

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

將新密碼指定為字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果指定的密碼符合現有的密碼，則傳回 true，否則傳回 false。

## <a name="remarks"></a>備註

目前，這個和所有相關的方法會忽略 *sUserName* 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>區段。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ChangePassword**](changepassword-method.md)
</dt> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 




