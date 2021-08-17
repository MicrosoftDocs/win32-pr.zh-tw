---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 885a5d930892d6e202764de8e58371f02690edee6715155f34533aaa110d7080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829180"
---
# <a name="elementschildhasdifferentparent"></a>ElementsChildHasDifferentParent

## <a name="text"></a>Text

專案的子 ({0}) 具有不同于元素的父 ({1}) 

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤表示在目標專案的子系上呼叫 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 時，子系不會報告一致的父系。

![一個專案的子系的範例，其會報告不一致的父系](images/accchecker-inconsistent-parent.png)

此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。

## <a name="possible-causes"></a>可能的原因

不正確或不正確 MSAA 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




