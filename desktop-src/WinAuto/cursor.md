---
title: 'Cursor (MSAA UI 元素參考) '
description: 游標是螢幕上的位置，由指標裝置（例如，滑鼠、畫筆或軌跡球）控制的小型圖片。 當使用者移動指標裝置時，Windows 作業系統會移動游標。
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52140da712c5fb889a12c466a34f8587c7291664fd774ac71a3f877031ce30b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830077"
---
# <a name="cursor-msaa-ui-element-reference"></a>Cursor (MSAA UI 元素參考) 

> [!Note]  
> 本主題說明 MSAA UI 專案參考之用途的資料指標。 此處未說明如何在各種 UI 架構中使用資料指標。 請參閱您所使用之 UI 架構的 API 參考檔。

 

游標是螢幕上的位置，由指標裝置（例如，滑鼠、畫筆或軌跡球）控制的小型圖片。 當使用者移動指標裝置時，Windows 作業系統會移動游標。

## <a name="iaccessible-methods"></a>IAccessible 方法

資料指標支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>IAccessible 屬性

資料指標支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：

-   [**get \_ AccChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)- **ChildCount** 屬性為零。
-   [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)-開發人員可以建立自訂資料指標，或使用其資料指標識別碼所識別的預先定義資料指標。 游標的 **名稱** 屬性取決於其圖形，而且是下列其中一項： 

    | 游標圖形     | 名稱              |
    |------------------|-------------------|
    | 自訂資料指標    | 不明         |
    | IDC \_ 箭號       | "Normal"          |
    | IDC \_ I 字形狀       | 編輯            |
    | IDC \_ 等候        | 繼續            |
    | IDC \_ 交叉       | 示意圖         |
    | IDC \_ UPARROW     | 創建              |
    | IDC \_ SIZENWSE    | 「NWSE 大小」       |
    | IDC \_ SIZENESW    | 「NESW 大小」       |
    | IDC \_ SIZEWE      | 「水準大小」 |
    | IDC \_ SIZENS      | 「垂直大小」   |
    | IDC \_ SIZEALL     | 刪除            |
    | IDC \_ 否          | 禁止       |
    | IDC \_ APPSTARTING | 「應用程式啟動」       |
    | IDC \_ 說明        | 連線            |

    

     

-   [**取得 \_ AccRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)- **role** 屬性是 [**role 系統 \_ 資料 \_ 指標**](object-roles.md)。
-   [**get \_ AccState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)- **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：

    [**狀態 \_系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 浮動**](object-state-constants.md)

## <a name="notes"></a>備註

-   與其他 UI 元素不同的是，資料指標物件沒有相關聯的視窗控制碼。 若要取得資料指標物件的存取權，用戶端必須設定 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) ，並等候資料指標物件產生事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




