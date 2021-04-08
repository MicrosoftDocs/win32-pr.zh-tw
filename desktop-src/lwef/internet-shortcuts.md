---
title: 網際網路快速鍵
description: 網際網路快捷方式物件是用來建立網際網路網站的桌面快捷方式。
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- 網際網路快捷方式物件
- WebBrowser 控制項
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14bc2ed58f75522e59b9008ded7b0f1416a21fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023441"
---
# <a name="internet-shortcuts"></a>網際網路快速鍵

網際網路快捷方式物件是用來建立網際網路網站的桌面快捷方式。 就像檔案系統中專案的快捷方式一樣，網際網路快速鍵會以圖示形式出現在桌面上。 當使用者按一下圖示時，就會啟動瀏覽器，並顯示與快捷方式相關聯的網站。

討論下列主題。

-   [建立網際網路快捷方式](#creating-internet-shortcuts)
    -   [從 WebBrowser 控制項建立網際網路快捷方式](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [從 URL 建立網際網路快捷方式](#creating-an-internet-shortcut-from-a-url)
-   [存取屬性儲存體](#accessing-property-storage)
-   [介面](#interfaces)
    -   [OLE 介面](#ole-interfaces)
    -   [Shell 介面](#shell-interfaces)
-   [函數](#functions)
    -   [網際網路快速鍵公用程式函式](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a>建立網際網路快捷方式

您可以使用 WebBrowser 控制項或頁面的 URL 來建立網際網路快捷方式。

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a>從 WebBrowser 控制項建立網際網路快捷方式

如果您的應用程式裝載了 WebBrowser 控制項，則可以使用網際網路快捷方式物件，以下列方式建立快捷方式。

1.  使用 (clsid) clsid InternetShortcut 的類別識別碼，建立具有 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的網際網路快捷方式物件的實例 \_ 。
2.  使用[IObjectWithSite：： SetSite](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite)，將 WebBrowser 的[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面指標傳遞至網際網路快捷方式物件。
3.  當您想要建立 WebBrowser 控制項所要查看之頁面的快捷方式時，請呼叫網際網路快捷方式物件的 [IPersistFile：： Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 方法。

將會在 [IPersistFile：： Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)中指定的位置建立快捷方式。 這個位置可讓 WebBrowser 控制項還原其狀態，包括將正確檔載入至框架的工作。

### <a name="creating-an-internet-shortcut-from-a-url"></a>從 URL 建立網際網路快捷方式

如果您有想要連結之頁面的 URL，您也可以建立網際網路快捷方式。

1.  使用 CLSID 的 clsid InternetShortcut，建立具有 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的網際網路快捷方式物件的實例 \_ 。
2.  您可以使用 [IUniformResourceLocator：： SetURL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) 方法來設定快速鍵中的 URL。
3.  使用 [IPersistFile：： save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 方法，將快捷方式檔案儲存至所需的位置。

## <a name="accessing-property-storage"></a>存取屬性儲存體

網際網路快捷方式物件包含數個屬性，您可以使用下列程式，透過物件的 [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) 介面來存取這些屬性。

1.  藉由呼叫具有 IID IPropertySetStorage 的[QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得[IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)介面 \_ 。
2.  藉由呼叫 [IPropertySetStorage：： Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) with FMTID \_ Intshcut 或 FMTID \_ InternetSite 來取得 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) 介面，以存取網際網路快速鍵屬性儲存集。
3.  藉由傳遞適當的屬性識別碼，以 [IPropertyStorage：： ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) 讀取屬性儲存體資訊。

使用 [4.70 版或更高版本](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85))的 Shell32.dll，您也可以藉由呼叫 [**IShellFolder：： BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) ，並將 *pidl* 參數設定為來取出 [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)介面。URL 檔案和 *riid* 參數設定為 IID \_ IPropertySetStorage。

下列屬性識別碼可針對 FMTID \_ Intshcut 要求。



| PROPID               | Variant 類型 | Description                                 |
|----------------------|--------------|---------------------------------------------|
| PID \_ 是 \_ URL         | VT \_ LPWSTR   | 快速鍵導向的 URL             |
| PID \_ 為 \_ NAME        | VT \_ LPWSTR   | 網際網路快捷方式的名稱               |
| PID \_ 為 \_ >\DREPLAYCLIENT\WORKINGDIR  | VT \_ LPWSTR   | 快速鍵的工作目錄          |
| PID \_ 是 \_ 熱鍵      | VT \_ UI2      | 快速鍵的熱鍵                     |
| PID \_ 為 \_ SHOWCMD     | VT \_ I4       | 顯示快捷方式的命令                   |
| PID \_ 為 \_ >ICONINDEX   | VT \_ I4       | 圖示的索引                           |
| PID \_ 為 \_ ICONFILE    | VT \_ LPWSTR   | 包含圖示的檔案                 |
| PID \_ 為 \_ >WHATSNEW.CASTING    | VT \_ LPWSTR   | 新功能文字                             |
| PID \_ 是 \_ 作者      | VT \_ LPWSTR   | 作者                                      |
| PID \_ 為 \_ 描述 | VT \_ LPWSTR   | 網站的描述文字                    |
| PID \_ 為 \_ 批註     | VT \_ LPWSTR   | 使用者批註批註                      |
| PID \_ 已 \_ 漫遊      | VT \_ BOOL     | 當快捷方式第一次漫遊時為 True |



 

下列屬性識別碼可針對 FMTID \_ InternetSite 要求。



| PROPID                     | Variant 類型 | Description                                       |
|----------------------------|--------------|---------------------------------------------------|
| PID \_ INTSITE \_ >WHATSNEW.CASTING     | VT \_ LPWSTR   | 新功能文字                                   |
| PID \_ INTSITE \_ 作者       | VT \_ LPWSTR   | 作者                                            |
| PID \_ INTSITE \_ LASTVISIT    | VT \_ FILETIME | 上次造訪時間網站                        |
| PID \_ INTSITE \_ LASTMOD      | VT \_ FILETIME | 上次修改時間網站                       |
| PID \_ INTSITE \_ VISITCOUNT   | VT \_ UI4      | 使用者造訪的次數                  |
| PID \_ INTSITE \_ 描述  | VT \_ LPWSTR   | 網站的描述文字                          |
| PID \_ INTSITE \_ 批註      | VT \_ LPWSTR   | 使用者批註批註                            |
| PID \_ INTSITE \_ 旗標        | VT \_ UI4      | 表示使用 PIDISF \_ 旗標 (請參閱下文)        |
| PID \_ INTSITE \_ CONTENTLEN   | N/A          | 目前不支援                           |
| PID \_ INTSITE \_ CONTENTCODE  | N/A          | 目前不支援                           |
| PID \_ INTSITE \_ 遞迴      | N/A          | 目前不支援                           |
| PID \_ INTSITE \_ 監看        | N/A          | 目前不支援                           |
| PID \_ INTSITE \_ 訂用帳戶 | VT \_ UI8      | 訂用帳戶管理員的 SUBSCRIPTIONCOOKIE 值 |
| PID \_ INTSITE \_ URL          | VT \_ LPWSTR   | 快速鍵導向的 URL                   |
| PID \_ INTSITE \_ 標題        | VT \_ LPWSTR   | 標題                                             |
| PID \_ INTSITE \_ 字碼頁     | VT \_ UI4      | 檔的字碼頁                          |
| PID \_ INTSITE \_ 追蹤     | N/A          | 目前不支援                           |
| PID \_ INTSITE \_ >ICONINDEX    | VT \_ I4       | 圖示的索引                                 |
| PID \_ INTSITE \_ ICONFILE     | VT \_ LPWSTR   | 包含圖示的檔案                       |
| 已 \_ 漫遊的 PID INTSITE \_       | VT \_ UI4      | 因為漫遊而新增了專案                |



 

以下是網際網路網站旗標。



| 旗標                    | 描述                                |
|-------------------------|--------------------------------------------|
| PIDISF \_ RECENTLYCHANGED | 指出最近已變更網站 |
| PIDISF \_ CACHEDSTICKY    | 目前不支援                    |
| PIDISF \_ CACHEIMAGES     | 目前不支援                    |
| PIDISF \_ FOLLOWALLLINKS  | 目前不支援                    |



 

以下是網際網路漫遊歷程記錄所使用的值。



| 已漫遊的 PID \_ INTSITE 值 \_         | Description                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 值未設定或 PIDISR \_ \_ 為最 \_ 新狀態 | 漫遊未修改此快取專案。                                                                                                                       |
| PIDISR \_ 需要 \_ 新增                    | 漫遊已將此快取專案新增至快取。 \_ \_ 完成專案的處理之後，將 PIDISR 設定為最新狀態 \_ 。                                                   |
| PIDISR \_ 需要 \_ 更新                 | 這個快取專案已經存在於本機電腦上，但已透過漫遊進行更新。 \_ \_ 完成專案的處理之後，將 PIDISR 設定為最新狀態 \_ 。                 |
| PIDISR \_ 需要 \_ 刪除                 | 漫遊偵測到應該刪除此快取專案。 例如，使用者可能已清除其瀏覽器歷程記錄。 使用 DeleteUrlCacheEntry 刪除專案。 |



 

## <a name="interfaces"></a>介面

網際網路快捷方式物件會公開多個介面。

### <a name="ole-interfaces"></a>OLE 介面

-   [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [IOleCommandTarget](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
-   [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)
-   [IObjectWithSite](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)

### <a name="shell-interfaces"></a>Shell 介面

-   [**ICoNtextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)
-   [**IExtractIcon**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona)
-   [**INewShortcutHook**](/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka)
-   [**IShellExtInit**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit)
-   [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)
-   [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
-   [**IQueryInfo**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo)

## <a name="functions"></a>函式

有幾個公用程式函式可用於網際網路快捷方式物件。

### <a name="internet-shortcut-utility-functions"></a>網際網路快速鍵公用程式函式

-   [**InetIsOffline**](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [**MIMEAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [**TranslateURL**](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [**URLAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 