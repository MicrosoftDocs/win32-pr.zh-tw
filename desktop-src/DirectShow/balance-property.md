---
description: 餘額屬性會設定或抓取音訊串流輸出的喇叭餘額。
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: 餘額屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971943"
---
# <a name="balance-property"></a>餘額屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`Balance`屬性會設定或抓取音訊串流輸出的喇叭餘額。

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a>傳回值

傳回代表餘額層級的整數值。 允許的輸入範圍為-10000 到10000。 值為0會設定中性餘額，也就是左和右喇叭都有相同的波幅音訊信號。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，預設值為0，表示兩個喇叭都會收到相等的音訊信號。 如同 [**Volume**](volume-property.md) 屬性，單位會對應到 .01 分貝 (乘以-1


```
iBalance
```



這是) 的正值。 例如，值1000表示右邊通道的10個 dB 和左邊通道上的 90 dB。

 

 



