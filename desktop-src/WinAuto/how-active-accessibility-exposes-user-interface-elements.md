---
title: Active Accessibility 如何公開消費者介面元素
description: Microsoft Active Accessibility 為其公開的每個使用者介面元素建立 proxy 物件。
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4260788cc37aa6d4a33fcccb68a51fb61833d753c98ba4ae5dcff89f0d18cec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994158"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a>Active Accessibility 如何公開消費者介面元素

Microsoft Active Accessibility 為其公開的每個使用者介面元素建立 *proxy* 物件。 Proxy 物件可作為用戶端公用程式和 UI 元素之間的媒介。 Proxy 物件的目的是要監視 UI 元素的存留期範圍，並代表 UI 元素來執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法。 建立自訂控制項或其他自訂 UI 元素的伺服器開發人員也應該建立 proxy 物件。 如需詳細資訊，請參閱 [建立 Proxy 物件](creating-proxy-objects.md)。

當 Microsoft Active Accessibility 建立物件來公開預先定義或通用的控制項時，實際上會建立至少兩個物件：一個用於控制項，另一個用於圍繞控制項的視窗。 在大部分的情況下，這些父視窗具有 [**角色 \_ 系統 \_ 視窗**](object-roles.md)的 [role 屬性](role-property.md)，而且具有與控制項相同的 [名稱屬性](name-property.md)和視窗類別名稱。 用戶端傳達給使用者之控制項的相關資訊會包含在 Microsoft Active Accessibility 建立來公開控制項的物件中，而不是由公開控制項周圍視窗的父物件所組成。

如需詳細資訊，請參閱下列主題。

-   [篩選掉不必要的物件](screening-out-unnecessary-objects.md)
-   [提供 Name 屬性](providing-the-name-property.md)
-   [確定 UI 元素的命名正確](ensure-that-ui-elements-are-named-correctly.md)
-   [不支援的消費者介面元素](unsupported-user-interface-elements.md)

 

 




