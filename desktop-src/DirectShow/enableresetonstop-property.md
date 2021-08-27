---
description: EnableResetOnStop 屬性會設定或抓取值，決定當篩選圖形從停止狀態轉換時，播放將如何繼續。
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: EnableResetOnStop 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4bfda62839f55dcb4c4597fdad6654072f4dfeb2450c3bce3ed99c13a418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107858"
---
# <a name="enableresetonstop-property"></a>EnableResetOnStop 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`EnableResetOnStop`屬性會設定或抓取值，決定當篩選圖形從停止狀態轉換時，播放將如何繼續。

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a>傳回值

傳回布林值，表示 MSWebDVD 物件在篩選圖形停止之後，會在何處開始播放。

## <a name="remarks"></a>備註

這是可讀寫的屬性。

這個屬性的可能值為：，預設值為 true。



| 值 | 描述                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | DVD Navigator 將會重設，並開始從光碟的開頭播放。這是預設值 |
| false | DVD 導覽器將會從停止的地方繼續播放。                                                 |



 

 

 



