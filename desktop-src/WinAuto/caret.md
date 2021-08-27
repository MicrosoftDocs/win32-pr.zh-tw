---
title: '插入號 (MSAA UI 元素參考) '
description: 插入點是視窗工作區或接受鍵盤輸入之控制項中的閃爍線、區塊或點陣圖。
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f846940a9180885da84cf8a030672b1473eab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467295"
---
# <a name="caret-msaa-ui-element-reference"></a>插入號 (MSAA UI 元素參考) 

> [!Note]  
> 本主題說明 MSAA UI 元素參考的游標。 此處未說明如何在各種 UI 架構中使用游標。 請參閱您所使用之 UI 架構的 API 參考檔。

 

插入點是視窗工作區或接受鍵盤輸入之控制項中的閃爍線、區塊或點陣圖。 指出插入文字或圖形的位置。 因為一次只有一個視窗具有鍵盤焦點，系統中只會有一個插入號。

## <a name="iaccessible-methods"></a>IAccessible 方法

插入號支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>IAccessible 屬性

插入號支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：




| 屬性 | 註解 | 
|----------|----------|
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a> | <strong>ChildCount</strong>屬性為零。 | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a> | <strong>Name</strong>屬性為 "Edit"。 | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a> | <strong>Role</strong>屬性為<strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>。 | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a> | <strong>State</strong>屬性可能的值包括：<ul><li>零，表示插入號是可見的</li><li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li></ul> | 




 

## <a name="notes"></a>備註

-   與其他 UI 元素不同的是，插入號物件沒有相關聯的視窗控制碼。 若要取得插入號物件的存取權，用戶端必須設定 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) ，並等候插入號物件產生事件。
-   Riched20.dll (所提供的 rich edit 控制項中的插入號物件，在 Windows 98) 的 Microsoft WordPad 等文字編輯器中，在文字選取期間變更其位置時，不會傳送任何[WinEvents](winevents-infrastructure.md) 。 當使用者按下 SHIFT 和方向鍵選取文字時，插入號物件不會觸發 [**事件 \_ 物件 \_ LOCATIONCHANGE**](event-constants.md) new-winevent。 同樣地，當您透過 rich edit 訊息以程式設計方式設定選取專案時，插入號物件不會傳送任何事件來指出其新位置。

    使用 Riched20.dll 的所有應用程式都會出現此問題。 使用較舊版本之 rich edit 控制項的應用程式，會根據選取專案正確地傳送事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




