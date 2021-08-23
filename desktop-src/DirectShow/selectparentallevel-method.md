---
description: SelectParentalLevel 方法會設定指定的家長層級，以供後續播放之用。
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: SelectParentalLevel 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95de7e8cbf1fb6fa284eddefa1ba07ebb9268825116fdac9c97fbd5d42bac84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684038"
---
# <a name="selectparentallevel-method"></a>SelectParentalLevel 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`SelectParentalLevel`方法會設定指定的家長層級，以供後續播放之用。

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

將家長管理層級指定為整數。 若要啟用家長管理， *iLevel* 參數的範圍必須介於1到8之間。 若要停用家長管理，請將 *iLevel* 設定為-1。

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

將目前使用者指定為字串。  (目前已忽略。 ) 

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

將目前儲存在登錄中的密碼指定為字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

這個方法會設定 MSWebDVD 物件中的存取層級，以決定使用者可播放的內容。 較高層級可以播放較低層級的內容，但較低層級無法播放較高層級的內容。 八個 DVD 家長監護管理層級的確切意義會根據國家/地區而有所不同。 在美國和加拿大地區，這些層級會對應至北美洲的「運動圖片」關聯 (MPAA) 評等類別。 預設會停用 [DVD 瀏覽器] 中的 [家長管理]。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



