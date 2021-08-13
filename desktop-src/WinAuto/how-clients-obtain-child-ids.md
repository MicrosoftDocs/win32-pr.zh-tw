---
title: 用戶端如何取得子識別碼
description: 用戶端如何取得子識別碼
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a12dc3f40c2aaa776c1fa8e61713c52ffbdcde554c9f6a1cbca7093998780c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388598"
---
# <a name="how-clients-obtain-child-ids"></a>用戶端如何取得子識別碼

用戶端開發人員可以利用下列方式取得物件的子識別碼：

-   呼叫 [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)。 此函數會抓取 [**VARIANT**](variant-structure.md) 結構的陣列。
-   查詢物件以查看它是否支援 [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) 介面。 如果有的話，請使用 [**IEnumVARIANT：： Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) 取得子識別碼。
-   藉由呼叫父物件的 [**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) 方法來收集子識別碼。

> [!Note]  
> 用戶端必須負責釋放用於 [**變異**](variant-structure.md) 結構的記憶體。 用戶端也必須在傳回的任何 [**IDispatch**](idispatch-interface.md)介面上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 。

 

 

 