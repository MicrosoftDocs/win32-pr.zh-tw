---
description: CurrentCCService 屬性會設定或抓取目前的隱藏式輔助字幕服務。
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: CurrentCCService 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d836e852d1a144abb5422f71d0127eb9c37b8f333dce0723db2c2b3b1889ec50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075958"
---
# <a name="currentccservice-property"></a>CurrentCCService 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

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

 

 



