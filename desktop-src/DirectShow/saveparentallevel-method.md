---
description: DVDAdm. SaveParentalLevel 方法會將新的預設家長監護儲存至登錄。
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: 'SaveParentalLevel 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e372563a6f5a1fe8e893efeb86633baa6a03a7b72c79e3f05a3ec7372bec2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315948"
---
# <a name="saveparentallevel-method"></a>SaveParentalLevel 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

**DVDAdm. SaveParentalLevel** 方法會將新的預設家長監護儲存至登錄。

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

將家長層級指定為從1到8的 anInteger 值。

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

將使用者名稱指定為字串。  (目前已忽略。 ) 

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

將密碼指定為字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

此方法可讓知道目前密碼的使用者將新的家長監護設定儲存至登錄。 如同 **MSDVDAdm** 的所有方法，這個方法不會影響播放程式中目前的層級;它只會變更登錄設定，如此 MSWebDVD 物件下次啟動時，就會以新的層級開啟。 指定-1 可停用家長管理。 若要在播放玩家變更家長監護，請呼叫 [**SelectParentalLevel**](selectparentallevel-method.md)，而不會變更登錄設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>區段。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 




