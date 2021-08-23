---
title: '標題控制項 (MSAA UI 元素參考) '
description: 標題控制項會在資訊的資料行頂端顯示標題，並讓使用者按一下標題來排序資訊。 Windows當選取 [詳細資料] 視圖時，Explorer 會使用標題控制項。
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c378bb0244e94f4cb95c8b2ba90512d2b17542bdef7428197ee58479dbfde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994178"
---
# <a name="header-control-msaa-ui-element-reference"></a>標題控制項 (MSAA UI 元素參考) 

> [!Note]  
> 本主題將描述用於 MSAA UI 元素參考的 **標題控制項** 物件。 此處未說明如何在各種 UI 架構中建立 **標題控制項** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

標題控制項會在資訊的資料行頂端顯示標題，並讓使用者按一下標題來排序資訊。 Windows當選取 [詳細資料] 視圖時，Explorer 會使用標題控制項。

標題控制項的視窗類別名稱是 WC \_ 標頭，其定義為 Commctrl 中的 "SysHeader32"。

## <a name="iaccessible-methods"></a>IAccessible 方法

標題控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：



| 方法                                                                    | 註解                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | 這個方法會藉由按一下標頭來執行預設動作。 |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>IAccessible 屬性

標題控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                       | 註解                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | **ChildCount** 屬性為零。                                                                                                                                                                                                   |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | **DefaultAction** 屬性為 "Click"。                                                                                                                                                                                             |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | **名稱** 屬性與資料行標題的名稱相同。                                                                                                                                                                    |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | **父** 屬性是視窗 ([**角色 \_ 系統 \_ 清單**](object-roles.md)) ，它會圍繞控制項，而且具有與控制項相同的視窗類別名稱。                                                      |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | **Role** 屬性為 [**role \_ SYSTEM \_ COLUMNHEADER**](object-roles.md)。                                                                                                                                  |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | **State** 屬性的值一律為 [**state \_ system \_ READONLY**](object-state-constants.md) ，也可以包含 [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




