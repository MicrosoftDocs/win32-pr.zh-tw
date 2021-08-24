---
description: 當 MSWebDVD 控制項的 ReadyState 屬性變更時，就會傳送 ReadyStateChange 事件。
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f73e0b5b7cd7178df31b3f6efda56e398d8cb406598355a3c49702714686af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697118"
---
# <a name="readystatechange"></a>ReadyStateChange

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`ReadyStateChange`當 MSWebDVD 控制項的 **ReadyState** 屬性變更時，就會傳送事件。

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*
</dt> <dd>

指定 [**ReadyState**](readystate-property.md) 屬性的新值。



| 值 | 描述               |
|-------|---------------------------|
| 0     | READYSTATE \_ 未初始化 |
| 1     | READYSTATE \_ 載入       |
| 2     | READYSTATE 已 \_ 載入        |
| 3     | READYSTATE \_ 互動   |
| 4     | READYSTATE \_ 完成      |



 

</dd> </dl>

 

 



