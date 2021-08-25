---
description: AcceptParentalLevelChange 方法會接受或拒絕新的暫時家長管理層級。
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: AcceptParentalLevelChange 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4742622ce9a2c65cdce660a8bae7fab6f84171d6bd61cdf88475c2bcd788c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873588"
---
# <a name="acceptparentallevelchange-method"></a>AcceptParentalLevelChange 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

AcceptParentalLevelChange 方法會接受或拒絕新的暫時家長管理層級。

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*
</dt> <dd>

將新的父層級指定為布林值。



| 值 | 描述                               |
|-------|-------------------------------------------|
| true  | 接受新的家長管理層級。 |
| false | 拒絕新的家長管理層級。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

呼叫這個方法以回應 [EC \_ DVD 家長監護] \_ \_ \_ 變更事件通知，以指定 DVD 導覽器是否應該播放具有新家長監護的內容，或在新的層級遭到拒絕時，將分支新增到光碟指定的位置。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[強制執行家長管理層級](enforcing-parental-management-levels.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



