---
title: 保存功能區狀態
description: Windows Ribon framework (功能區) 可讓您在應用程式會話之間保留各種使用者設定和喜好設定的狀態。
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a3b704151b657bdfe95845c8473a0fd197e87b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315763"
---
# <a name="persisting-ribbon-state"></a><span data-ttu-id="920c1-103">保存功能區狀態</span><span class="sxs-lookup"><span data-stu-id="920c1-103">Persisting Ribbon State</span></span>

<span data-ttu-id="920c1-104">Windows Ribon framework (功能區) 可讓您在應用程式會話之間保留各種使用者設定和喜好設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="920c1-104">The Windows Ribon framework (Ribbon) provides the ability to preserve the state of a variety of user settings and preferences across application sessions.</span></span>

-   [<span data-ttu-id="920c1-105">簡介</span><span class="sxs-lookup"><span data-stu-id="920c1-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="920c1-106">可預測的體驗</span><span class="sxs-lookup"><span data-stu-id="920c1-106">A Predictable Experience</span></span>](#a-predictable-experience)
-   [<span data-ttu-id="920c1-107">儲存功能區設定</span><span class="sxs-lookup"><span data-stu-id="920c1-107">Save Ribbon Settings</span></span>](#save-ribbon-settings)
-   [<span data-ttu-id="920c1-108">載入功能區設定</span><span class="sxs-lookup"><span data-stu-id="920c1-108">Load Ribbon Settings</span></span>](#load-ribbon-settings)
-   [<span data-ttu-id="920c1-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="920c1-109">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="920c1-110">簡介</span><span class="sxs-lookup"><span data-stu-id="920c1-110">Introduction</span></span>

<span data-ttu-id="920c1-111">使用者可以在執行時間自訂功能區的各個層面，包括設定和互動喜好設定，以改善可用性和生產力。</span><span class="sxs-lookup"><span data-stu-id="920c1-111">Various aspects of a ribbon, including configuration and interaction preferences, can be customized by a user at run time to improve usability and productivity.</span></span> <span data-ttu-id="920c1-112">功能區架構可透過在 [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) 介面的執行中定義的兩種方法，提供在應用程式會話之間保留這些設定的功能： [**IUIRibbon：： LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) 和 [**IUIRibbon：： SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)。</span><span class="sxs-lookup"><span data-stu-id="920c1-112">The Ribbon framework provides the functionality to preserve these settings across application sessions through two methods defined in the implementation of the [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) interface: [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) and [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream).</span></span>

## <a name="a-predictable-experience"></a><span data-ttu-id="920c1-113">可預測的體驗</span><span class="sxs-lookup"><span data-stu-id="920c1-113">A Predictable Experience</span></span>

<span data-ttu-id="920c1-114">[功能區使用者經驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx)會建議您盡可能提供可預測的使用者體驗，功能區應用程式應該會在應用程式關閉時，從最後選取的索引標籤) 保留功能區的狀態 (。</span><span class="sxs-lookup"><span data-stu-id="920c1-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) advise that, to provide the most predictable user experience possible, Ribbon applications should preserve the state of the ribbon (aside from the last selected tab) as the application is closed.</span></span> <span data-ttu-id="920c1-115">如此一來，當相同的應用程式啟動時，就可以還原前一個會話的設定和自訂，而且使用者可以使用與其留下的相同方式來繼續與應用程式互動。</span><span class="sxs-lookup"><span data-stu-id="920c1-115">In this way, when the same application is launched, the settings and customizations from the previous session can be restored and the user can expect to continue interacting with the application in the same way as they left it.</span></span>

<span data-ttu-id="920c1-116">可在執行時間修改並在應用程式會話之間保留的功能區設定會列在命令內容功能表中。</span><span class="sxs-lookup"><span data-stu-id="920c1-116">Ribbon settings that can be modified at run time and preserved across application sessions are listed in the Command context menu.</span></span> <span data-ttu-id="920c1-117">包括：</span><span class="sxs-lookup"><span data-stu-id="920c1-117">They include:</span></span>

-   <span data-ttu-id="920c1-118">由使用者新增至 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md) 命令清單的命令。</span><span class="sxs-lookup"><span data-stu-id="920c1-118">Commands added to the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) Command list by the user.</span></span> <span data-ttu-id="920c1-119">由 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件透過 [UI \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) 屬性索引鍵來指定。</span><span class="sxs-lookup"><span data-stu-id="920c1-119">Specified by an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span>

    <span data-ttu-id="920c1-120">下列螢幕擷取畫面顯示 [ **新增至快速存取] 工具列** 內容功能表命令。</span><span class="sxs-lookup"><span data-stu-id="920c1-120">The following screen shot shows the **Add to Quick Access Toolbar** context menu Command.</span></span>

    ![microsoft 油漆功能區中命令內容功能表的螢幕擷取畫面。](images/controls/qat-contextmenu-add.png)

-   <span data-ttu-id="920c1-122">慣用的 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md) 停駐狀態。</span><span class="sxs-lookup"><span data-stu-id="920c1-122">The preferred [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) docking state.</span></span> <span data-ttu-id="920c1-123">由 [ui \_ PKEY \_ QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md)屬性索引鍵的 [**ui \_ CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock)值所指定。</span><span class="sxs-lookup"><span data-stu-id="920c1-123">Specified by the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) value of the [UI\_PKEY\_QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md) property key.</span></span>

    <span data-ttu-id="920c1-124">這個螢幕擷取畫面會在其預設應用程式標題列位置顯示 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md) ，並在功能區內容功能表命令 **下方顯示快速存取工具列** 。</span><span class="sxs-lookup"><span data-stu-id="920c1-124">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) in its default application title bar location and the **Show Quick Access Toolbar below the Ribbon** context menu Command.</span></span>

    ![microsoft 油漆功能區中命令內容功能表的螢幕擷取畫面。](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="920c1-126">這個螢幕擷取畫面會顯示功能區下方的 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md) 。</span><span class="sxs-lookup"><span data-stu-id="920c1-126">This screen shot shows the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md) below the ribbon.</span></span>

    ![快速存取工具列上停駐于功能區下方的螢幕擷取畫面。](images/controls/qat-dockbottom.png)

