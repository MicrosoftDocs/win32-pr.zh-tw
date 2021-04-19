---
description: DVDAdm. SaveParentalLevel 方法會將新的預設家長監護儲存至登錄。
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: 'SaveParentalLevel 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976095"
---
# <a name="saveparentallevel-method"></a>SaveParentalLevel 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

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

 

 




