---
description: CurrentCCService 屬性會設定或抓取目前的隱藏式輔助字幕服務。
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: CurrentCCService 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846476"
---
# <a name="currentccservice-property"></a>CurrentCCService 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`CurrentCCService`屬性會設定或抓取目前的隱藏式輔助字幕服務。

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>傳回值

傳回整數值，表示已啟用隱藏式輔助字幕服務的類型。

## <a name="remarks"></a>備註

這個屬性的可能值為：



| 值 | 描述                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | 沒有目前的服務。 這是預設值。                       |
| 0x1   | 真正的標題，第一個欄位。 預設服務。                       |
| 0x2   | 次要語言的標題，第二個欄位。 通常不會使用。 |



 

這是可讀寫的屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCActive**](ccactive-property.md)
</dt> </dl>

 

 



