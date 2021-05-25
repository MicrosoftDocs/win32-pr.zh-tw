---
title: Direct3D 12 程式設計環境設定
description: 描述組成具生產力之 Direct3D 12 開發環境的安裝、工具和支援的程式庫。
ms.assetid: B2288866-E95F-46B8-A7A1-19888F029C03
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7079207f91185cc14b37d9056a4fa813b251bce5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342813"
---
# <a name="direct3d-12-programming-environment-setup"></a>Direct3D 12 程式設計環境設定

描述組成具生產力之 Direct3D 12 開發環境的安裝、工具和支援的程式庫。

-   [開發環境](#development-environment)
-   [支援的語言](#supported-languages)
-   [Helper 結構](#helper-structures)
-   [記憶體管理程式庫](#memory-management-library)
-   [支援的工具和程式庫](#supported-tools-and-libraries)
-   [範例](#samples)
-   [Debug 圖層](#debug-layer)
-   [教育影片](#educational-videos)
-   [相關主題](#related-topics)

## <a name="development-environment"></a>開發環境

Direct3D 12 標頭和程式庫是 Windows 10 SDK 的一部分。 使用 Direct3D 12 不需要個別的下載或安裝。

在您安裝 Windows 10 SDK 軟體並 Visual Studio 之後，您的 Direct3D 12 程式設計環境設定就會完成。 建議使用 Visual Studio 2019，因為它會包含 D3D12 圖形偵錯工具，但舊版的 Visual Studio 適用于程式開發。

若要使用 [Direct3D 12 API](direct3d-12-reference.md)，請包含 D3d12 和 D3d12 的連結，或直接在 D3d12.dll 中查詢進入點。

以下是可用的標頭和程式庫。 靜態程式庫的位置取決於電腦上執行的 Windows 10)  (32 位或64位的版本。



| 標頭檔或文件庫檔案名 | Description                         | 安裝位置      |
|-----------------------------|-------------------------------------|-----------------------|
| D3d12。h                     | Direct3D 12 API 標頭              | % WindowsSdkDir \\ 包含 \% WindowsSDKVersion% \\ \um |
| D3d12 .lib                   | 靜態 Direct3D 12 API 存根程式庫 | % WindowsSdkDir \\ Lib \% WindowsSDKVersion% \\ \um\arch |
| D3d12.dll                   | 動態 Direct3D 12 API 程式庫     | % WINDIR% \\ System32    |
| D3d12SDKLayers。h            | Direct3D 12 debug 標頭            | % WindowsSdkDir \\ 包含 \% WindowsSDKVersion% \\ \um |
| D3d12SDKLayers.dll          | 動態 Direct3D 12 debug 程式庫   | % WINDIR% \\ System32    |



## <a name="supported-languages"></a>支援的語言

C + + 是 Direct3D 12 開發的唯一支援語言，c # 和其他 .NET 語言則不受支援。

## <a name="helper-structures"></a>Helper 結構

有一些協助程式結構，特別是可讓您輕鬆地初始化多個 D3D12 結構。 這些結構和一些公用程式函式位於 D3dx12 標頭中。 此標頭是開放原始碼，且由開發人員視需要修改-請從 [D3D12 helper 程式庫](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12) 下載，並參考 [Helper 結構和函式以進行 D3D12](helper-structures-and-functions-for-d3d12.md)。

## <a name="memory-management-library"></a>記憶體管理程式庫

記憶體管理協助程式程式庫可供下載，您可以將它整合到您的應用程式，以更緊密地符合 D3D11 記憶體管理行為。 作為 D3D11 樣式管理程式庫，這對仍在使用 *認可資源* 樣式配置策略的應用程式最有效。 尤其是，程式庫應該會被視為一種逐步執行的石頭，讓您在記憶體受限的案例中 (例如，低端記憶卡、4k、ultra 設定等) ，讓您回到 D3D11 高效能記憶體管理。 D3D12 Api 可讓您透過 D3D11 取得更好的記憶體效率，不過這些技術可能是極具挑戰性且耗時的程式。

請注意，此程式庫是進行中的工作，可能會隨著時間而變更。 使用下列連結來存取程式庫和範例。

-   [D3D12 常駐入門程式庫](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries)

## <a name="supported-tools-and-libraries"></a>支援的工具和程式庫

下列程式庫都可以搭配 Direct3D 12 使用。



| 程式庫                                                                                 |  用途                                                                                                                                                                                                                                                                      | 文件                                                                                                           |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [DirectX 12 的 DirectX 工具套件](https://github.com/Microsoft/DirectXTK12) | 用來撰寫通用 Windows 平臺 (UWP) 應用程式的 Direct3D 12 c + + 程式碼、適用于 Windows 10 的 Win32 桌面應用程式，以及 Xbox One 專屬應用程式的一系列 helper 類別。                                                                         | [DirectX12TK wiki](https://github.com/Microsoft/DirectXTK12/wiki)                                          |
| [DirectXTex](https://github.com/Microsoft/DirectXTex)                      | 您可以使用此功能來讀取和寫入 DDS 檔案，以及執行各種材質內容處理作業，包括調整大小、格式轉換、mip 對應產生、針對 Direct3D 執行時間材質資源封鎖壓縮，以及將高度對應到一般地圖的轉換。 | [DirectXTex wiki](https://github.com/Microsoft/DirectXTex/wiki)                                            |
| [DirectXMesh](https://github.com/Microsoft/DirectXMesh)                   | 您可使用此值來執行各種幾何內容處理作業，包括產生法線和正切框架、三角形相鄰計算和頂點快取優化。                                                                                | [DirectXMesh wiki](https://github.com/Microsoft/DirectXMesh/wiki)                                          |
| [DirectXMath](https://github.com/Microsoft/DirectXMath)                     | 支援向量、純量、矩陣、四元數及許多其他數學運算的大量協助程式類別和方法。                                                                                                                               | [MSDN 上的 DirectXMath 檔](/windows/desktop/dxmath/ovw-xnamath-progguide) |
| [UVAtlas](https://github.com/Microsoft/UVAtlas)                         | 使用此來建立和封裝 isochart 材質塔。                                                                                                                                                                                                           | [UVAtlas wiki](https://github.com/Microsoft/UVAtlas/wiki)                                                  |



 

## <a name="samples"></a>範例

如需工作 D3D12 範例的清單，以及如何尋找和執行這些範例，請參閱 [工作範例](working-samples.md)。

如需如何加入程式碼以啟用特定功能的逐步解說解說，請參閱 [D3D12 程式碼逐步解說-解說](d3d12-code-walk-throughs.md)。

## <a name="debug-layer"></a>Debug 圖層

Debug 層提供大量的額外參數和一致性驗證 (例如驗證著色器連結和資源系結、驗證參數一致性，以及報告錯誤描述) 。

> [!Note]  
> 針對 Windows 10，若要建立支援 debug 層的裝置，請啟用 [圖形工具] 選用功能。 移至 [設定] 面板中的 [系統、應用程式 & 功能]、[管理選擇性功能]、[新增功能]，然後尋找 [圖形工具]。

預設會在 d3d12 中包含支援調試層（D3D12SDKLayers）所需的標頭。

當 debug 圖層列出記憶體流失時，它會輸出物件介面指標清單及其易記名稱。 預設的易記名稱是「 &lt; 未命名」 &gt; 。 您可以使用 [**ID3D12Object：： SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) 方法來設定易記名稱。 一般而言，您應該從生產版本編譯這些呼叫。

建議您使用 debug 層來將您的應用程式進行偵錯工具，以確保這些應用程式的錯誤和警告都已清除。 Debug 層可協助您撰寫 Direct3D 12 程式碼。 此外，當您使用 debug 圖層時，您的產能會增加，因為您可以立即查看其來源的隱匿轉譯錯誤或甚至是黑色畫面的原因。 Debug 層提供許多問題的警告。 例如︰

-   忘記設定材質，但在您的圖元著色器中讀取它。
-   輸出深度，但沒有系結的深度樣板狀態。
-   材質建立失敗，INVALIDARG。

設定編譯器定義 D3DCOMPILE \_ DEBUG，告知 HLSL 編譯器將 DEBUG 資訊納入著色器 blob 中。

``` syntax
#define D3DCOMPILE_DEBUG 1
```

如需所有 debug 介面和方法的詳細資訊，請參閱 [Debug Layer 參考](direct3d-12-sdklayers-reference.md)。

如需有關使用 debug layer 的總覽資訊，請參閱 [瞭解 D3D12 的調試層](understanding-the-d3d12-debug-layer.md)。

## <a name="educational-videos"></a>教育影片

[DirectX advanced learning 影片教學課程](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)有許多 Direct3D 12 和 Windows 10 相關影片，包括圖形偵錯工具的影片，以及報告圖形 bug。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[瞭解 Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 