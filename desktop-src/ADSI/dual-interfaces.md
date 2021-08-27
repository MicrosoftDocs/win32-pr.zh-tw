---
title: " (ADSI) 的雙重介面"
description: 使用 COM 介面存取任何提供者 ADSI 物件上的屬性和方法。
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d1cf89ef07e573be8f59805034ff8c567e75fd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884060"
---
# <a name="dual-interfaces-adsi"></a> (ADSI) 的雙重介面

使用 COM 介面存取任何提供者 ADSI 物件上的屬性和方法。 唯讀屬性會對應至表單 **get \_ &lt; &gt; PropertyName** 的介面專案。 讀取/寫入屬性會對應至表單 **get \_ &lt; &gt; propertyname** 和 **put \_ &lt; propertyname &gt;** 的兩個介面專案。

COM 介面上的所有方法都必須：

-   傳回 HRESULT 值以表示成功或失敗。 **HRESULT** 型別會在 COM 規格中討論。
-   在對 **QueryInterface** 的呼叫中，傳回未實現介面的 **E \_ NOINTERFACE** 。
-   針對未在其他方式執行的介面傳回未完成之方法的 **E \_ >notimpl** 。
-   不支援的介面屬性 **\_ \_ \_ 不 \_ 支援傳回 E ADS 屬性** 。

為了維持與 Automation 控制器的相容性，所有參數和傳回類型都應該在 Automation VARIANT 資料類型所定義的子集內。 如需詳細資訊，請參閱平臺軟體發展工具組中的 **變異** 和 **VARIANTARG** (SDK) 。

提供者 Active Directory 物件可以公開使用 **變數** 子集中以外之資料類型的介面。 不過，Visual Basic 的 Automation 控制器無法呼叫這些介面。 大部分的 ADSI 提供者介面都是衍生自 [**idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ，而且可以當做 **idispatch** 介面指標使用。 但是， [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)、 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)和 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ADSI 介面不是衍生自 **IDispatch**。

 

 
