---
description: 使用 COM 進行 DirectX 程式設計。
title: 使用 COM 進行 DirectX 程式設計
ms.topic: article
ms.date: 01/29/2019
ms.openlocfilehash: 67fc7a35f42439e1a9eeef1b2895d88dc0dbf5d4
ms.sourcegitcommit: f712e5fed19d6afe2762a77ffcdf8b5977f85901
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "103945533"
---
# <a name="programming-directx-with-com"></a>使用 COM 進行 DirectX 程式設計

Microsoft 元件物件模型 (COM) 是數種技術所使用的物件導向程式設計模型，包括大量的 DirectX API 介面。 基於這個理由，您 (為 DirectX 開發人員) 在程式設計 DirectX 時，不一定要使用 COM。

> [!NOTE]
> 使用 [COM 元件與 c + +/WinRT](/windows/uwp/cpp-and-winrt-apis/consume-com) 的主題) 會示範如何使用 [c + +/WinRT](/windows/uwp/cpp-and-winrt-apis/) (和任何 COM API 來使用 DirectX api。 這是目前最方便使用和建議使用的技術。

或者，您也可以使用原始的 COM，這就是本主題的內容。 您將需要對使用 COM Api 的原則和程式設計技術有基本的瞭解。 雖然 COM 的聲譽很困難且複雜，但大部分 DirectX 應用程式所需的 COM 程式設計很簡單。 在部分情況下，這是因為您將使用 DirectX 提供的 COM 物件。 您不需要撰寫自己的 COM 物件，這通常會發生複雜度。

## <a name="com-component-overview"></a>COM 元件總覽

COM 物件基本上是功能的封裝元件，可供應用程式用來執行一或多個工作。 針對部署，會將一或多個 COM 元件封裝成稱為 COM 伺服器的二進位檔;通常比 DLL 更多。

傳統的 DLL 會匯出免費的函式。 COM 伺服器可以這樣做。 但是 COM 伺服器內的 COM 元件會公開 COM 介面和屬於這些介面的成員方法。 您的應用程式會建立 COM 元件的實例、從中抓取介面，以及在這些介面上呼叫方法，以受益于 COM 元件中所執行的功能。

在實務上，這似乎類似于在一般 c + + 物件上呼叫方法。 但有一些差異。

- COM 物件會強制執行比 c + + 物件更嚴格的封裝。 您無法只建立物件，然後呼叫任何公用方法。 相反地，COM 元件的公用方法會分組為一或多個 COM 介面。 若要呼叫方法，您可以建立物件，並從物件取出實作為方法的介面。 介面通常會執行一組相關的方法，以提供物件特定功能的存取權。 例如， [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) 介面代表一個虛擬圖形介面卡，其中包含可讓您建立資源的方法，例如，以及許多其他與介面卡相關的工作。
- COM 物件的建立方式與 c + + 物件的方式相同。 有幾種方式可以建立 COM 物件，但全都牽涉到 COM 專屬的技巧。 DirectX API 包含各種協助程式函式和方法，可簡化大部分的 DirectX COM 物件的建立工作。
- 您必須使用 COM 特定的技術來控制 COM 物件的存留期。
- COM 伺服器 (通常不需要明確載入 DLL) 。 您也可以連結到靜態程式庫，以便使用 COM 元件。 每個 COM 元件都有唯一的註冊識別碼 (全域唯一識別碼或 GUID) ，您的應用程式會使用此識別碼來識別 COM 物件。 您的應用程式會識別元件，而 COM 執行時間會自動載入正確的 COM 伺服器 DLL。
- COM 是二進位規格。 您可以使用各種語言來撰寫和存取 COM 物件。 您不需要知道物件原始程式碼的任何相關資訊。 例如，Visual Basic 的應用程式會定期使用以 c + + 撰寫的 COM 物件。

## <a name="component-object-and-interface"></a>元件、物件和介面

請務必瞭解元件、物件和介面之間的差異。 在偶爾使用的情況下，您可能會聽到其主體介面名稱所參考的元件或物件。 但是這些詞彙不是可互換的。 元件可以執行任意數目的介面;而物件是元件的實例。 例如，雖然所有元件都必須執行 [**IUnknown 介面**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)，但它們通常會執行至少一個額外的介面，而且它們可能會實作為多個介面。

若要使用特定的介面方法，您不能只具現化物件，您也必須從它取得正確的介面。

此外，有一個以上的元件可能會執行相同的介面。 介面是一組方法，可執行邏輯相關的作業集合。 介面定義只會指定方法的語法及其一般功能。 任何需要支援一組特定作業的 COM 元件都可以藉由執行適當的介面來執行此作業。 某些介面具有高度特製化，而且只能由單一元件執行;其他在各種情況下都很有用，而且是由許多元件所執行。

如果元件會執行介面，則必須支援介面定義中的每個方法。 換句話說，您必須能夠呼叫任何方法，並確信它存在。 不過，特定方法的執行方式詳細資料可能會與另一個元件不同。 例如，不同的元件可能會使用不同的演算法來到達最終結果。 也不保證會以重要的方式支援方法。 有時候，元件會實作為常用的介面，但它只需要支援方法的子集。 您仍然可以成功呼叫其餘的方法，但是會傳回 [**HRESULT**](#hresult-values) (，這是代表結果碼的標準 COM 型別，) 包含 **E_NOTIMPL** 值的結果碼。 您應該參考其檔，以查看介面如何由任何特定元件來執行。

COM 標準需要介面定義在發行之後不能變更。 例如，作者無法將新的方法加入至現有的介面。 作者必須改為建立新的介面。 雖然該介面中的方法沒有任何限制，但常見的作法是讓下一代介面包含舊介面方法的所有方法，再加上任何新的方法。

介面不尋常有數個層代。 一般而言，所有世代的執行基本上都是相同的整體工作，但它們在細節方面不同。 COM 元件通常會在每個目前和先前產生的指定介面歷程中進行。 這麼做可讓較舊的應用程式繼續使用物件的舊版介面，而較新的應用程式可以利用較新介面的功能。 一般而言，介面的下降群組全都具有相同的名稱，加上指出世代的整數。 例如，如果原始介面命名為 **IMyInterface** (意指第1代) ，則接下來的兩個層代會稱為 **IMyInterface2** 和 **IMyInterface3**。 在 DirectX 介面的情況下，後續的世代通常會命名為 DirectX 的版本號碼。

## <a name="guids"></a>GUID

Guid 是 COM 程式設計模型的重要部分。 在最基本的情況下，GUID 是128位的結構。 不過，Guid 的建立方式，是為了保證兩個 Guid 都不相同。 COM 會將 Guid 廣泛使用於兩個主要用途。

- 唯一識別特定的 COM 元件。 指派用來識別 COM 元件的 GUID 稱為)  (CLSID 的識別碼，當您想要建立相關聯之 COM 元件的實例時，可以使用 CLSID。
- 唯一識別特定的 COM 介面。 指派用來識別 COM 介面的 GUID 稱為 (IID) 的介面識別碼，當您從元件的實例要求特定介面時，您會使用 IID)  (物件。 無論哪個元件會執行介面，介面的 IID 都會相同。

為了方便起見，DirectX 檔通常會以描述性名稱參考元件和介面 (例如， **ID3D12Device**) ，而不是其 guid。 在 DirectX 檔的內容中，不會有任何混淆。 技術上來說，協力廠商有可能會以描述性名稱 **ID3D12Device** 來撰寫介面 (必須有不同的 IID 才能成為有效的) 。 不過，為了清楚起見，我們不建議這麼做。

因此，唯一參考特定物件或介面的唯一方法是透過其 GUID。

雖然 GUID 是一個結構，但是 GUID 通常是以對等字串形式來表示。 GUID 字串形式的一般格式為32十六進位數位，格式為8-4-4-4-12。 也就是 {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}，其中每個 x 都對應到一個十六進位數位。 例如， **ID3D12Device** 介面的 IID 字串形式為 {189819F1-1DB6-4B57-BE54-1821339B85F7}。

因為實際的 GUID 有點笨拙，而且很容易出錯，所以通常也會提供對等的名稱。 在您的程式碼中，當您呼叫函式時（例如，當您將參數的引數傳遞給 D3D12CreateDevice），就可以使用這個名稱來取代實際的結構 `riid` 。 [](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) 慣例命名慣例是分別在介面或物件的描述性名稱前面加上 IID_ 或 CLSID_。 例如， **ID3D12Device** 介面的 IID 名稱是 IID_ID3D12Device。

> [!NOTE]
> DirectX 應用程式應與 ``dxguid.lib`` 和連結， ``uuid.lib`` 以提供各種介面和類別 guid 的定義。 Visual C++ 和其他編譯器支援 **__uuidof** 運算子語言延伸模組，但與這些程式庫的明確 C 樣式連結也受到支援且可完整移植。

## <a name="hresult-values"></a>HRESULT 值

大部分的 COM 方法會傳回稱為 **HRESULT** 的32位整數。 使用大部分的方法時，HRESULT 基本上是包含兩個主要資訊片段的結構。
- 方法是否成功或失敗。
- 方法所執行之作業結果的詳細資訊。

某些方法會從所定義的標準集傳回 **HRESULT** 值 `Winerror.h` 。 但是，方法可以用來傳回自訂的 **HRESULT** 值，並提供更多特製化的資訊。 這些值通常會記載在方法的參考頁面上。

您在方法參考頁面上找到的 **HRESULT** 值清單通常只是可能傳回的可能值子集。 此清單通常只會涵蓋方法特有的值，以及具有某些特定方法意義的標準值。 您應該假設某個方法可能會傳回各種標準 **HRESULT** 值，即使這些值未明確記載也是一樣。

雖然 **HRESULT** 值通常用來傳回錯誤資訊，但您不應該將它們視為錯誤碼。 表示成功或失敗的位會與包含詳細資訊的位分開儲存，讓 **HRESULT** 值具有任何數目的成功和失敗代碼。 依照慣例，成功碼的名稱前面會加上 S_ 和失敗代碼，E_。 例如，兩個最常使用的程式碼是 S_OK 並 E_FAIL，分別表示簡單的成功或失敗。

COM 方法可能會傳回各種成功或失敗的程式碼，這表示您必須小心測試 **HRESULT** 值。 例如，假設有一個假設性的方法，其中包含已記載的 S_OK 的傳回值，如果成功，則 E_FAIL。 不過，請記住，此方法可能也會傳回其他失敗或成功碼。 下列程式碼片段說明使用簡單測試的風險，其中 `hr` 包含方法所傳回的 **HRESULT** 值。

```cpp
if (hr == E_FAIL)
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

只要在失敗的情況下，此方法只會傳回 E_FAIL (，而不是) 其他失敗代碼，則這項測試會正常運作。 但是，為了傳回一組特定的失敗代碼（可能是 E_NOTIMPL 或 E_INVALIDARG），會更實際地執行指定的方法。 使用上述程式碼，這些值將會不正確地解讀為成功。

如果您需要有關方法呼叫結果的詳細資訊，您需要測試每個相關的 **HRESULT** 值。 不過，您可能只對方法是否成功或失敗感興趣。 測試 **HRESULT** 值是否會指出成功或失敗的健全方式，是將值傳遞至下列其中一個在 winerror.h 中定義的宏。

- `SUCCEEDED`宏會針對成功碼傳回 TRUE，並針對失敗碼傳回 FALSE。
- `FAILED`針對失敗代碼，宏會傳回 TRUE，若為成功碼，則會傳回 FALSE。

因此，您可以使用宏來修正上述程式碼片段 `FAILED` ，如下列程式碼所示。

```cpp
if (FAILED(hr))
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

此更正的程式碼片段會適當地將 E_NOTIMPL 和 E_INVALIDARG 視為失敗。

雖然大部分的 COM 方法會傳回結構化的 **hresult** 值，但較小的數位會使用 **HRESULT** 傳回簡單的整數。 這些方法一律會成功。 如果您將此排序的 **HRESULT** 傳遞至成功的宏，則宏一律會傳回 TRUE。 不會傳回 **HRESULT** 的一般呼叫方法範例是 **IUnknown：： Release** 方法，它會傳回 ULONG。 這個方法會將物件的參考計數遞減1，並傳回目前的參考計數。 如需參考計數的討論，請參閱 [管理 COM 物件的存留期](#managing-a-com-objects-lifetime) 。

## <a name="the-address-of-a-pointer"></a>指標的位址

如果您看到幾個 COM 方法參考頁面，您可能會在類似下面的內容上執行。

```cpp
HRESULT D3D12CreateDevice(
  IUnknown          *pAdapter,
  D3D_FEATURE_LEVEL MinimumFeatureLevel,
  REFIID            riid,
  void              **ppDevice
);
```

雖然 C/c + + 開發人員很熟悉一般指標，但 COM 通常會使用額外的間接取值層級。 第二個層級的間接取值是由兩個星號（在類型宣告之後）來表示， `**` 而變數名稱通常會有前置詞 `pp` 。 針對上面的函式， `ppDevice` 參數通常稱為 void 的指標位址。 實際上，在此範例中， `ppDevice` 是 **ID3D12Device** 介面指標的位址。

與 c + + 物件不同的是，您不會直接存取 COM 物件的方法。 您必須改為取得介面的指標，該介面會公開方法。 若要叫用方法，基本上使用的語法與叫用 c + + 方法指標的語法相同。 例如，若要叫用 **IMyInterface：:D osomething** 方法，您可以使用下列語法。

```cpp
IMyInterface * pMyIface = nullptr;
...
pMyIface->DoSomething(...);
```

第二層間接取值的需求來自于您未直接建立介面指標的事實。 您必須呼叫其中一種方法，例如上面所示的 **D3D12CreateDevice** 方法。 若要使用這類方法來取得介面指標，您可以將變數宣告為所需介面的指標，然後將該變數的位址傳遞給方法。 換句話說，您會將指標的位址傳遞給方法。 當方法傳回時，變數會指向要求的介面，您可以使用該指標來呼叫任何介面的方法。

```cpp
IDXGIAdapter * pIDXGIAdapter = nullptr;
...
ID3D12Device * pD3D12Device = nullptr;
HRESULT hr = ::D3D12CreateDevice(
    pIDXGIAdapter,
    D3D_FEATURE_LEVEL_11_0,
    IID_ID3D12Device,
    &pD3D12Device);
if (FAILED(hr)) return E_FAIL;

// Now use pD3D12Device in the form pD3D12Device->MethodName(...);
```

## <a name="creating-a-com-object"></a>建立 COM 物件

建立 COM 物件的方式有好幾種。 這些是 DirectX 程式設計中最常使用的兩個。

- 間接地呼叫為您建立物件的 DirectX 方法或函式。 方法會建立物件，並傳回物件上的介面。 當您以這種方式建立物件時，有時您可以指定應該傳回的介面，其他時候則會隱含介面。 上述程式碼範例顯示如何間接建立 Direct3D 12 裝置 COM 物件。
- 直接將物件的 CLSID 傳遞至 [**CoCreateInstance 函數**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。 此函式會建立物件的實例，並將指標傳回您指定的介面。

一次，在您建立任何 COM 物件之前，必須先呼叫 [**CoInitializeEx 函數**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)來初始化 com。 如果您要間接建立物件，則物件建立方法會處理這項工作。 但是，如果您需要建立具有 **CoCreateInstance** 的物件，則必須明確呼叫 **CoInitializeEx** 。 當您完成時，COM 必須藉由呼叫 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)來解除初始化。 如果您對 **CoInitializeEx** 進行呼叫，則必須與 **CoUninitialize** 的呼叫相符。 一般而言，需要明確初始化 COM 的應用程式會在其啟動常式中進行，並在其清除常式中將 COM 解除初始化。

若要使用 **CoCreateInstance** 來建立 COM 物件的新實例，您必須擁有物件的 CLSID。 如果此 CLSID 可公開取得，您將會在參考檔或適當的標頭檔中找到它。 如果 CLSID 無法公開使用，則您無法直接建立物件。

**CoCreateInstance** 函數有五個參數。 針對您將搭配 DirectX 使用的 COM 物件，您通常可以依照下列方式設定參數。

*rclsid* 將此設定為您想要建立之物件的 CLSID。

*pUnkOuter* 設定為 `nullptr` 。 只有當您要匯總物件時，才會使用這個參數。 COM 匯總的討論已超出本主題的範圍。

*dwClsCoNtext* 設定為 CLSCTX_INPROC_SERVER。 這項設定表示物件會實作為 DLL，並在您的應用程式進程中執行。

*riid* 設定為您想要傳回之介面的 IID。 函式會建立物件，並在 ppv 參數中傳回要求的介面指標。

*ppv* 將此設定為指標的位址，這個指標會設定為函式傳回時所指定的介面 `riid` 。 此變數應宣告為所要求介面的指標，而參數清單中指標的參考應轉換為 (LPVOID * ) 。

間接建立物件通常很簡單，如上述程式碼範例中所見。 您可以將物件建立方法傳遞給介面指標的位址，然後方法會建立物件並傳回介面指標。 當您間接建立物件時，即使您無法選擇該方法所傳回的介面，通常仍然可以指定如何建立物件的各種相關事項。

例如，您可以傳遞給 **D3D12CreateDevice** 值，指定所傳回裝置應該支援的最小 D3D 功能等級，如上述程式碼範例所示。

## <a name="using-com-interfaces"></a>使用 COM 介面

當您建立 COM 物件時，建立方法會傳回介面指標。 然後，您可以使用該指標來存取任何介面的方法。 語法與 c + + 方法的指標所使用的語法相同。

## <a name="requesting-additional-interfaces"></a>要求其他介面

在許多情況下，您從建立方法收到的介面指標可能是您唯一需要的介面指標。 事實上，物件只匯出 **IUnknown** 以外的一個介面相當常見。 不過，許多物件會匯出多個介面，而您可能需要其中一些介面的指標。 如果您需要的介面多於建立方法所傳回的介面，則不需要建立新的物件。 相反地，請使用物件的 [**IUnknown：： QueryInterface 方法**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void))來要求另一個介面指標。

如果您使用 **CoCreateInstance** 建立物件，則可以要求 **iunknown** 介面指標，然後呼叫 **iunknown：： QueryInterface** 要求您需要的每個介面。 但是，如果您只需要單一介面，這種方法就很不方便，如果您使用的物件建立方法不允許您指定應該傳回的介面指標，則這種方法並不適用。 在實務上，您通常不需要取得明確的 **iunknown** 指標，因為所有的 COM 介面都會擴充 **iunknown** 介面。

擴充介面在概念上類似于繼承自 c + + 類別。 子介面會公開所有父介面的方法，加上一或多個它自己的方法。 事實上，您通常會看到「繼承自」，而不是「擴充」。 您需要記住的是，繼承是物件內部的。 您的應用程式無法繼承或擴充物件的介面。 不過，您可以使用子系介面呼叫子系或父系的任何方法。

因為所有介面都是 **IUnknown** 的子系，所以您可以在任何已有物件的介面指標上呼叫 **QueryInterface** 。 當您這樣做時，必須提供所要求介面的 IID，以及當方法傳回時將包含介面指標的指標位址。

例如，下列程式碼片段會呼叫 **IDXGIFactory2：： CreateSwapChainForHwnd** 來建立主要交換鏈物件。 此物件會公開數個介面。 **CreateSwapChainForHwnd** 方法會傳回 **IDXGISwapChain1** 介面。 後續的程式碼接著會使用 **IDXGISwapChain1** 介面來呼叫 **QueryInterface** ，以要求 **IDXGISwapChain3** 介面。

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;
```

> [!NOTE]
> 在 c + + 中，您可以使用 ``IID_PPV_ARGS`` 宏，而不是明確的 IID 和 cast 指標： ``pDXGISwapChain1->QueryInterface(IID_PPV_ARGS(&pDXGISwapChain3));`` 。
> 這通常用於建立方法和 **QueryInterface**。 如需詳細資訊，請參閱[combaseapi。](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)

## <a name="managing-a-com-objects-lifetime"></a>管理 COM 物件的存留期

當建立物件時，系統會配置必要的記憶體資源。 當不再需要物件時，應該將它終結。 系統可以將該記憶體用於其他用途。 使用 c + + 物件時，您可以直接使用和運算子來控制物件的存留期 `new` `delete` ，因為您是在該層級運作，或是使用堆疊和範圍存留期。 COM 無法讓您直接建立或終結物件。 這項設計的原因是，相同的物件可能會由應用程式的多個部分使用，或在某些情況下由一個以上的應用程式使用。 如果其中一個參考是終結物件，則其他參考會變成無效。 相反地，COM 會使用參考計數系統來控制物件的存留期。

物件的參考計數是它的其中一個介面已被要求的次數。 每次要求介面時，參考計數就會遞增。 應用程式會在不再需要該介面時釋放介面，遞減參考計數。 只要參考計數大於零，物件就會保留在記憶體中。 當參考計數到達零時，物件就會終結本身。 您不需要知道物件參考計數的任何資訊。 只要您正確地取得和釋放物件的介面，物件將會有適當的存留期。

正確處理參考計數是 COM 程式設計的重要部分。 若未這麼做，可能會很容易造成記憶體流失或損毀。 COM 程式設計人員所做的最常見錯誤之一，就是無法釋放介面。 發生這種情況時，參考計數永遠不會到達零，而物件會無限期保留在記憶體中。

> [!NOTE]
> Direct3D 10 或更新版本有稍微修改物件的存留期規則。 尤其是，衍生自 **ID3DxxDeviceChild** 的物件絕不會存留時間其父裝置 (也就是，如果擁有 **ID3DxxDevice** 叫用 0 refcount，則所有子物件也會立即無效，) 。 此外，當您使用 **Set** 方法將物件系結至轉譯管線時，這些參考不會增加參考計數 (也就是) 的弱式參考。 在實務上，最好是在釋出裝置之前，確保您完全釋出所有裝置子物件。

## <a name="incrementing-and-decrementing-the-reference-count"></a>遞增和遞減參考計數

每當您取得新的介面指標時，參考計數都必須透過呼叫 [**IUnknown：： AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)來遞增。 不過，您的應用程式通常不需要呼叫此方法。 如果您藉由呼叫物件建立方法或呼叫 **IUnknown：： QueryInterface** 來取得介面指標，則物件會自動遞增參考計數。 但是，如果您以其他方式建立介面指標，例如複製現有的指標，則您必須明確地呼叫 **IUnknown：： AddRef**。 否則，當您釋出原始介面指標時，即使您仍然需要使用指標的複本，該物件仍可能會被破壞。

無論您或物件是否遞增參考計數，您都必須釋放所有介面指標。 當您不再需要介面指標時，請呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 來遞減參考計數。 常見的作法是將所有介面指標初始化為 `nullptr` ，然後在釋放時將其設定回 `nullptr` 。 該慣例可讓您測試清除程式碼中的所有介面指標。 那些未處於作用 `nullptr` 中狀態，而且您必須在終止應用程式之前釋放它們。

下列程式碼片段會擴充稍早所示的範例，以說明如何處理參考計數。

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3Copy = nullptr;

// Make a copy of the IDXGISwapChain3 interface pointer.
// Call AddRef to increment the reference count and to ensure that
// the object is not destroyed prematurely.
pDXGISwapChain3Copy = pDXGISwapChain3;
pDXGISwapChain3Copy->AddRef();
...
// Cleanup code. Check to see whether the pointers are still active.
// If they are, then call Release to release the interface.
if (pDXGISwapChain1 != nullptr)
{
    pDXGISwapChain1->Release();
    pDXGISwapChain1 = nullptr;
}
if (pDXGISwapChain3 != nullptr)
{
    pDXGISwapChain3->Release();
    pDXGISwapChain3 = nullptr;
}
if (pDXGISwapChain3Copy != nullptr)
{
    pDXGISwapChain3Copy->Release();
    pDXGISwapChain3Copy = nullptr;
}
```

## <a name="com-smart-pointers"></a>COM 智慧型指標

目前為止的程式碼已明確呼叫 ``Release`` 並 ``AddRef`` 使用 **IUnknown** 方法維護參考計數。 這種模式需要用心程式設計人員記住，才能在所有可能的 codepaths 中正確維護計數。 這可能會導致複雜的錯誤處理，而已啟用 c + + 例外狀況處理可能會特別難以實行。 使用 c + + 的較佳解決方案是利用 [智慧型指標](/cpp/cpp/smart-pointers-modern-cpp)。

* **winrt：： com_ptr** 是 [c + +/WinRT 語言投影](/uwp/cpp-ref-for-winrt/com-ptr)提供的智慧型指標。 這是建議用於 UWP 應用程式的 COM 智慧型指標。 請注意，c + +/WinRT 需要 c + + 17。

* **Microsoft：： WRL：： ComPtr** 是 [Windows 執行階段 C++ 範本庫 (WRL)](/cpp/cppcx/wrl/comptr-class)所提供的智慧型指標。 此程式庫是「純」 c + +，因此可用於透過 c + +/CX 或 c + +/WinRT) 以及傳統 Win32 桌面應用程式 (的 Windows 執行階段應用程式。 這個智慧型指標也適用于不支援 Windows 執行階段 Api 的較舊版本 Windows。 針對 Win32 桌面應用程式，您可以使用 ``#include <wrl/client.h>`` 僅包含此類別，並選擇性地定義預處理器符號 ``__WRL_CLASSIC_COM_STRICT__`` 。 如需詳細資訊，請參閱進行中的 [COM 智慧型指標](/archive/msdn-magazine/2015/february/windows-with-c-com-smart-pointers-revisited)。

* **CComPtr** 是 [Active Template Library (ATL)](/cpp/atl/reference/ccomptr-class)所提供的智慧型指標。 **Microsoft：： WRL：： ComPtr** 是此實作為的較新版本，可解決一些微妙的使用問題，因此不建議在新的專案中使用這個智慧型指標。 如需詳細資訊，請參閱 [如何建立和使用 CComPtr 和 CComQIPtr](/cpp/cpp/how-to-create-and-use-ccomptr-and-ccomqiptr-instances)。


## <a name="using-atl-with-directx-9"></a>使用 ATL 搭配 DirectX 9

若要使用 Active Template Library (ATL) 搭配 DirectX 9，您必須重新定義 ATL 相容性的介面。 這可讓您正確地使用 **CComQIPtr** 類別，以取得介面的指標。

您會知道是否未重新定義 ATL 的介面，因為您會看到下列錯誤訊息。

```
[...]\atlmfc\include\atlbase.h(4704) :   error C2787: 'IDirectXFileData' : no GUID has been associated with this object
```

下列程式碼範例說明如何定義 IDirectXFileData 介面。

```cpp
// Explicit declaration
struct __declspec(uuid("{3D82AB44-62DA-11CF-AB39-0020AF71E433}")) IDirectXFileData;

// Macro method
#define RT_IID(iid_, name_) struct __declspec(uuid(iid_)) name_
RT_IID("{1DD9E8DA-1C77-4D40-B0CF-98FEFDFF9512}", IDirectXFileData);
```

重新定義介面之後，您必須使用 **attach** 方法將介面附加至所傳回的介面指標 **：:D irect3dcreate9**。 如果沒有，則 **IDirect3D9** 介面將不會由智慧型指標類別正確釋放。

**CComPtr** 類別會在建立物件時，以及將介面指派給 **CComPtr** 類別時，在內部對介面指標呼叫 **IUnknown：： AddRef** 。 若要避免洩漏介面指標，請不要對從 **：:D irect3dcreate9** 傳回的介面呼叫 * * IUnknown：： AddRef。

下列程式碼會適當地釋放介面，而不需要呼叫 **IUnknown：： AddRef**。

```cpp
CComPtr<IDirect3D9> d3d;
d3d.Attach(::Direct3DCreate9(D3D_SDK_VERSION));
```

使用先前的程式碼。 請勿使用下列程式碼，此程式碼會呼叫 **iunknown：： AddRef** 後面接著 **Iunknown：： Release**，而不會釋放由下列方法新增的參考 **：:D irect3dcreate9**。

```cpp
CComPtr<IDirect3D9> d3d = ::Direct3DCreate9(D3D_SDK_VERSION);
```

請注意，這是在 Direct3D 9 中的唯一位置，您必須以這種方式使用 **附加** 方法。

如需 **CComPTR** 和 **CComQIPtr** 類別的詳細資訊，請參閱標頭檔中的定義 `Atlbase.h` 。
