---
description: Windows 執行階段 c + + 函式的參考。
ms.assetid: 3D60C81F-B1CC-4485-B7C3-B1C6E903865B
title: '函數 (Windows 執行階段) '
ms.topic: article
ms.date: 05/10/2019
ms.openlocfilehash: 1ed2ea39385ac5cb7afc34770a5ee2d2a572bb8b
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106979626"
---
# <a name="functions-windows-runtime-c-reference"></a>函數 (Windows 執行階段 c + + 參考) 

## <a name="in-this-section"></a>本節內容



| 函式 | 描述 |
|-|-|
| [**CoDecodeProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy) | 在指定介面給 proxy 物件的伺服器進程中，找出元件物件模型的實 (COM) 介面。 |
| [**CreateControlInput**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinput) | 在呼叫端的 UI 執行緒中，建立 [**ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) 物件。 |
| [**CreateControlInputEx**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinputex) | 在背景工作執行緒或 UI 執行緒中，建立 [**ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) 物件。  |
| [**CreateDirect3D11DeviceFromDXGIDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) | 從 IDXGIDevice 建立 IDirect3DDevice 的實例。 |
| [**CreateDirect3D11SurfaceFromDXGISurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11surfacefromdxgisurface) | 從 IDXGISurface 建立 IDirect3DSurface 的實例。 |
| [**CreateDirect3DDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3ddevice) | 從[IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)建立[IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice)的實例。 |
| [**CreateDirect3DSurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3dsurface) | 從[IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)建立[IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface)的實例。 |
| [**CreateRandomAccessStreamOnFile**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamonfile) | 建立檔案的 Windows 執行階段隨機存取資料流程。 |
| [**CreateRandomAccessStreamOverStream**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamoverstream) | 在 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 基底執行周圍建立 Windows 執行階段隨機存取資料流程。 |
| [**CreateStreamOverRandomAccessStream**](/windows/win32/api/shcore/nf-shcore-createstreamoverrandomaccessstream) | 在 Windows 執行階段 [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85))物件周圍建立 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 。 |
| [**CreateXamlUIPresenter**](createxamluipresenter.md) | 靜態 creator 函式，可在桌面應用程式中建立呈現介面的 [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) 。 |
| [**DbgRaiseAssertionFailure**](/previous-versions//jj635749(v=vs.85)) | 引發要進行偵錯工具的判斷提示。  |
| [**GetDXGIInterface (IDirect3DDevice ^，DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface) | 從 [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) 實例中抓取 DXGI 介面。 |
| [**GetDXGIInterface (IDirect3DSurface ^，DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface-r1) | 從 [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) 實例中抓取 DXGI 介面。 |
| [**GetDXGIInterfaceFromObject**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterfacefromobject) | 從物件捕獲 DXGI 介面。 |
| [**GetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo) | 取得在目前的邏輯執行緒中，由先前呼叫 [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) 所設定的受限制的錯誤資訊物件。 |
| [**HSTRING \_ UserFree**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree) | 由 RPC 存根檔案呼叫時，釋放伺服器端上的資源。 |
| [**HSTRING \_ UserFree64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree64) | 由 RPC 存根檔案呼叫時，釋放伺服器端上的資源。  |
| [**HSTRING \_ UserMarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal) | 將 [**HSTRING**](hstring.md) 物件封送處理至 RPC 緩衝區。 |
| [**HSTRING \_ UserMarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal64) | 將 [**HSTRING**](hstring.md) 物件封送處理至 RPC 緩衝區。 |
| [**HSTRING \_ UserSize**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize) | 計算 [**HSTRING**](hstring.md) 物件的網路大小，並取得其控制碼和資料。 |
| [**HSTRING \_ UserSize64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize64) | 計算 [**HSTRING**](hstring.md) 物件的網路大小，並取得其控制碼和資料。 |
| [**HSTRING \_ UserUnmarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal) | 從 RPC 緩衝區拆收 [**HSTRING**](hstring.md) 物件。 |
| [**HSTRING \_ UserUnmarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal64) | 從 RPC 緩衝區拆收 [**HSTRING**](hstring.md) 物件。 |
| [**IsErrorPropagationEnabled**](/windows/win32/api/roerrorapi/nf-roerrorapi-iserrorpropagationenabled) | 指出針對 Windows 執行階段 API 事件或完成非同步方法而註冊為回呼函式的委派所傳回的錯誤，是否會發生 [**CoreApplication. UnhandledErrorDetected**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) 事件。 |
| [**DllGetActivationFactory**](/previous-versions//br205771(v=vs.85)) | 從包含可啟動的 Windows 執行階段類別的 DLL 抓取啟用 factory。 |
| [**Rometadata.h**](/windows/win32/api/rometadata/nf-rometadata-metadatagetdispenser) | 建立分配器類別。 |
| [**PdfCreateRenderer**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfcreaterenderer) | 取得 [**IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) 介面的實例，以顯示可攜檔案格式的單一頁面 (PDF) 檔。 |
| [**PdfRenderParams**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfrenderparams) | 填入 [**PDF \_ 呈現 \_ 參數**](/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params) 結構。 PDF 轉譯 \_ \_ 參數結構代表一組用於輸出 PDF 檔案單一頁面的屬性。 |
| [**RoActivateInstance**](/windows/win32/api/roapi/nf-roapi-roactivateinstance) | 啟用指定的 Windows 執行階段類別。 |
| [**RoCaptureErrorCoNtext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext) | 儲存目前的錯誤內容，使其可供稍後呼叫 [**RoFailFastWithErrorCoNtext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) 函數。 |
| [**RoClearError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roclearerror) | 從目前的執行緒環境區塊移除現有的錯誤資訊 (TEB) 。 |
| [**RoFailFastWithErrorCoNtext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) | 在目前的進程中引發不可持續性例外狀況。 |
| [**RoFailFastWithErrorCoNtextInternal2**](./roerrorapi/nf-roerrorapi-rofailfastwitherrorcontextinternal2.md) | 在目前的進程中引發不可持續性例外狀況，也可讓您包含作業系統尚未捕捉的其他錯誤內容。 |
| [**RoFreeParameterizedTypeExtra**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rofreeparameterizedtypeextra) | 釋放 [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid)所配置的控制碼。 |
| [**RoGetActivatableClassRegistration**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration) | 啟用抓取類別註冊資訊。 |
| [**RoGetActivationFactory**](/windows/win32/api/roapi/nf-roapi-rogetactivationfactory) | 取得所指定執行時間類別的啟用 factory。 |
| [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) | 為指定介面所指定的物件建立 agile 參考。 |
| [**RoGetApartmentIdentifier**](/windows/win32/api/roapi/nf-roapi-rogetapartmentidentifier) | 取得目前單元的唯一識別碼。 |
| [**RoGetBufferMarshaler**](/windows/win32/api/robuffer/nf-robuffer-rogetbuffermarshaler) | 提供標準 Windows.storage.streams.ibuffer 封送處理器，以在封送處理時，執行與 Windows.storage.streams.ibuffer 介面相關聯的語法。 |
| [**RoGetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags) | 取得 Windows 執行階段錯誤函式目前的報告行為。 |
| [**RoGetMetaDataFile**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile) | 找出並抓取中繼資料檔案，該檔案會描述指定之 typename 的應用程式二進位介面 (ABI) 。 |
| [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) | 計算當參數化介面或委派以指定的型別引數具現化時，所產生之介面或委派類型 (IID) 的介面識別碼。 |
| [**RoGetServerActivatableClasses**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetserveractivatableclasses) | 抓取為指定的可執行檔註冊的可啟動類別 (EXE) server，該伺服器是在呼叫進程的封裝識別碼下註冊。 |
| [**RoInitialize**](/windows/win32/api/roapi/nf-roapi-roinitialize) | 使用指定的並行模型，初始化目前線程上的 Windows 執行階段。 |
| [**RoInspectThreadErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo) | 取得錯誤物件，此物件表示發生錯誤之位置的呼叫堆疊 |
| [**RoInspectCapturedStackBackTrace**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace) | 提供一種方式，讓偵錯工具從目標進程檢查呼叫堆疊。 |
| [**RoOriginateError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerror) | 向附加的偵錯工具報告錯誤和有資訊的字串。 |
| [**RoOriginateErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerrorw) | 向附加的偵錯工具報告錯誤和有資訊的字串。 |
| [**RoOriginateLanguageException**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception) | 向附加的偵錯工具報告錯誤、資訊性字串和錯誤物件。 |
| [**RoParameterizedTypeExtraGetTypeSignature**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-roparameterizedtypeextragettypesignature) | 取得型別簽章，用來計算上次呼叫 [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) 與指定之控制碼的 IID。 |
| [**RoParseTypeName**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roparsetypename) | 剖析型別名稱和現有的型別參數（如果是參數化型別）。 |
| [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) | 針對 Windows 執行階段 exe 伺服器，註冊陣列跨進程啟動處理站。 |
| [**RoRegisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-roregisterforapartmentshutdown) | 註冊當目前的單元關閉時要叫用的 [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) 回呼。 |
| [**RoReportUnhandledError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportunhandlederror) | 發生未處理的例外狀況時，觸發全域錯誤處理常式。 |
| [**RoReportFailedDelegate**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportfaileddelegate) | 發生委派失敗時，觸發全域錯誤處理常式。 |
| [**Rometadataresolution.h roresolvenamespace**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roresolvenamespace) | 從 Windows 執行階段所支援的任何程式設計語言，判斷指定之 Windows 執行階段命名空間的直接子系、類型和子命名空間。 |
| [**RoResolveRestrictedErrorInfoReference**](/windows/win32/api/roerrorapi/nf-roerrorapi-roresolverestrictederrorinforeference) | 根據給定的參考傳回 [**IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) 介面指標。 |
| [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) | 從 Windows 執行階段中移除已註冊之啟用 factory 的陣列。 |
| [**RoSetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags) | 設定 Windows 執行階段錯誤函式的報告行為。 |
| [**RoTransformError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerror) | 將修改過的錯誤和資訊性字串報告至附加的偵錯工具。 |
| [**RoTransformErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerrorw) | 將已轉換的錯誤和資訊性字串報告至附加的偵錯工具。 |
| [**RoUninitialize**](/windows/win32/api/roapi/nf-roapi-rouninitialize) | 關閉目前線程上的 Windows 執行階段。 |
| [**RoUnregisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-rounregisterforapartmentshutdown) | 取消註冊先前註冊的 [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) 介面。 |
| [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) | 為目前的執行緒設定受限制的錯誤資訊物件。 |
| [**WindowsCompareStringOrdinal**](/windows/win32/api/winstring/nf-winstring-windowscomparestringordinal) | 比較兩個指定的 [**HSTRING**](hstring.md) 物件，並傳回一個整數，指出它們在排序次序中的相對位置。 |
| [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) | 串連兩個指定的字串。 |
| [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) | 根據指定的來源字串，建立新的 [**HSTRING**](hstring.md) 。 |
| [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) | 根據指定的字串建立新的字串參考。 |
| [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) | 遞減字串緩衝區的參考計數。 |
| [**WindowsDeleteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowsdeletestringbuffer) | 如果未升級為 [**HSTRING**](hstring.md)，則會捨棄預先配置的字串緩衝區。 |
| [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) | 建立指定字串的複本。 |
| [**WindowsGetStringLen**](/windows/win32/api/winstring/nf-winstring-windowsgetstringlen) | 取得指定之字串的長度（以 Unicode 字元為單位）。 |
| [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) | 取得指定之字串的支援緩衝區。 |
| [**WindowsInspectString**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring) | 提供一種方式，讓偵錯工具顯示另一個位址空間、遠端或傾印中 Windows 執行階段 [**HSTRING**](hstring.md) 的值。  |
| [**WindowsInspectString2**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring2) | 提供一種方式，讓偵錯工具顯示另一個位址空間、遠端或傾印中 Windows 執行階段 [**HSTRING**](hstring.md) 的值。  |
| [**WindowsIsStringEmpty**](/windows/win32/api/winstring/nf-winstring-windowsisstringempty) | 指出指定的字串是否為空字串。 |
| [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) | 配置可變動的字元緩衝區，以便在建立 [**HSTRING**](hstring.md) 時使用。 |
| [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) | 從指定的 [**HSTRING \_ 緩衝區**](hstring-buffer.md)建立 [**HSTRING**](hstring.md) 。 |
| [**WindowsReplaceString**](/windows/win32/api/winstring/nf-winstring-windowsreplacestring) | 以另一組字元取代指定之字串中一組字元的所有出現專案，以建立新的字串。 |
| [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) | 指出指定的字串是否具有內嵌的 null 字元。 |
| [**WindowsSubstring**](/windows/win32/api/winstring/nf-winstring-windowssubstring) | 從指定的字串抓取子字串。 子字串會從指定的字元位置開始。 |
| [**WindowsSubstringWithSpecifiedLength**](/windows/win32/api/winstring/nf-winstring-windowssubstringwithspecifiedlength) | 從指定的字串抓取子字串。 子字串起始於指定的字元位置，並且具有指定的長度。 |
| [**WindowsTrimStringEnd**](/windows/win32/api/winstring/nf-winstring-windowstrimstringend) | 從來源字串中移除所有尾端出現的指定字元組。 |
| [**WindowsTrimStringStart**](/windows/win32/api/winstring/nf-winstring-windowstrimstringstart) | 從來源字串中移除所有開頭出現的指定字元組。 |



 

 

 
