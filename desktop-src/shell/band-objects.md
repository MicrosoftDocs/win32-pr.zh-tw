---
description: Microsoft Internet Explorer 4.0 引進了 Explorer 列，以提供與瀏覽器窗格連續的顯示區域。
title: 建立自訂瀏覽器列、工具區和桌上區
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9a57cc5bc8afa3e973c6d4d99b8bcee186287a6c9278407b900f84500d7d0e51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118461739"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a>建立自訂的瀏覽器列、工具區和書桌區

Microsoft Internet Explorer 4.0 引進了 Explorer 列，以提供與瀏覽器窗格連續的顯示區域。 基本上它是 Windows Internet Explorer 視窗中的子視窗，可用來顯示資訊，並以許多相同的方式與使用者互動。 Explorer 橫條最常顯示為 [瀏覽器] 窗格左側的垂直窗格。 不過，您也可以在瀏覽器窗格下方，以水準方式顯示 Explorer 列。

![顯示垂直和水準瀏覽器列的螢幕擷取畫面。](images/expl1.jpg)

Explorer 列有各式各樣的可能用途。 使用者可以透過數種不同的方式來選取想要查看的選項，包括從 [ **View** ] 功能表的 [ **Explorer** ] 列子功能表選取它，或按一下工具列按鈕。 Internet Explorer 提供數個標準 Explorer 列，包括我的最愛和搜尋。

您可以自訂 Internet Explorer 的其中一種方式是加入自訂的瀏覽器列。 當執行並註冊時，它會加入至 [ **View** ] 功能表的 [ **Explorer Bar** ] 功能表中。 當使用者選取此選項時，就可以使用 Explorer 列的顯示區域來顯示資訊，並以一般視窗的相同方式來進行使用者輸入。

![explorer 列的螢幕擷取畫面](images/expl2.jpg)

若要建立自訂的瀏覽器列，您必須先執行並註冊一個 *帶線物件*。 在版本4.71 中引進了頻外物件，並提供類似于一般 windows 的功能。 不過，因為它們是元件物件模型 (COM) 物件，並由 Internet Explorer 或 Shell 所包含，所以會以不同的方式來執行。 簡單的帶狀物件是用來建立第一個圖形中所顯示的範例瀏覽器列。 將在稍後的章節中詳細討論垂直 Explorer Bar 範例的執行。

## <a name="tool-bands"></a>工具區

「*工具區*」是一種以 Microsoft Internet Explorer 5 引進的寬線物件，可支援 Windows 的選項按鈕功能。 Internet Explorer 的工具列實際上是包含數個[工具列控制項](../controls/toolbar-control-reference.md)的[Rebar 控制項](../controls/rebar-controls.md)。 藉由建立工具區，您就可以在該 Rebar 控制項中加入一個頻外。 不過，如同 Explorer 橫條，工具區是一般用途的視窗。

![工具區段的螢幕擷取畫面](images/toolband1.jpg)

使用者可以從 [ **View** ] 功能表的 [**工具列**] 子功能表，或是以滑鼠右鍵按一下工具列區域所顯示的快捷方式功能表中選取工具列來顯示工具列。

## <a name="desk-bands"></a>書桌區

頻外物件也可以用來建立 *桌面* 群組。 雖然其基本的執行類似于 Explorer 列，但服務中心區與 Internet Explorer 無關。 桌上型電腦區基本上是在桌面上建立可停駐視窗的方式。 使用者可以在工作列上按一下滑鼠右鍵，然後從 [ **工具列** ] 子功能表中選取它來選取它。

![顯示範例服務中心的螢幕擷取畫面。](images/desk2.png)

一開始，桌面群組會停駐在工作列上。

![螢幕擷取畫面，顯示停駐在工作列上的桌面群組。](images/desk1.jpg)

然後，使用者可以將書桌波段拖曳至桌面，它就會顯示為一般視窗。

![書桌波段的螢幕擷取畫面](images/desk3.png)

## <a name="implementing-band-objects"></a>執行帶狀物件

討論下列主題。

