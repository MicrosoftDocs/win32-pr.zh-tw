---
description: DVDAdm 方法會在登錄中儲存新的應用程式密碼。
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f5d15eef943afa019f1b1bba4e3b1412978bc5dd8f52f411c504e880428848a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999328"
---
# <a name="changepassword-method"></a>ChangePassword 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

方法會將 `DVDAdm.ChangePassword` 新的應用程式密碼儲存在登錄中。

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

將目前使用者的登入名稱指定為字串。 MSDVDAdm 物件會忽略這個參數。 請參閱＜備註＞。

</dd> <dt>

<span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*出售*
</dt> <dd>

將使用者的舊密碼指定為字串。

</dd> <dt>

<span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*
</dt> <dd>

將使用者的新密碼指定為字串。 不能是空字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

目前，這個和所有相關的方法會忽略 *sUserName* 參數。 這表示任何知道密碼的人都可以設定家長的層級。 應用程式只有一個密碼和一個家長層級。 不支援個別使用者登入名稱或多重密碼管理。 若要強制執行家長管理層級，家長應設定密碼，然後為親屬群組的年輕成員設定適當的家長監護層級。 當家長想要查看具有成人分級內容的光碟時，他們可以變更層級，然後在完成觀看時將其變更回來。 只要子系不知道密碼，他們就只能在其設定的層級或下方監看內容。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ConfirmPassword**](confirmpassword-method.md)
</dt> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 



