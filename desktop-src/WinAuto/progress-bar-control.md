---
title: '進度列控制項 (MSAA UI 元素參考) '
description: 進度列控制項指出冗長作業的進度，例如從網際網路下載檔案。 通常進度會以從零 (0) 到 100 (100) 的百分比表示。
ms.assetid: 9165d00e-b3f3-41cd-812c-cd39313460fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9bbd9a648ee1c4d4f112577c8e41a5983f69038
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183874"
---
# <a name="progress-bar-control-msaa-ui-element-reference"></a>進度列控制項 (MSAA UI 元素參考) 

> [!Note]  
> 本主題說明 MSAA UI 元素參考的 **進度列控制項** 物件。 此處未說明如何在各種 UI 架構中建立 **進度列控制項** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

進度列控制項指出冗長作業的進度，例如從網際網路下載檔案。 通常進度會以從零 (0) 到 100 (100) 的百分比表示。

進度列控制項的視窗類別名稱是進度 \_ 類別，在 Commctrl 中定義為「msctls \_ 進度」。

## <a name="iaccessible-methods"></a>IAccessible 方法

進度列控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

進度列控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | **ChildCount** 屬性為零。                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | **KeyboardShortcut** 屬性是進度列的存取金鑰，在進度列的標籤文字中是加上底線的字元。 傳回的字串包含附加至字串 "Alt +" 的存取金鑰字元。                                                                                                                                                                                                                                 |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | **Name** 屬性是靜態文字控制項中的文字，會標記進度列。                                                                                                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。                                                                                                                                                                                                                                                              |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性為 [**role \_ SYSTEM \_ PROGRESSBAR**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                      |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)<br/> |
| [**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | **值** 屬性是從 "0%" 到 "100%" 的字串，可描述進度。                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