-   [頻外物件基本概念](#band-object-basics)
-   [頻外註冊](#band-registration)
-   [自訂 Explorer 列的簡單範例](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a>頻外物件基本概念

雖然它們可以像一般視窗一樣使用，但頻外物件是存在於容器內的 COM 物件。 Explorer 列是由 Internet Explorer 所包含，而服務台則包含在 Shell 中。 雖然它們可提供不同的功能，但其基本的執行非常類似。 主要差異在於如何註冊波段物件，進而控制物件和其容器的類型。 本節將討論所有帶狀物件通用的執行層面。 如需其他的執行詳細資料，請參閱 [自訂 Explorer 列的簡單範例](#a-simple-example-of-a-custom-explorer-bar) 。

除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 和 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)，所有的帶狀物件都必須執行下列介面。

-   [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)

除了將其類別識別碼註冊 (CLSID) 之外，還必須針對適當的元件類別註冊 Explorer Bar 和書桌等物件。 註冊元件類別會決定物件類型及其容器。 工具群組使用不同的註冊程式，且沒有 (CATID) 的分類識別碼。 需要它們的三個頻外物件的 Catid 是：



| 頻外類型               | 元件類別 |
|-------------------------|--------------------|
| 垂直瀏覽器列   | CATID \_ InfoBand    |
| 水準瀏覽器列 | CATID \_ CommBand    |
| 書桌區               | CATID \_ DeskBand    |



 

請參閱 [頻外註冊](#band-registration) ，以進一步討論如何註冊波段物件。

如果寬線物件是接受使用者輸入，則也必須執行 [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)。 若要將專案加入至 Explorer 橫條圖或書桌群組的快捷方式功能表，必須將 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)匯出。 工具區不支援快捷方式功能表。

因為頻外物件會執行子視窗，所以它們也必須執行視窗程式來處理 Windows 訊息處理。

頻外物件可以透過容器的 [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) 介面，將命令傳送到其容器。 若要取得介面指標，請呼叫容器的 [**IInputObjectSite：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法，並要求 IID \_ IOleCommandTarget。 然後，您可以使用 [**IOleCommandTarget：： Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec)將命令傳送至容器。 命令群組為 CGID \_ DeskBand。 當呼叫帶狀物件的 [**IDeskBand：： GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) 方法時，容器會使用 *dwBandID* 參數來指派用於三個命令的一個識別碼。 支援四個 **IOleCommandTarget：： Exec** 命令識別碼。

-   DBID \_ BANDINFOCHANGED

    波段的資訊已變更。 將 *pvaIn* 參數設定為最新的 [**IDeskBand：： GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)呼叫中所收到的頻外識別碼。 容器會呼叫波段物件的 **IDeskBand：： GetBandInfo** 方法，以要求更新的資訊。

-   DBID \_ MAXIMIZEBAND

    最大化頻外。 將 *pvaIn* 參數設定為最新的 [**IDeskBand：： GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)呼叫中所收到的頻外識別碼。

-   DBID \_ SHOWONLY

    開啟或關閉容器中的其他波段。 將 *pvaIn* 參數設定為 \_ 具有下列其中一個值的 VT 未知類型：

    

    | 值 | 描述                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | 朋 克  | 頻外物件的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。 所有其他的桌面群組將會隱藏。 |
    | 0     | 隱藏所有的桌上波段。                                                                                        |
    | 1     | 顯示所有的桌面群組。                                                                                        |

    

     

-   DBID \_ PUSHCHEVRON

    [第5版](versions.md)。 顯示箭號功能表。 容器會傳送 [**RB \_ PUSHCHEVRON**](../controls/rb-pushchevron.md) 訊息，而此寬線物件會收到 [RBN \_ CHEVRONPUSHED](../controls/rbn-chevronpushed.md) 通知，提示它顯示箭號功能表。 將 [**IOleCommandTarget：： Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) 方法的 *nCmdExecOpt* 參數設定為最近呼叫 [**IDeskBand：： GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)時所收到的頻外識別碼。 使用應用程式定義的值，將 **IOleCommandTarget：： Exec** 方法的 *pvaIn* 參數設定為 VT \_ I4 類型。 它會將 RBN CHEVRONPUSHED 通知的 *lAppValue* 值傳回給波段物件 \_ 。

### <a name="band-registration"></a>頻外註冊

波段物件必須註冊為支援單元執行緒的 OLE 同進程伺服器。 伺服器的預設值是功能表文字字串。 若是 Explorer 橫條，它會出現在 [Internet Explorer **View** ] 功能表的 [ **Explorer Bar** ] 子功能表中。 針對工具群組，它會出現在 [Internet Explorer **視圖**] 功能表的 [**工具列**] 子功能表中。 若為 [中]，則會出現在工作列快捷方式功能表的 [ **工具列** ] 子功能表中。 如同功能表資源，在字母前面加上連字號 (&) 會讓它加上底線，並啟用鍵盤快速鍵。 例如，第一個圖形中顯示的垂直 Explorer 列的功能表字串為 "Sample &垂直 Explorer Bar"。

一開始，Internet Explorer 會使用元件類別，從登錄中取出已註冊之 Explorer Bar 物件的列舉。 為了提高效能，它會快取此列舉，進而忽略後續新增的瀏覽器列。 若要強制 Windows Internet Explorer 重建快取並辨識新的瀏覽器列，請在註冊新的瀏覽器列時刪除下列登錄機碼：

**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Discardable** \\ **PostSetup** \\ **元件類別** \\ **{00021493-0000-0000-C000-000000000046}** \\ **Enum**

**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Discardable** \\ **PostSetup** \\ **元件類別** \\ **{00021494-0000-0000-C000-000000000046}** \\ **Enum**

> [!Note]  
> 因為系統會為每個使用者建立 Explorer Bar 快取，所以您的安裝應用程式可能需要列舉所有使用者登錄區，或新增每個使用者的存根，以在使用者第一次登入時執行。

 

一般情況下，寬線物件的基本登錄專案會如下所示。

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

工具群組也必須將其物件的 CLSID 註冊 Internet Explorer。 若要這樣做，請在 [ **HKEY \_ 本機 \_ 電腦** 軟體 Microsoft Internet Explorer] 工具列上指派值（以 \\  \\  \\  \\ 工具區物件的 CLSID GUID 命名），如下所示。 它的資料值會被忽略，因此值型別不重要。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

您也可以將數個選擇性值新增至登錄。 比方說，如果您想要使用 Explorer 列來顯示 HTML，所顯示的值不是範例，而是應該使用的實際值，則必須使用下列值。

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

搭配上述的值使用時，如果您想要使用 Explorer 列來顯示 HTML，也需要下列選用值。 此值應該設定為包含 Explorer 列 HTML 內容之檔案的位置。

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

另一個選擇性值會定義 Explorer 列的預設寬度或高度，取決於它是垂直或水準。

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

BarSize 值應該設定為橫條的寬度或高度。 值需要八個位元組，並以二進位值的形式放在登錄中。 前四個位元組以十六進位格式指定以圖元為單位的大小，從最左邊的位元組開始。 最後四個位元組是保留的，而且應該設定為零。

例如，這裡顯示預設寬度為 291 (0x123) 圖元的 HTML 可用瀏覽器列的完整登錄專案。

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

您可以透過程式設計方式來處理帶物件 CATID 的註冊。  (CLSID StdComponentCategoriesMgr) 建立元件類別管理員物件 \_ ，並要求其 [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) 介面指標。 將帶狀物件的 CLSID 和 CATID 傳遞給 [**ICatRegister：： RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories)。

### <a name="a-simple-example-of-a-custom-explorer-bar"></a>自訂 Explorer 列的簡單範例

這個範例會逐步解說簡介中所顯示的範例垂直瀏覽器列。

建立自訂瀏覽器列的基本程式如下所示。

1.  [執行 DLL 所需的函數](#dll-functions)。
2.  [執行必要的 COM 介面。](#required-interface-implementations)
3.  [執行任何想要的選擇性 COM 介面。](#optional-interface-implementations)
4.  [註冊物件的 CLSID 和（如有必要）元件類別。](#clsid-registration)
5.  建立 Internet Explorer 的子視窗，調整大小以符合 Explorer 橫條圖的顯示區域。
6.  [您可以使用子視窗來顯示資訊，並與使用者互動。](#the-window-procedure)

在 Explorer Bar 範例中使用的非常簡單的實作為，只要針對適當的元件類別註冊，就可以用於任一種類型的 Explorer Bar 或書桌波段。 針對每個物件類型的顯示區域和容器，必須自訂更複雜的實作為。 不過，您可以藉由採用範例程式碼並將熟悉的 Windows 程式設計技術套用至子視窗，來完成這項自訂作業。 例如，您可以加入控制項以進行使用者互動，或為圖形提供更豐富的顯示。

### <a name="dll-functions"></a>DLL 函數

這三個物件都會封裝在單一 DLL 中，這會公開下列函式。

-   [**DllMain**](../dlls/dllmain.md)
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

前三個函式是標準的實作為，將不會在此討論。 Class Factory 實也是標準的。

### <a name="required-interface-implementations"></a>必要的介面實現

垂直 Explorer 列範例會實作為 CExplorerBar 類別一部分的四個必要介面： [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)、 [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)、 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)和 [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) 。 函式、函式和 **IUnknown** 實作為簡單的，而且不會在這裡討論。 如需詳細資訊，請參閱範例程式碼。

以下是詳細討論的介面。

-   [IObjectWithSite](#iobjectwithsite)
-   [IPersistStream](#ipersiststream)
-   [IDeskBand](#ideskband)

### <a name="iobjectwithsite"></a>IObjectWithSite

當使用者選取 Explorer 列時，容器會呼叫對應的帶狀物件的 [**IObjectWithSite：： SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 方法。 *PunkSite* 參數將設定為網站的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標。

一般情況下， [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 執行應該執行下列步驟：

1.  釋放目前保留的任何網站指標。
2.  如果傳遞至 [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 的指標設為 **Null**，則會移除該頻外。 **SetSite** 可以傳回 S \_ OK。
3.  如果傳遞至 [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 的指標為非 **Null**，則會設定新的網站。 **SetSite** 應該執行下列作業：
    1.  針對其 [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)介面呼叫網站上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。
    2.  呼叫 [**IOleWindow：： GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) 來取得父視窗的控制碼。 儲存控制碼以供稍後使用。 如果不再需要，請發行 [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) 。
    3.  建立帶狀物件的視窗，作為上一個步驟中取得之視窗的子系。 請勿將它建立為可見視窗。
    4.  如果寬線物件會執行 [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)，請針對其 [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite)介面呼叫網站上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。 將指標儲存至此介面，以供稍後使用。
    5.  如果所有步驟都成功，請返回 \_ [確定]。 如果不是，則傳回 OLE 自訂錯誤碼，指出失敗的內容。

Explorer Bar 範例以下列方式執行 [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 。 在下列程式碼中， *m \_ pSite* 是保存 [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) 指標的私用成員變數，而 *m \_ hwndParent* 會保存父視窗的控制碼。 在此範例中，也會處理視窗建立。 如果視窗不存在，這個方法會將 Explorer 列的視窗建立為 **SetSite** 所取得之父視窗的適當大小子系。 子視窗的控制碼會儲存在 *m \_ hwnd* 中。


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



範例的 [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite)實只要使用 [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite)所儲存的網站指標來包裝對網站的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法的呼叫。


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a>IPersistStream

Internet Explorer 會呼叫 Explorer 列的 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) 介面，以允許 explorer 列載入或儲存持續性資料。 如果沒有持續性資料，則方法仍必須傳回成功碼。 **IPersistStream** 介面繼承自 [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist)，因此必須執行五個方法。

-   [**IPersist：： GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [**IPersistStream：： IsDirty**](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [**IPersistStream：： Load**](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [**IPersistStream：： Save**](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [**IPersistStream：： GetSizeMax**](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

Explorer Bar 範例不會使用任何持續性資料，而且只有最基本的 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)執行。 [**IPersist：： GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) 會傳回物件的 CLSID (clsid \_ SampleExplorerBar) ，其餘部分則會傳回 \_ [OK]、[ \_ FALSE] 或 [E >notimpl] \_ 。

### <a name="ideskband"></a>IDeskBand

[**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)介面是適用于頻外物件的。 除了它的方法之外，它也繼承自 [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)，而後者又繼承自 [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)。

有兩種 [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) 方法： [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) 和 [**IOleWindow：： CoNtextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp)。 Explorer Bar 範例的 **GetWindow** 會傳回 explorer 列的子視窗控制碼（ *m \_ hwnd*）。 不會執行即時線上說明，因此 **CoNtextSensitiveHelp** 會傳回 **E \_ >notimpl**。

[**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)介面有三個方法。

-   [**IDockingWindow::ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [**IDockingWindow::CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [**IDockingWindow::ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

[**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)方法不會與任何類型的波段物件一起使用，且一律會傳回 E \_ >notimpl。 [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)方法會根據其參數的值顯示或隱藏 Explorer 工具列的視窗。


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



[**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)方法會終結 Explorer 工具列的視窗。


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



其餘的方法 [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)是 **IDeskBand** 專用的。 Internet Explorer 使用它來指定 Explorer 列的識別碼和瀏覽模式。 Internet Explorer 也可能會填入以第三個參數傳遞之 [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo)結構的 **dwMask** 成員，以從 Explorer 列要求一或多個資訊。 **GetBandInfo** 應該儲存識別碼和查看模式，並以要求的資料填入 **DESKBANDINFO** 結構。 Explorer Bar 範例會實 **GetBandInfo** ，如下列程式碼範例所示。


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a>選用介面實作為

有兩個介面不是必要的，但可能有助於實作為： [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) 和 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)。 Explorer Bar 範例會執行 **IInputObject**。 如需如何執行 **ICoNtextMenu** 的相關資訊，請參閱檔。

### <a name="iinputobject"></a>IInputObject

如果波段物件接受使用者輸入，則必須執行 [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) 介面。 Internet Explorer 會執行 [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) ，並使用 **IInputObject** 來維持適當的使用者輸入焦點（當它有一個以上的包含視窗時）。 有三種方法需要由 Explorer 列來執行。

-   [**IInputObject::UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [**IInputObject::HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [**IInputObject::TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

Internet Explorer 會呼叫 [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) 來通知 Explorer 列正在啟用或停用。 啟用時，Explorer Bar 範例會呼叫 [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) 將焦點設定至其視窗。

Internet Explorer 在嘗試判斷哪個視窗具有焦點時，會呼叫 [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) 。 如果 Explorer 列的視窗或其中一個子代具有焦點，則 **HasFocusIO** 應該會傳回 \_ [確定]。 如果沒有，則應該傳回 \_ FALSE。

[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) 可讓物件處理鍵盤快捷。 Explorer Bar 範例不會執行此方法，因此它會傳回 \_ FALSE。

範例列的 [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) 執行如下所示。


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a>CLSID 註冊

和所有 COM 物件一樣，必須註冊 Explorer 列的 CLSID。 為了讓物件能夠與 Internet Explorer 正常運作，它也必須註冊 (CATID InfoBand) 的適當元件類別 \_ 。 下列程式碼範例會顯示 Explorer 列的相關程式碼區段。


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



範例中的頻外物件註冊會使用一般 COM 程式。

除了 CLSID 之外，也必須針對一或多個元件類別目錄註冊帶狀物件服務器。 這實際上是在垂直和水準瀏覽器橫條圖範例之間執行的主要差異。 這項處理常式的處理方式是建立元件類別管理員物件 (CLSID \_ StdComponentCategoriesMgr) 並使用 [**ICatRegister：： RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) 方法來註冊帶的物件服務器。 在此範例中，元件類別註冊的處理方式是將 Explorer Bar 範例的 CLSID 和 CATID 傳遞至私用函式（**RegisterComCat**），如下列程式碼範例所示。


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a>視窗程式

因為寬線物件會使用子視窗來顯示它，所以它必須執行視窗程式來處理 Windows 訊息處理。 頻外範例有最基本的功能，因此其視窗程式只會處理五個訊息：

-   [**WM \_ NCCREATE**](../winmsg/wm-nccreate.md)
-   [**WM \_ 油漆**](../gdi/wm-paint.md)
-   [**WM \_ 命令**](../menurc/wm-command.md)
-   [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md)
-   [**WM \_ KILLFOCUS**](../inputdev/wm-killfocus.md)

您可以輕鬆地展開程式以容納額外的訊息，以支援更多的功能。


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



WM \_ 命令處理常式只會傳回零。 在 \_ 簡介中，WM 油漆處理常式會建立顯示在 Explorer Bar 範例中的簡單文字顯示。


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



WM \_ SETFOCUS 和 WM \_ KILLFOCUS 處理常式會藉由呼叫網站的 [**IInputObjectSite：： OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) 方法，來通知網站焦點變更。


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



頻外物件可透過建立自訂的瀏覽器列，提供有彈性且功能強大的方式來擴充 Internet Explorer 的功能。 執行服務台區可讓您延伸一般視窗的功能。 雖然需要一些 COM 程式設計，但最終還是會為您的使用者介面提供子視窗。 從該處，大量的執行都可以使用熟悉的 Windows 程式設計技術。 雖然這裡所討論的範例僅具有有限的功能，但它也說明了一個頻外物件的所有必要功能，而且可以輕鬆擴充以建立獨特且功能強大的使用者介面。

 

 
