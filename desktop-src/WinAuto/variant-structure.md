---
title: VARIANT 結構
description: 大部分的 Microsoft Active Accessibility 函數和 IAccessible 屬性和方法都採用 VARIANT 結構作為參數。 基本上，VARIANT 結構是大型聯集的容器，它會攜帶許多類型的資料。
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063d1e17d998f3cb7d70a0a271e55f02628e7864164e00becb5a708af371e12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563546"
---
# <a name="variant-structure"></a>VARIANT 結構

大部分的 Microsoft Active Accessibility 函數和 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法都採用 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構作為參數。 基本上， **VARIANT** 結構是大型聯集的容器，它會攜帶許多類型的資料。

結構中第一個成員的值（ **vt**）描述了哪些 union 成員是有效的。 雖然 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構支援許多不同的資料類型，但是 Microsoft Active Accessibility 只會使用下列類型。



| vt 值     | 對應的值成員名稱 |
|--------------|---------------------------------|
| VT \_ I4       | **lVal**                        |
| VT \_ 分派 | **pdispVal**                    |
| VT \_ BSTR     | **bstrVal**                     |
| VT \_ 空白    | 無                            |



 

當您在 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構中接收資訊時，請檢查 **vt** 成員以找出哪些成員包含有效的資料。 同樣地，當您使用 **VARIANT** 結構傳送資訊時，請一律設定 **vt** 以反映包含資訊的聯集成員。

使用結構之前，請先呼叫 [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) 元件物件模型 (COM) 函數來將它初始化。 完成結構之後，請先將它清除，然後再呼叫 [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)來釋放包含 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)的記憶體。

 

 