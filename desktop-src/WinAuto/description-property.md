---
title: '描述屬性 (Windows 協助工具功能) '
description: 物件的 Description 屬性提供有關物件視覺外觀的文字描述。
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c695ae4ed8968620776aa0786358c98372940749be4a1c4335cb89f84b373ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994228"
---
# <a name="description-property-windows-accessibility-features"></a>描述屬性 (Windows 協助工具功能) 

> [!Note]  
> **Description** 屬性通常使用不正確，且不受 Microsoft 消費者介面自動化支援。 Microsoft Active Accessibility 伺服器開發人員不應使用此屬性。 如果存取範圍和自動化案例需要詳細資訊，請使用消費者介面自動化專案和控制項模式所支援的屬性。

 

物件的 **description** 屬性提供有關物件視覺外觀的文字描述。 描述主要是用來為視力或失明使用者提供更好的內容，但也用於內容搜尋或其他應用程式。 這個屬性可協助使用者瞭解圖示或整體的視覺外觀。

藉由呼叫 [**IAccessible：： get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)，即可抓取 **Description** 屬性。

## <a name="when-to-support-the-description-property"></a>何時支援 Description 屬性

如果描述不明顯，或根據物件的 [**名稱**](name-property.md)、[**角色**](role-property.md)、[**狀態**](state-property.md)和 [**值**](value-property.md)屬性而不是多餘的，則伺服器支援 **description** 屬性。 例如，標示為「確定」的按鈕不需要額外的資訊，而顯示仙人掌圖片的按鈕則會。 這類按鈕的 [ **名稱**]、[ **角色** [**] 和 [**](help-property.md) 說明] 屬性會描述其用途，但是 **Description** 屬性會傳達較不明確的資訊;例如，「這個按鈕會顯示仙人掌的圖片」。

Microsoft Active Accessibility server 可以藉由使用 [直接注釋](direct-annotation.md)、使用 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面，或是同時執行 Microsoft Active Accessibility 和消費者介面自動化並存來處理 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息，來新增消費者介面自動化的支援。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用直接注釋](using-direct-annotation.md)
</dt> <dt>

[IAccessibleEx 介面](iaccessibleex.md)
</dt> </dl>

 

 




