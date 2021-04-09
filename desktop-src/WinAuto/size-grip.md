---
title: '大小手柄 (MSAA UI 元素參考) '
description: 大小底圖是視窗右下角的特殊滑鼠指標，可讓使用者按一下並拖曳大小底框來調整視窗大小。
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675623"
---
# <a name="size-grip-msaa-ui-element-reference"></a>大小手柄 (MSAA UI 元素參考) 

大小底圖是視窗右下角的特殊滑鼠指標，可讓使用者按一下並拖曳大小底框來調整視窗大小。

## <a name="iaccessible-methods"></a>IAccessible 方法

大小的底框支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>IAccessible 屬性

大小的底框支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                   | 註解                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | **Description** 屬性是「可以用來調整視窗的寬度和高度」。                                                                                   |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | **Name** 屬性為「Size box」。                                                                                                                                   |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | 包含大小底框的視窗。                                                                                                                                |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | **Role** 屬性是 [**role \_ SYSTEM \_**](object-roles.md)的底框。                                                                                  |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | **State** 屬性的值為零，表示物件為可見或 [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




