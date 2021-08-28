---
description: '介面 (Windows 執行階段 c + +) '
ms.assetid: CB05B5F8-BE15-4BE0-A651-F6E8912D649D
title: '介面 (Windows 執行階段) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e813bce21e44a7fe7a3b5f2feffbc31b78a4f8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884683"
---
# <a name="interfaces"></a>介面

## <a name="in-this-section"></a>本節內容

| 介面 | 描述 |
|-|-|
| [**IActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iactivatableclassregistration) | 允許取得類別的註冊資訊。 |
| [**IActivationFactory**](/windows/win32/api/activation/nn-activation-iactivationfactory) | 讓類別由 Windows 執行階段來啟用。 |
| [**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference) | 啟用物件的 agile 參考。 |
| [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) | 啟用單元關機通知處理常式的註冊。 |
| [**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md) | 表示非同步動作完成時所呼叫的方法。 |
| [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) | 表示非同步動作。 |
| [**IAsyncActionProgressHandler &lt; TProgress&gt;**](/previous-versions//br205782(v=vs.85)) | 表示非同步動作報告進度時所呼叫的方法。 |
| [**Iasyncactionwithprogress<tprogress> iasyncoperation<tresult> &lt; TProgress&gt;**](/previous-versions//br205784(v=vs.85)) | 表示報告進度的非同步動作。 |
| [**IAsyncActionWithProgressCompletedHandler &lt; TProgress&gt;**](/previous-versions//br205785(v=vs.85)) | 表示當報告進度的非同步動作完成時，所呼叫的方法。 |
| [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo) | 提供非同步作業的支援。 |
| [**Iasyncoperation<tresult>HTTP &lt; TResult&gt;**](/previous-versions//br205802(v=vs.85)) | 表示傳回結果的非同步作業。 |
| [**IAsyncOperationCompletedHandler &lt; TResult&gt;**](/previous-versions//br205803(v=vs.85)) | 表示非同步作業完成時所呼叫的方法。 |
| [**IAsyncOperationProgressHandler**](/previous-versions//br205805(v=vs.85)) | 表示非同步作業報告進度時所呼叫的方法。 |
| [**IAsyncOperationWithProgress**](/previous-versions//br205807(v=vs.85)) | 表示傳回結果和報告進度的非同步作業。 |
| [**IAsyncOperationWithProgressCompletedHandler<TResult，TProgress>**](/previous-versions//br205808(v=vs.85)) | 表示當報告進度的非同步作業完成時，所呼叫的方法。 |
| [**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative) | 代表音訊資料的框架。 |
| [**IAudioFrameNativeFactory**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenativefactory) | 建立 [**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)的實例。 |
| [**Windows.storage.streams.ibuffer**](/previous-versions//hh438362(v=vs.85)) | 表示位元組陣列。 |
| [**IBufferByteAccess**](/previous-versions//hh846267(v=vs.85)) | 以位元組陣列表示緩衝區。 |
| [**Windows.foundation.iclosable**](/windows/win32/api/windows.foundation/nn-windows-foundation-iclosable) | 定義釋放已配置資源的方法。 |
| [**ICompositionDrawingSurfaceInterop**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop) | 原生互通性介面，可讓您使用矩形來定義要繪製的區域，以在介面物件上繪製。 |
| [**ICompositionDrawingSurfaceInterop2**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop2) | 原生互通介面，可讓您讀回組合繪圖介面 (或複合虛擬繪圖表面) 的內容。 |
| [**ICompositionGraphicsDeviceInterop**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiongraphicsdeviceinterop) | 原生互通性介面，可讓您取得及設定圖形裝置。 |
| [**IContactManagerInterop**](/previous-versions//dn302109(v=vs.85)) | 可存取管理多個視窗的應用程式中的 [**ContactManager**](/uwp/api/Windows.ApplicationModel.Contacts.ContactManager?view=winrt-19041) 方法。 |
| [**ICoreApplication**](/previous-versions//hh438365(v=vs.85)) | 可讓應用程式處理狀態變更、管理 windows，以及與各種 UI 架構整合。 |
| [**ICoreApplicationExit**](/previous-versions//hh438366(v=vs.85)) | 提供 Windows 存放區應用程式停止執行的方法。 |
| [**ICoreApplicationInitialization**](/previous-versions//hh438370(v=vs.85)) | 包含用來從應用程式進入點啟動應用程式物件的 run 方法。 |
| [**ICoreApplicationView**](/previous-versions//hh438372(v=vs.85)) | 表示應用程式的視圖。 |
| [**ICoreImmersiveApplication**](/previous-versions//hh438382(v=vs.85)) | 包含在應用程式中管理檢視的方法。 |
| [**ICoreInputInterop**](/windows/desktop/api/corewindow/nn-corewindow-icoreinputinterop) | 在 Windows 存放區應用程式的 [**CoreInput**](https://www.bing.com/search?q=**CoreInput**)物件上啟用輸入來源。 |
| [**ICoreWindowInterop**](/windows/desktop/api/corewindow/nn-corewindow-icorewindowinterop) | 讓應用程式取得與此介面相關聯 ([**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041)) 視窗 handleof 視窗。 |
| [**IDllServerActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-idllserveractivatableclassregistration) | 允許取得同進程伺服器的註冊資訊。 |
| [**IErrorReportingSettings**](/previous-versions//br205818(v=vs.85)) | 提供 Windows 執行階段應用程式的偵錯工具整合。 |
| [**IEventHandler &lt; T&gt;**](/previous-versions//hh438385(v=vs.85)) | 表示方法，該方法將處理具有 **T** 類型事件資料的事件。 |
| [**IExeServerActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration) | 允許取得跨進程伺服器的註冊資訊。 |
| [**IExeServerRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserverregistration) | 表示已註冊的跨進程伺服器。 |
| [**IFindReferenceTargetsCallback**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ifindreferencetargetscallback) | 定義來自 [**IReferenceTracker：： FindTrackerTargets**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets)之回呼的介面。 此介面的執行必須將它找到的任何 [**IReferenceTrackerTarget**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) 實例傳遞給 **FoundTrackerTarget** 方法。 |
| [**IInputPaneInterop**](/windows/desktop/api/inputpaneinterop/nn-inputpaneinterop-iinputpaneinterop) | 啟用存取桌面應用程式中 [**InputPane**](/uwp/api/Windows.UI.ViewManagement.InputPane?view=winrt-19041) 類別的成員。 |
| [**IInputStream**](/previous-versions//hh438387(v=vs.85)) | 可讓您在連續的位元組資料流程上取得非同步讀取器作業。 |
| [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable) | 提供所有 Windows 執行階段類別所需的功能。 |
| [**Iiterable<t> &lt; T&gt;**](/previous-versions//br205825(v=vs.85)) | 公開反覆運算器，其支援在指定類型的集合上進行簡單的反覆運算。 |
| [**Iiterator<t> &lt; T&gt;**](/previous-versions//br205827(v=vs.85)) | 支援對集合進行反復專案。 |
| [**Inputiterator<ikeyvaluepair<k<K，V>**](/previous-versions//br205831(v=vs.85)) | 代表索引鍵/值組。 |
| [**ILanguageExceptionErrorInfo**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo) | 透過呼叫 RoOriginateLanguageException，可讓您抓取儲存在錯誤資訊中的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標。 |
| [**ILanguageExceptionErrorInfo2**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2) | 可讓語言投射以 [**ILanguageExceptionErrorInfo**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo)的形式提供和取出錯誤資訊，並提供跨語言界限運作的額外優點。 |
| [**ILanguageExceptionTransform**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptiontransform) | 允許語言投射提供給系統的任何和所有內容，從攔截不同例外狀況的 catch 處理常式內容擲回的例外狀況。 |
| [**ILanguageExceptionStackBackTrace**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionstackbacktrace) | 允許投影針對該例外狀況提供自訂堆疊追蹤。 |
| [**IMap<K，V>**](/previous-versions//br205834(v=vs.85)) | 表示關聯集合。 |
| [**IMapChangedEventArgs &lt; K&gt;**](/previous-versions//br205835(v=vs.85)) | 提供 [**MapChanged**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) 事件的資料。 |
| [**IMapView<K，V>**](/previous-versions//br205838(v=vs.85)) | 代表 [**IMap (K，V)**](/previous-versions//br205834(v=vs.85))中不可變的視圖。 |
| [**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85)) | 以位元組陣列的形式提供 [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) 的存取權。 |
| [**IMetaDataAssemblyImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport) | 提供存取及檢查組件資訊清單內容的方法。 |
| [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) | 提供方法來建立新的中繼資料範圍，或開啟現有的範圍。 |
| [**IMetaDataDispenserEx**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenserex) | 擴充 [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) 介面，以提供控制中繼資料 api 在目前中繼資料範圍上運作方式的功能。 |
| [**IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) | 提供從可攜式執行檔 (PE) 或其他來源匯入及管理現有中繼資料的方法，例如類型程式庫或獨立的執行階段中繼資料二進位檔。 |
| [**IMetaDataImport2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport2) | 擴充 [**IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) 介面，以提供使用泛型型別的功能。 |
| [**IMetaDataTables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) | 提供儲存和擷取資料表中的中繼資料資訊的方法。 |
| [**IMetaDataTables2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables2) | 擴充 [**IMetaDataTables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) ，以包含處理中繼資料資料流程的方法。 |
| [**Iobservablemap 且<K，V>**](/previous-versions//br205851(v=vs.85)) | 通知事件處理常式動態變更對應，例如新增或移除專案時。 |
| [**IObservableVector &lt; T&gt;**](/previous-versions//br205854(v=vs.85)) | 通知事件處理常式對向量的變更。 |
| [**IOplockBreakingHandler**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-ioplockbreakinghandler) | 目前未執行這個介面。 |
| [**IOutputStream**](/previous-versions//hh438390(v=vs.85)) | 可讓您在連續的位元組資料流程上取得非同步寫入器作業。 |
| [**IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) | 代表高效能 API，用來顯示可攜檔案格式的單一頁面 (PDF) 檔。 |
| [**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85)) | 可讓偵錯工具開發人員控制 Windows 存放區應用程式的生命週期，例如暫停或繼續。 |
| [**IPlayToManagerInterop**](/windows/desktop/api/playtomanagerinterop/nn-playtomanagerinterop-iplaytomanagerinterop) | 可存取管理多個視窗的 Windows 存放區應用程式中的 [**PlayToManager**](/uwp/api/Windows.Media.PlayTo.PlayToManager?view=winrt-19041)方法。 |
| [**IPrintManagerInterop**](/windows/desktop/api/printmanagerinterop/nn-printmanagerinterop-iprintmanagerinterop) | 可存取管理多個視窗的 Windows 存放區應用程式中的 [**PrintManager**](/uwp/api/Windows.Graphics.Printing.PrintManager?view=winrt-19041)方法。 |
| [**IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) | 表示 Windows 執行階段屬性存放區中的值。 |
| [**IPropertyValueStatics**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics) | 建立可儲存在屬性存放區中的 [**IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) 物件。 |
| [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) | 允許取得位於隨機存取位元組資料流程上指定位置的非同步位元組讀取器或位元組寫入器。 |
| [**IRandomAccessStreamFileAccessMode**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-irandomaccessstreamfileaccessmode) | 提供在呼叫 [**StorageFile. OpenAsync**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) 方法以開啟隨機存取位元組資料流程時，所使用之檔案存取模式的存取權。 |
| [**IReference &lt; T&gt;**](/previous-versions//br224583(v=vs.85)) | 可延伸使用者定義列舉、結構和委派類型的 Windows 執行階段屬性系統。 |
| [**IReferenceArray &lt; T&gt;**](/previous-versions//br224584(v=vs.85)) | 針對使用者定義的列舉、結構和委派類型的陣列，可延伸 Windows 執行階段的屬性系統。 |
| [**IReferenceTracker**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) | 定義 XAML 架構用來管理 XAML 物件參考的介面。 |
| [**IReferenceTrackerHost**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost) | 定義介面，這個介面會提供由 XAML 架構使用的垃圾收集 (GC) 系統所使用的全域服務。 |
| [**IReferenceTrackerManager**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager) | 定義 XAML 物件參考管理員的介面。 執行此介面來管理 XAML 物件上的 [**IReferenceTracker**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) 實例。 |
| [**IReferenceTrackerTarget**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) | 定義由 XAML 參考之垃圾收集行程物件所執行的介面。 |
| [**IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) | 表示錯誤的詳細資料，包括受限制的錯誤資訊。 |
| [**ISoftwareBitmapNative**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative) | 代表軟體點陣圖。 |
| [**ISoftwareBitmapNativeFactory**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnativefactory) | 建立 [**ISoftwareBitmapNative**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative)的實例。 |
| [**IStorageFolderHandleAccess**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istoragefolderhandleaccess) | 提供存取儲存體資料夾的作業系統控制碼。 |
| [**IStorageItemHandleAccess**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istorageitemhandleaccess) | 提供存取儲存體檔案的作業系統控制碼。 |
| [**IStringable**](/windows/win32/api/windows.foundation/nn-windows-foundation-istringable) | 提供將目前物件表示為字串的方法。 |
| [**ISurfaceImageSourceManagerNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcemanagernative) | 可在相同進程中建立的所有 [**SurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) 物件上執行大量作業。 |
| [**ISurfaceImageSourceNativeWithD2D**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d) | 提供 [**SurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) 或 [**virtualsurfaceimagesource 這是**](/uwp/api/Windows.UI.Xaml.Media.Imaging.VirtualSurfaceImageSource?view=winrt-19041)中顯示的共用 Microsoft DirectX 介面的實作為。 |
| [**ISurfaceImageSourceNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative) | 提供 Direct2D 繪圖的共用固定大小表面的執行。 |
| [**ISuspendingDeferral**](isuspendingdeferral.md) | 管理延遲的應用程式暫停作業。 |
| [**ISuspendingEventArgs**](isuspendingeventargs.md) | 提供應用程式暫停事件的資料。 |
| [**ISuspendingOperation**](isuspendingoperation.md) | 提供應用程式暫停作業的相關資訊。 |
| [**ISwapChainBackgroundPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative) | 提供 XAML 與 DirectX 交換鏈之間的互通性。 |
| [**ISwapChainPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative) | 提供 XAML 與 DirectX 交換鏈之間的互通性。 不同于 [**SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041)， **SwapChainPanel** 可以出現在 XAML 顯示樹狀結構中的任何層級，而且任何指定的樹狀結構中都可以有1個以上的位置。 |
| [**ISwapChainPanelNative2**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative2) | 提供 XAML 與 DirectX 交換鏈之間的互通性。 不同于 [**SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041)， **SwapChainPanel** 可以出現在 XAML 顯示樹狀結構中的任何層級，而且任何指定的樹狀結構中都可以有1個以上的位置。 |
| [**ITypedEventHandler<Windows.foundation.typedeventhandler<tsender、TArgs>**](/previous-versions//hh438424(v=vs.85)) | 表示方法，該方法會處理來自類型 **windows.foundation.typedeventhandler<tsender** 的傳送者和類型 **T** 之事件資料的事件。 |
| [**IUnbufferedFileHandleOplockCallback**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleoplockcallback) | 定義當您藉由呼叫 [**IUnbufferedFileHandleProvider：： OpenUnbufferedFileHandle**](/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle) 方法所取得之控制碼的隨機鎖定中斷時，想要執行的回呼方法。 |
| [**IUnbufferedFileHandleProvider**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleprovider) | 提供 [**StorageFile. OpenAsync**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) 方法所建立之隨機存取位元組資料流程的控制碼存取。 |
| [**IVector &lt; T&gt;**](/previous-versions//br224590(v=vs.85)) | 代表元素的隨機存取集合。 |
| [**IVectorChangedEventArgs**](ivectorchangedeventargs.md) | 提供 [**VectorChanged**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) 事件的資料。 |
| [**IVectorView &lt; T&gt;**](/previous-versions//br224594(v=vs.85)) | 將不可變的視圖表示為 [**IVector (T)**](/uwp/api/windows.foundation.collections.ivector-1?view=winrt-19041)。 |
| [**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative) | 表示影片資料的框架。 |
| [**IVideoFrameNativeFactory**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenativefactory) | 建立 [**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)的實例。 |
| [**IViewProvider**](/previous-versions//hh438426(v=vs.85)) | 表示應用程式中的視圖。 |
| [**IViewProviderFactory**](/previous-versions//hh438427(v=vs.85)) | 建立會執行 [**IViewProvider**](/previous-versions//hh438426(v=vs.85)) 介面的視圖實例。 |
| [**IVirtualSurfaceImageSourceNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) | 針對 DirectX 繪圖的) 共用介面，提供大量 (大於螢幕大小的實。 |
| [**IVirtualSurfaceUpdatesCallbackNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative) | 提供當 [**virtualsurfaceimagesource 這是**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) 要求更新時，繪製行為的介面。 |
| [**IWeakReference**](/windows/win32/api/weakreference/nn-weakreference-iweakreference) | 代表物件的弱式參考。 |
| [**IWeakReferenceSource**](/windows/win32/api/weakreference/nn-weakreference-iweakreferencesource) | 表示可從中抓取弱式參考的來源物件。 |
| [**MapChangedEventHandler<K，V>**](/previous-versions//br224612(v=vs.85)) | 表示處理可觀察對應之 [**MapChanged**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) 事件的方法。 |
| [**VectorChangedEventHandler &lt; T&gt;**](/previous-versions//br224626(v=vs.85)) | 表示處理可觀察向量之 [**VectorChanged**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) 事件的方法。 |