-   <span data-ttu-id="920c1-128">功能區最小化狀態，如 [UI \_ PKEY \_ 最小化](windowsribbon-reference-properties-uipkey-minimized.md) 屬性索引鍵的布林值所指定。</span><span class="sxs-lookup"><span data-stu-id="920c1-128">The ribbon minimized state as specified by the boolean value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key.</span></span>

    > [!Note]  
    > <span data-ttu-id="920c1-129">功能區最小化狀態不等於功能區折迭狀態。</span><span class="sxs-lookup"><span data-stu-id="920c1-129">The ribbon minimized state is not equivalent to the ribbon collapsed state.</span></span> <span data-ttu-id="920c1-130">處於折迭狀態時，功能區會完全隱藏，而且無法與互動。</span><span class="sxs-lookup"><span data-stu-id="920c1-130">When in collapsed state, the ribbon is completely hidden and cannot be interacted with.</span></span> <span data-ttu-id="920c1-131">如果應用程式視窗的大小縮小（水準或垂直）至功能區遮蔽應用程式工作區的點，則架構會自動叫用此狀態。</span><span class="sxs-lookup"><span data-stu-id="920c1-131">The framework invokes this state automatically if the application window is reduced in size, either horizontally or vertically, to the point that the ribbon obscures the application workspace.</span></span> <span data-ttu-id="920c1-132">當應用程式視窗的大小增加時，架構會還原功能區。</span><span class="sxs-lookup"><span data-stu-id="920c1-132">The framework restores the ribbon when the size of the application window is increased.</span></span>

     

    <span data-ttu-id="920c1-133">這個螢幕擷取畫面會顯示 [功能區] 內容功能表命令的 **最小化** 。</span><span class="sxs-lookup"><span data-stu-id="920c1-133">This screen shot shows the **Minimize the Ribbon** context menu Command.</span></span>

    ![microsoft 油漆功能區中命令內容功能表的螢幕擷取畫面。](images/controls/qat-contextmenu-add.png)

    <span data-ttu-id="920c1-135">這個螢幕擷取畫面顯示最小化的功能區。</span><span class="sxs-lookup"><span data-stu-id="920c1-135">This screen shot shows a minimized ribbon.</span></span>

    ![最小化 microsoft 油漆功能區的螢幕擷取畫面。](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a><span data-ttu-id="920c1-137">儲存功能區設定</span><span class="sxs-lookup"><span data-stu-id="920c1-137">Save Ribbon Settings</span></span>

<span data-ttu-id="920c1-138">[**IUIRibbon：： SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)方法會將持續性功能區狀態的二進位表示寫入 (上一節中所述的) 至 [IStream](/windows/win32/api/objidl/nn-objidl-istream)物件。</span><span class="sxs-lookup"><span data-stu-id="920c1-138">The [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method writes a binary representation of the persistent ribbon state (outlined in the previous section) to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object.</span></span> <span data-ttu-id="920c1-139">然後，應用程式會將 IStream 物件的內容儲存到檔案或 Windows 登錄中。</span><span class="sxs-lookup"><span data-stu-id="920c1-139">The application then saves the content of the IStream object to a file or the Windows registry.</span></span>

<span data-ttu-id="920c1-140">下列範例示範使用 [**IUIRibbon：： SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)方法將功能區狀態寫入 [IStream](/windows/win32/api/objidl/nn-objidl-istream)物件時所需的基本程式碼。</span><span class="sxs-lookup"><span data-stu-id="920c1-140">The following example demonstrates the basic code required to write the ribbon state to an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span>


```C++
// pRibbon        - Pointer to the IUIRibbon interface
// ppStatusStream - Pointer to the location of a newly created IStream object
HRESULT CApplication::SaveRibbonStatusToStream(
                        __in IUIRibbon *pRibbon, 
                        __out IStream **ppStatusStream)
{
  HRESULT hr = E_FAIL; 

  *ppStatusStream = NULL;
  IStream* pStream;
  if (SUCCEEDED(hr = CreateStreamOnHGlobal(
                       NULL,  // Internally allocate a new shared memory.
                       FALSE, // Free hGlobal after IStream object released.
                       &pStream)))
  {
    if (SUCCEEDED(hr = pRibbon->SaveSettingsToStream(*ppStatusStream)))
    {                  
      pStream->AddRef();
      *ppStatusStream = pStream;
    }
    pStream->Release();
  }
  return hr;
}
```



## <a name="load-ribbon-settings"></a><span data-ttu-id="920c1-141">載入功能區設定</span><span class="sxs-lookup"><span data-stu-id="920c1-141">Load Ribbon Settings</span></span>

<span data-ttu-id="920c1-142">[**IUIRibbon：： LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)方法可用來透過 [**IUIRibbon：： SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)方法，取得儲存為 [IStream](/windows/win32/api/objidl/nn-objidl-istream)物件的持續性功能區狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="920c1-142">The [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method is used to retrieve the persistent ribbon state information stored as an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object by the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method.</span></span> <span data-ttu-id="920c1-143">當應用程式初始化時，IStream 物件中的資訊會套用至功能區 UI。</span><span class="sxs-lookup"><span data-stu-id="920c1-143">The information in the IStream object is applied to the ribbon UI when the application initializes.</span></span>

<span data-ttu-id="920c1-144">下列範例示範使用 [**IUIRibbon：： LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)方法從 [IStream](/windows/win32/api/objidl/nn-objidl-istream)物件載入功能區狀態所需的基本程式碼。</span><span class="sxs-lookup"><span data-stu-id="920c1-144">The following example demonstrates the basic code required to load the ribbon state from an [IStream](/windows/win32/api/objidl/nn-objidl-istream) object with the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>


```C++
// pRibbon       - Pointer to the IUIRibbon interface
// pStatusStream - Pointer to the IStream object that contains the Ribbon state information
HRESULT CApplication::LoadRibbonStatusFromStream(
                        __in IUIRibbon *pRibbon, 
                        __in IStream *pStatusStream)
{     
  HRESULT hr = E_FAIL;
  if (pStatusStream)
  {
    // Set the stream position to the beginning first.
    LARGE_INTEGER liStart = {0, 0};
    ULARGE_INTEGER ulActual;
    pStatusStream->Seek(liStart, STREAM_SEEK_SET, &ulActual);
    hr = pRibbon->LoadSettingsFromStream(pStatusStream);
  }
  return hr;
}
```



<span data-ttu-id="920c1-145">為了達到最佳效能， [**IUIRibbon：： LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) 方法應該在 framework 初始化階段期間從 [**IUIApplication：： OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) 回呼函式中呼叫，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="920c1-145">For optimal performance, the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method should be called from the [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) callback function during the framework initialization phase, as shown in the following example.</span></span>


```C++
IFACEMETHODIMP CMyRibbonApplication::OnViewChanged(
                                       UINT nViewID, 
                                       __in UI_VIEWTYPE typeID, 
                                       __in IUnknown* pView, 
                                       UI_VIEWVERB verb, 
                                       INT iReasonCode)
{
  HRESULT hr = E_NOTIMPL;
  if (UI_VIEWVERB_CREATE == verb)
  {
    IUIRibbon* pRibbon = NULL;
    hr = pView->QueryInterface(IID_PPV_ARGS(&pRibbon));

    if (SUCCEEDED(hr))
    {
      hr = _LoadRibbonSettings(pRibbon);
      pRibbon->Release();
    }
  }
  return hr;
}

HRESULT CMyRibbonApplication::_LoadRibbonSettings(IUIRibbon* pRibbon)
{
  ...
  pRibbon->LoadSettingsFromStream(pStream);
  ...
}
```



<span data-ttu-id="920c1-146">相同功能區架構應用程式的多個實例可以個別管理每個功能區狀態為個別的 [istream](/windows/win32/api/objidl/nn-objidl-istream) 物件，或透過單一 istream 物件以群組的方式來管理。</span><span class="sxs-lookup"><span data-stu-id="920c1-146">Multiple instances of the same Ribbon framework application can manage each ribbon state independently as separate [IStream](/windows/win32/api/objidl/nn-objidl-istream) objects or as a group through a single IStream object.</span></span>

<span data-ttu-id="920c1-147">在跨應用程式實例群組同步處理功能區狀態時，每個最上層視窗都必須接聽 [WM \_ 啟用](../inputdev/wm-activate.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="920c1-147">When synchronizing ribbon state across a group of application instances, each top-level window must listen for a [WM\_ACTIVATE](../inputdev/wm-activate.md) notification.</span></span> <span data-ttu-id="920c1-148">停用的最上層視窗會使用 [**IUIRibbon：： SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) 方法來儲存其功能區狀態，而所啟動的最上層視窗會使用 [**IUIRibbon：： LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) 方法載入其功能區狀態。</span><span class="sxs-lookup"><span data-stu-id="920c1-148">The top-level window being deactivated saves its ribbon state using the [**IUIRibbon::SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) method, and the top-level window being activated loads its ribbon state using the [**IUIRibbon::LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="920c1-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="920c1-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="920c1-150">快速存取工具列</span><span class="sxs-lookup"><span data-stu-id="920c1-150">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 