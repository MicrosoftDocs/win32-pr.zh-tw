---
title: 動態注釋的替代方案
description: 動態注釋的替代方案
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af7582ec0fa3f317a0fabbdde0474c6a2e4d0b361062243d7518edf317477ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122428"
---
# <a name="alternatives-to-dynamic-annotation"></a>動態注釋的替代方案

還有其他方法可以提供 UI 元素的自訂 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 支援，而且在某些情況下，它們是正確的解決方案。 在動態注釋之前，這些替代技術是開發人員唯一可用的選項。 它們包括執行所有 **IAccessible** 介面和程式設計技術。

## <a name="implementing-all-of-the-iaccessible-interface"></a>執行所有 IAccessible 介面

另一個方法是執行所有 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。 自訂控制項或完全不同的 UI 元素通常需要這種方法;不過，開發和測試成本相當重要，除非真的需要，否則應該避免此情況。 如果目標是要修改單一屬性，則成本很難證明。

## <a name="programmatic-techniques"></a>程式設計技術

另一個選項是使用子類別化和包裝技術來修改針對特定屬性公開的資訊。 這是動態注釋要取代的技巧。 若要使用子類別化和包裝來覆寫單一屬性，開發人員必須執行下列步驟：

1.  子類別化 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件的 HWND。
2.  攔截 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息以取得正確的 IParam/OBJID 值。
3.  使用 [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85))函式，將 [**WM \_ GETOBJECT**](wm-getobject.md)訊息轉送至基類。 如果傳回零，則呼叫 [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject);否則，請在傳回的值上呼叫 [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) ，以取得控制項的原生 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。
4.  建立包裝函式類別，以執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 並包裝上一個步驟所傳回的 **IAccessible** 介面指標。 除了要覆寫的方法和屬性以外，此包裝函式類別會將所有方法和屬性傳送至原始 **IAccessible** 介面指標。 這牽涉到撰寫所有 **IAccessible** 介面的21個屬性和方法的轉送程式碼，而不論實際覆寫了多少。

此外，開發人員必須確認下列條件：

-   覆寫的方法或屬性只能處理所需的子識別碼，並將所有其他識別碼轉寄至原始 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。
-   只有當原始物件支援 [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) 和 [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) 介面時，換行也必須轉送這些介面。
-   參考計數必須正確處理，特別是在支援其他介面時。
-   [**IDispatch**](idispatch-interface.md) 傳回值必須正確處理，尤其是使用 [**ITypeInfo：： Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) 方法時，必須使用包裝函式介面的介面指標來呼叫，而不是原始 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的指標。

這些技術需要相當大量的工作，即使只有一或兩個屬性需要覆寫。 大部分產生的程式碼都涉及子類別化和包裝，而只有小小部分實際上提供覆寫的資訊。

不過，在某些情況下需要這些技術。 例如，如果您要進行結構變更以建立預留位置 UI 元素，則應該使用這些技術，而不是動態注釋。

## <a name="fixing-names-derived-from-labels"></a>修正衍生自標籤的名稱

某些 Microsoft Win32 通用控制項（例如編輯方塊控制項）幾乎一律會搭配 (資源檔) 中的 LTEXT 專案，或資源檔) 中群組方塊 (的群組方塊使用。 Microsoft Active Accessibility 會自動從其標籤衍生控制項的 [名稱] 屬性。 針對這類控制項，會忽略 Microsoft Visual Studio 中顯示的 [名稱] 或 [識別碼] 屬性) 的視窗文字 (，因為它通常是自動產生的，而且很少描述。例如，「IDC \_ EDIT1」。

如果未正確設計應用程式的使用者介面，Microsoft Active Accessibility 可能無法正確設定名稱。 若要與控制項相關聯，標籤或群組方塊必須緊接在定位順序中的動態控制項之前。

當資源編輯器開啟) 或直接編輯資源檔時，可以使用 [**格式**] 功能表上 Visual Studio (中的工具來變更定位順序。

下列範例顯示包含兩個標記編輯方塊之對話方塊的資源檔描述。


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



在此範例中，標籤和控制項不會以正確的定位順序列出。 如此一來，Microsoft Active Accessibility 會將名稱「姓氏」指派給第一個名稱編輯方塊，而不是「姓氏」編輯方塊的名稱。

下列範例會顯示正確的資源清單。 另外也請注意，快速鍵已在標籤中指定。


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



當控制項有輔助標籤（例如，針對標題的最小值和最大值）時，這些標籤應放置在定位順序中的控制項之後。 控制項的主要標籤必須緊接在控制項本身之前出現。

## <a name="naming-controls-without-labels"></a>在沒有標籤的情況下命名控制項

每個控制項都不一定要有可見的標籤。 不過，您仍然可以藉由新增不可見的標籤，來提供控制項的名稱。 如同往常，隱藏的標籤必須緊接在定位順序中的控制項之前。

如果您在 Microsoft Visual Studio .net 中使用資源編輯器，則可以將 Visible 屬性設為 False。 若要在編輯資源檔時使標籤隱藏 ( .rc) ，請將 [不是 WS] \_ 或 [標籤] 控制項的樣式部分新增，如下列範例所示。


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



請注意，即使標籤不可見，任何指定的快速鍵仍可運作。

 

 