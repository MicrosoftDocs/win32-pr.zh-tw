---
title: 桌面 DirectX 應用程式的藍圖
description: 以下是可協助您開始使用 DirectX 和 c + + 開發需要大量圖形的桌面應用程式（例如遊戲）的重要資源。
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca95e1fe281253705620136afdced3cb705fe02
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104024371"
---
# <a name="roadmap-for-desktop-directx-apps"></a>桌面 DirectX 應用程式的藍圖

以下是可協助您開始使用 DirectX 和 c + + 開發需要大量圖形的桌面應用程式（例如遊戲）的重要資源。 這不是所有功能或可用資源的完整清單。

## <a name="get-started"></a>開始使用

以下是一些重要主題。 設定您的 DirectX 專案，acclimating 您自己的 Windows，以及範例應用程式。

| 主題 | 描述 |
|-|-|
| [使用 DirectX 建立您的第一個 Windows 應用程式](building-your-first-directx-app.md) | 使用這個基本教學課程來開始進行 DirectX 應用程式開發，然後使用藍圖繼續探索 DirectX。 |
| [開始使用適用于 Windows 的 DirectX](getting-started-with-a-directx-game.md) | 請參閱使用 DirectX 和 c + + 開始開發遊戲時必須採取的步驟。 |
| [DirectX framework 的完整程式碼](complete-code-sample-for-using-a-corewindow-with-directx.md) | 取得基本 DirectX 轉譯架構的程式碼。 |
| [如何使用 Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | 本節將示範如何使用 Microsoft Direct3D 11 API 來完成數個常見工作。 |
| [Direct3D 11 的程式設計指南](/windows/desktop/direct3d11/dx-graphics-overviews) | 程式設計指南包含如何使用 Microsoft Direct3D 11 可程式化管線來建立桌面應用程式的即時3D 圖形的相關資訊。 |
| [適用于 DirectX 圖形的工具](/windows/desktop/direct3dtools/dx-graphics-tools) | 用於支援 DirectX 開發的工具檔。 |
| [Direct3D 11 的新功能](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | 最新的 DirectX 和 Direct3D 版本中新增的所有功能的細目 (目前為 11.2) 。 |
| [下載 Visual Studio 2013](https://msdn.microsoft.com/windows/apps/br229516.aspx) | 您必須有 Visual Studio Express 2013 for Windows Desktop 才能建立 Windows Store 遊戲。 如需 Visual Studio 的導覽，請參閱 [使用 Visual Studio 2012 開發 Windows Store 應用程式](/previous-versions/windows/apps/br211384(v=win.10))。 如需 Visual Studio 中新功能的相關資訊，請參閱 [Visual Studio 2013 的產品重點](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120))。 |
| [DirectX SDK 在哪裡？](../directx-sdk--august-2009-.md) | 包含開發人員的指導方針，他們想要將 DirectX 專案帶入 Microsoft Visual Studio。 |

## <a name="sample-applications"></a>範例應用程式

| 主題 | 描述 |
|-|-|
| [Direct3D 教學課程 Win32 範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | 基本桌面 Direct3D 教學課程範例。 |
| [DirectX 影片轉譯範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | 示範使用 Direct3D 來呈現自訂影片的範例。 |

## <a name="review-key-direct3d-11-concepts"></a>複習金鑰 Direct3D 11 概念

| 主題 | 描述 |
|-|-|
| [圖形管線](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | 涵蓋基本的 Direct3D 11 圖形管線。 |
| [轉譯](/windows/desktop/direct3d11/overviews-direct3d-11-render) | 涵蓋 Direct3D 轉譯模型、元件、著色器和 API 呼叫流程。 |
| [資源](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | 涵蓋 Direct3D "resources"，例如緩衝區和其他 GPU 資源類型。 |
| [影響](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | 涵蓋 Direct3D 多重著色器的實例和效果。  |
| [如何：建立交換鏈](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | 如何建立交換鏈，以用來繪製螢幕區域的圖元。 |
| [如何：建立裝置和立即內容](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | 如何建立 Direct3D 裝置抽象概念，以及用於繪圖的立即內容。 |
| [如何：建立頂點緩衝區](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | 如何建立可供 GPU 處理的簡單網格頂點清單。 |
| [如何：建立索引緩衝區](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | 如何建立索引緩衝區，讓頂點著色器能夠在網格中引導頂點的順序。 |
| [如何：建立常數緩衝區](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | 如何在轉譯期間傳遞 CPU 與 GPU 之間的常數 (統一) 資料。 |
| [如何：建立材質](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | 如何建立可由 GPU 取樣的材質或其他緩衝區資源。 |
| [如何：從檔案初始化材質](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | 如何從檔案載入材質並加以處理，以供著色器管線使用。 |
| [如何：編譯著色器](../direct3d11/how-to--compile-a-shader.md) | 如何編譯要在圖形應用程式中使用的著色器。 |

## <a name="graphics-apis"></a>圖形 Api

| 主題 | 描述 |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | 核心 Api 的檔，用於虛擬化 GPU 和其資源，並使用統一的著色器模型繪製圖形。 |
| [Direct3D HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | High-Level 著色器語言的參考檔，這是用來定義在統一著色器模型中當做圖形管線一部分執行之著色器程式的語法和規則。 |
| [DirectX 圖形介面 (DXGI) ](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | 用來取得 GPU 介面和系統資源的低層級 Api 檔。 |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Direct2D Api 的檔，可支援2D 基本專案的繪製。 一般而言，Direct2D 是用於自訂使用者介面、影像處理和批次處理，以及簡單的遊戲。 |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | DirectWrite Api 的檔，可支援自訂字型轉譯和縮放。 |
| [Windows 影像處理元件 (WIC)](/windows/desktop/wic/-wic-api) | WIC Api 的檔，可用來讀取和管理不同的點陣圖影像格式。 |
| 適用于材質[ (DDS) 的 DirectDraw 表面](/windows/desktop/direct3ddds/dx-graphics-dds) | DDS Api 的檔，用於2D 紋理壓縮和解壓縮與 WIC Api 搭配使用。 |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | DirectXMath Api 的檔，支援 Direct3D 搭配一組適用于3D 即時圖形開發的類型和功能。  (先前的 XNAMath。 )  |
| [DirectCompute](https://walbourn.github.io/) | DirectCompute Api 的檔，用於計算或一般使用著色器功能。 |

## <a name="audio-media-and-input-apis"></a>音訊、媒體和輸入 Api

| 主題 | 描述 |
|-|-|
| [XAudio2 程式設計指南](/windows/desktop/xaudio2/programming-guide) | XAudio2 音訊 API 概念檔的最上層節點。 |
| [XAudio2 程式設計參考](/windows/desktop/xaudio2/programming-reference) | XAudio2 音訊 API 參考檔的最上層節點。 |
| [XInput 程式設計指南](/windows/desktop/xinput/programming-guide) | XInput 控制器 API 概念檔的最上層節點。 |
| [XInput 程式設計參考](/windows/desktop/xinput/programming-reference) | XInput 控制器 API 參考檔的最上層節點。 |
| [媒體基礎](/windows/desktop/medfound/about-the-media-foundation-sdk) | 媒體基礎 (MF) 媒體的最上層節點 (音訊/影片) 播放 API 檔。 通常會在遊戲中使用 MF 來播放聲場播放，而 XAudio2 則是用於動態音訊。 |

## <a name="port-to-directx-11"></a>埠到 DirectX 11

| 主題 | 描述 |
|-|-|
| [遷移至 Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | 將 DirectX 9 程式碼基底移至 DirectX 11 的基本指導方針。 |
| [遊戲的雙重使用程式碼撰寫技術](https://walbourn.github.io/) | 針對在 \_ \* \_ \* 單一應用程式中進行 directx 9 和 directx 11 功能等級開發的詳細 blog 文章。 |
| [針對 Direct3D 功能層級9執行陰影緩衝區](/previous-versions/windows/apps/jj262110(v=win.10)) | 在 DirectX 功能層級9下執行陰影對應的指引 \_ \* 。 |

## <a name="work-with-c"></a>使用 c + +

如果您是在 Windows 平臺上使用 c + + 的老手，可能看起來有點不同。 以下是一些主題的指標，可協助您取得差異的控制碼。

> [!NOTE]
> 這些主題中有一些可協助您維護 c + +/CX 應用程式。 但我們建議您將 [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) 用於新的應用程式。 C++/WinRT 是完全標準現代的 Windows 執行階段 (WinRT) API 的 C++17 語言投影，僅實作為標頭檔案式程式庫，以及設計用來提供您現代化 Windows API 的第一級存取。

| 主題 | 描述 |
|-|-|
| [**C + +/CX (Visual C++ 語言參考)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | 連結至 c + + 相關內容的高層級頁面。 |
| [**快速參考 (Windows 執行階段和 Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | 提供有關 Visual C++ 元件延伸模組 (c + +/CX) 運算子和關鍵字之快速資訊的表格。 |
| [**Type system (c + +/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | C + +/CX。支援之類型的參考內容 |
| [**命名空間 (c + +/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | 命名空間的參考內容，其中包含可在 Windows Store 應用程式中使用的 c + + 特定類型。 |

| | |
|-|-|
| [ (DirectX 和 c + + 的非同步程式設計) ](/previous-versions/windows/apps/hh994919(v=win.10)) | 瞭解 DirectX 應用程式和遊戲的非同步和多執行緒程式設計。 |
| [C + + 中的非同步程式設計](/previous-versions/windows/apps/hh780559(v=win.10)) | 描述使用 task 類別來取用 Windows 執行階段非同步方法的基本方式。 |
| [**task 類別 (並行執行階段)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Task 類別的參考檔。 |
| [工作平行處理 (並行執行階段) ](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | 有關工作類別以及如何使用它的深入討論。 |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>適用于 Windows c + + 程式設計的其他實用程式庫

| | |
|-|-|
| [C + + 標準範本庫](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | Windows 執行階段類型適用于標準範本程式庫類型。 大部分的 c + + Windows Store 應用程式都會使用標準範本程式庫集合和演算法，但在 ABI 界限除外。 |
| [平行模式程式庫](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | PPL 提供的演算法和類型可簡化 CPU 上的工作平行處理原則和資料平行處理原則。  |
| [C++ Accelerated Massive Parallelism (C++ AMP) ](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ AMP 針對支援 DirectX 11 的視訊卡上的一般用途資料平行處理原則，提供 GPU 的存取權。 |

## <a name="blogs-and-other-resources"></a>Blog 和其他資源

| 主題 | 描述 |
|-|-|
| [Windows 和 DirectX blog 的遊戲](https://walbourn.github.io/) | 從重要的 DirectX 開發人員參與者定期更新的 blog，以及最新的 DirectX 開發人員資源。 |
| [Windows DirectX 開發人員 blog](https://devblogs.microsoft.com/directx/) | 官方 Windows DirectX blog。 |
| [Shawn Hargreave 的 DirectX blog](https://www.shawnhargreaves.com/blogindex.html))  | 來自另一個知名 Windows DirectX 開發人員參與者的開發人員 blog。 |
| [DirectX 工具組](https://directxtk.codeplex.com/) | 適用于 DirectX 工具套件的 CodePlex 網站 (DxTK) ，其中包含一些有助於載入網格、播放音效和其他常見行為的實用支援 Api。 |
| [DirectXTex 紋理處理程式庫](https://directxtex.codeplex.com/) | 適用于 DirectX 材質處理程式庫的 Code plex 網站 (DxTEX) ，其中包含紋理處理和壓縮/解壓縮的支援 Api。 |