---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cde3597a0922159eb035e94e08691cf9d36a07f8a1c23ec0cb25280ab961faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829527"
---
# <a name="elementhasnoname"></a>ElementHasNoName

## <a name="text"></a>Text

元素沒有名稱

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

元素沒有名稱。 例如，元素未實 accName，而且當 [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) 方法用來取得專案的 MSAA 名稱時，會傳回空字串。

這個問題會讓依賴螢幕讀取器和鍵盤進行流覽的人員遇到問題，因為專案可能會不正確地識別給使用者。

## <a name="possible-causes"></a>可能的原因

-   元素或其父系沒有名稱或標籤。
-   系統會為元素指派 [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) ，以建議專案有名稱。
-   具有焦點的元素不應獲得焦點。 例如，標籤或停用的控制項。
-   不可見的控制項已獲得焦點。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name 屬性](name-property.md)
</dt> </dl>

 

 




