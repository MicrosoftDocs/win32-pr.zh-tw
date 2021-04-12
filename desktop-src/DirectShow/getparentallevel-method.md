---
description: DVDAdm. GetParentalLevel 方法會抓取上次儲存至登錄的父層級。
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: GetParentalLevel 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385565"
---
# <a name="getparentallevel-method"></a>GetParentalLevel 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`DVDAdm.GetParentalLevel`方法會抓取上次儲存至登錄的家長監護層級。

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a>傳回值

傳回從1到8的整數，表示預設的父層級。

## <a name="remarks"></a>備註

這個方法所抓取的父層級不一定是目前儲存在 MSWebDVD 控制項中的相同層級;若要取得目前儲存在控制項中的層級，請呼叫 [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) 方法。 -1 的值表示已停用家長管理。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSDVDAdm 物件](msdvdadm-object.md)
</dt> </dl>

 

 



