---
description: 當 MSWebDVD 控制項的 ReadyState 屬性變更時，就會傳送 ReadyStateChange 事件。
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510173"
---
# <a name="readystatechange"></a>ReadyStateChange

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

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

 

 



