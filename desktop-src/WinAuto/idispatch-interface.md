---
title: IDispatch 介面和協助工具
description: IDispatch 介面最初是設計來支援 Automation。
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641ca3e4cc18b96441aefbbc46231e3f7753a94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965648"
---
# <a name="idispatch-interface-and-accessibility"></a>IDispatch 介面和協助工具

[**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)介面最初是設計來支援 Automation。 它提供晚期繫結機制，以存取和取得物件之方法和屬性的相關資訊。 之前，伺服器開發人員必須針對其可存取的物件，同時執行 **IDispatch** 和 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面;也就是說，他們必須提供 [雙重介面](dual-interfaces--iaccessible-and-idispatch.md)。 在 Microsoft Active Accessibility 2.0 中，伺服器可以從 **IDispatch** 方法傳回 **E \_ >notimpl** ，而 Microsoft Active Accessibility 將會為其執行 **IAccessible** 介面。

除了繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)的方法之外，伺服器開發人員必須在公開的每個物件的類別定義中，執行下列方法：

-   [**GetTypeInfoCount**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) 會傳回物件的類型描述數目。 針對支援 [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)的物件，類型資訊計數一律為1。
-   [**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) 會抓取物件的可程式化介面描述。
-   [**GetIDsOfNames**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) 會將方法或屬性的名稱對應到 **DISPID**，稍後用來叫用方法或屬性。
-   [**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) 會呼叫其中一個物件的方法，或取得或設定其中一個屬性。

 

 