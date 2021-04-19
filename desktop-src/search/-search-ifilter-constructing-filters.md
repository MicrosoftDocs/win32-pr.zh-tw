---
description: 請務必瞭解篩選處理常式的必要 DLL 結構， (IFilter 介面的執行) 。
ms.assetid: a2b5a813-573a-44d3-8780-99603e3246c1
title: 在 Windows Search 中執行篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5f326440b31b62ff5697274962f4d4a2cfe7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970383"
---
# <a name="implementing-filter-handlers-in-windows-search"></a>在 Windows Search 中執行篩選處理常式

請務必瞭解篩選處理常式的必要 DLL 結構， ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行) 。

本主題的組織方式如下：

- [執行和匯出 DLL 進入點](#implementing-and-exporting-the-dll-entry-points)
- [執行 IFilter 類別和 Class Factory](#implementing-the-ifilter-class-and-class-factory)
- [繼承 COM 介面](#inheriting-the-com-interfaces)
- [執行 COM 介面方法](#implementing-the-com-interface-methods)
  - [未執行的 COM 方法](#com-methods-that-are-not-implemented)
- [其他資源](#additional-resources)
- [相關主題](#related-topics)

## <a name="implementing-and-exporting-the-dll-entry-points"></a>執行和匯出 DLL 進入點

此區段中的 Ifilter.dll 所表示的每個 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL () 必須執行和匯出下列進入點。 這些進入點通常會使用 () 的 **IFilter** 介面或使用 **\_ \_ declspec (dllexport)** 關鍵字的模組定義來匯出。 DLL 檔案可以註冊在任何資料夾中，但通常位於% SystemRoot% \\ system32 資料夾中。

下表列出並描述 DLL 進入點。

| DLL 名稱                                                                                     | DLL 描述                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver)            | [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver)進入點會將 DLL 註冊為登錄中的篩選準則。 您可以藉由以 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面 DLL 檔案名作為引數來執行 regsvr32.exe 程式，以註冊 DLL： `regsvr32.exe %SystemRoot%\system32\Ifilter.dll`                                              |
| [DllUnregisterServer 函式](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) | [DllUnregisterServer](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)函式進入點會移除 DLL 做為登錄中的持續性處理常式。 您可以使用旗標執行 regsvr32.exe 程式，以取消註冊 DLL `/u` ： `regsvr32.exe /u %SystemRoot%\system32\Ifilter.dll`                                                                                    |
| [DllGetClassObject 函式](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)   | 內容編制索引用戶端會透過元件物件模型 (COM) 來呼叫 [DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式進入點，以建立 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的 class factory 物件，並取得該物件的 class factory 介面指標。                                               |
| [DllCanUnloadNow 函式](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)     | 內容索引用戶端會透過 COM 呼叫 [DllCanUnloadNow](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) 函式進入點，以判斷是否可以卸載 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  DLL。 如果 **IFilter** 介面未使用一段時間，就會卸載，如 FilterIdleTimeOut 登錄值所指定。 |

## <a name="implementing-the-ifilter-class-and-class-factory"></a>執行 IFilter 類別和 Class Factory

至少有兩個類別（例如 CFilter 和 CFilterCF）通常會由每個 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL 來執行。 CFilter 類別會產生可執行內容篩選功能的 **IFilter** 介面物件。 它的成員函式會執行 **IFilter** 介面的介面方法。 每個 **ifilter** 類別都需要 (CLSID 介面所產生之 CLSID) **的唯一** 類別識別碼。

CFilterCF 類別會產生 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的 class factory 物件。 藉由 DLL 的[DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)函式進入點，會透過其[IClassFactory 介面](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)介面呼叫 class factory。 CFilterCF 類別會建立 CFilter 物件，並將指標傳回至 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)。 在更複雜的情況下， **IFilter** 可以執行類別階層來取代單一 CFilter 類別。

## <a name="inheriting-the-com-interfaces"></a>繼承 COM 介面

Windows Search 3.0 和更新版本要求您使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 的原因如下：

- 以確保效能和未來的相容性。
- 有助於提高安全性。 使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 執行的 ifilter 比較安全，因為 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面執行所在的內容不需要在磁片上或透過網路開啟檔案的許可權。
- 雖然 Windows Search 只使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)，但 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面類別別也可以繼承 [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile) 和/或 [IPersistStorage 介面](/windows/win32/api/objidl/nn-objidl-ipersiststorage) 介面，以提供回溯相容性。

這些介面是在 mssdk include 目錄所包含的檔案中宣告 \\ ，並且具有預先定義的介面識別碼， (iid) 。 內容編制索引用戶端會透過 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)查詢 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面，以判斷在篩選內容時要使用的介面。

## <a name="implementing-the-com-interface-methods"></a>執行 COM 介面方法

[**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面會針對 **ifilter** 介面類別別和 **ifilter** 介面 class factory，同時執行 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法。 下表依 vtable 順序列出 **ifilter** 介面所應執行的 **ifilter** 介面特定介面和方法。 **IFilter** 介面必須執行至少 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)，但可以執行其他 IPersist 衍生的介面。

| COM 介面                                                                             | 方法                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IClassFactory 介面](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)   | CreateInstance、LockServer                                                                                                                                                                                                                                                     |
| [IClassFactory2 介面](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)  | GetLicInfo, RequestLicKey, CreateInstanceLic                                                                                                                                                                                                                                   |
| [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)                                                        | [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)、 [**Ifilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)、 [**IFilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)、 [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue)、 [**IFilter：： BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) |
| [IPersist 介面](/windows/desktop/api/objidl/nn-objidl-ipersist)               | GetClassID                                                                                                                                                                                                                                                                     |
| [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile)    | IsDirty、Load、Save、SaveCompleted、GetCurFile                                                                                                                                                                                                                                 |
| [IPersistStorage 介面](/windows/win32/api/objidl/nn-objidl-ipersiststorage) | IsDirty、載入、儲存、GetSizeMax                                                                                                                                                                                                                                                |
| [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)            | IsDirty、載入、儲存、GetSizeMax                                                                                                                                                                                                                                                |

每個方法的參考頁面會指定該方法的參數和功能行為。 每個參考頁面也會提供要針對該方法執行的結果碼。 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)方法的參考頁面提供 [設備 \_ ITF](../com/codes-in-facility-itf.md)結果碼中所要執行的介面特定程式碼，而內容索引用戶端也可以處理任何一般結果碼，例如設備 \_ Null 和設備 \_ WIN32。 如需詳細資訊，請參閱 [COM 錯誤碼的結構](../com/structure-of-com-error-codes.md)。

### <a name="com-methods-that-are-not-implemented"></a>未執行的 COM 方法

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面必須執行至少 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)，但不需要執行其他 IPersist 衍生的介面。

Windows Search 不需要執行下表所列的 COM 方法。

| 不需要的方法                               | Description                       |
|-----------------------------------------------------------|-----------------------------------|
| IPersistStream：： IsDirty                                   | 篩選應該會傳回 E \_ >notimpl。 |
| IPersistStream：： Save                                      | 篩選應該會傳回 E \_ >notimpl。 |
| IPersistStream：： GetSizeMax                                | 篩選應該會傳回 E \_ >notimpl。 |
| [**IFilter：： BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | 篩選應該會傳回 E \_ >notimpl。 |

## <a name="additional-resources"></a>其他資源

- [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例會示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基礎類別。
- 如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。
- 如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。
- 若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。

## <a name="related-topics"></a>相關主題

[開發篩選處理常式](-search-ifilter-conceptual.md)

[瞭解 Windows Search 中的篩選處理常式](-search-ifilter-about.md)

[在 Windows Search 中建立篩選處理常式的最佳作法](-search-3x-wds-extidx-filters.md)

[從篩選處理常式傳回屬性](-search-ifilter-property-filtering.md)

[Windows 隨附的篩選處理常式](-search-ifilter-implementations.md)

[註冊篩選處理常式](-search-ifilter-registering-filters.md)

[測試篩選處理常式](-search-ifilter-testing-filters.md)
