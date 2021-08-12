---
description: 步驟 8。
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: 步驟 8。 套用屬性變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2292d9f294711129b2edba50ef6fb623d767dfba4122295222d08eb1ad21dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652054"
---
# <a name="step-8-apply-property-changes"></a>步驟 8。 套用屬性變更

覆寫 [**CBasePropertyPage：： OnApplyChanges**](cbasepropertypage-onapplychanges.md) 方法，以認可任何屬性變更。 在此範例中， \_ 每當使用者滾動滑動軸時，就會更新 m lNewVal 變數。 **OnApplyChanges** 方法會將此值複製到 m \_ lVal 變數，並覆寫原始值：


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



下一 [步：步驟9。中斷屬性頁面的連接](step-9--disconnect-the-property-page.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立篩選屬性頁](creating-a-filter-property-page.md)
</dt> </dl>

 

 



