---
description: 從 Windows 8 開始，DirectX SDK 會包含在 Windows SDK 中。
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: DirectX SDK 在哪裡？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd863bf29858f2313641aca161c73754b789015c
ms.sourcegitcommit: b4beb606419fea6a256b8332a9ea930607e60612
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "103945768"
---
# <a name="where-is-the-directx-sdk"></a>DirectX SDK 在哪裡？

從 Windows 8 開始，DirectX SDK 會包含在 Windows SDK 中。

我們最初將 DirectX SDK 建立為高效能平臺，以在 Windows 上進行遊戲開發。 隨著 DirectX 技術的成熟，這些技術也與更廣泛的應用程式有關。 現今，電腦上的 Direct3D 硬體可用性甚至是傳統的桌面應用程式，都可以使用圖形硬體加速。 相較之下，DirectX 技術已與 Windows 整合。 DirectX 現在是 Windows 的基本部分。

由於 Windows SDK 是 Windows 的主要開發人員 SDK，因此現在已包含 DirectX。 您現在可以使用 Windows SDK 為 Windows 打造絕佳的遊戲。 若要下載 Windows 8. x SDK 或 Windows 10 SDK，請參閱 [Windows SDK 和模擬器保存](https://developer.microsoft.com/windows/downloads/sdk-archive)。

下列技術和工具（前身為 DirectX SDK 的一部分）現在是 Windows SDK 的一部分。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>技術或工具</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Windows 圖形元件<br/></td>
<td>適用于 <a href="/windows/desktop/direct3d">Direct3D</a> 和其他 Windows 圖形 api 的標頭和程式庫（例如 <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>）可在 Windows SDK 中取得。 <br/>
<blockquote>
[!Note]<br />
已淘汰的 D3DX9/D3DX10/D3DX11 公用程式程式庫可透過 <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>取得，但也有一些 <a href="https://walbourn.github.io/living-without-d3dx/">開放原始碼替代方案</a>。 Windows SDK 中提供 D3DCSX DirectCompute 公用程式程式庫和可轉散發 DLL。 D3DX12 可在 <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>上取得。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>HLSL 編譯器 (FXC.EXE) <br/></td>
<td><a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a>編譯器是 Windows SDK 中 bin 資料夾下適當架構子目錄中的工具。<br/>
<blockquote>
[!Note]<br />
Windows SDK 中提供 D3DCompiler API 和可轉散發 DLL。
</blockquote>
<br/><br/>針對 DirectX 12 開發，請使用 Windows SDK 中的 DXCompiler，並裝載于 [GitHub](https://github.com/Microsoft/DirectXShaderCompiler)上。
<br/></td>
</tr>
<tr class="odd">
<td><span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>適用于 Windows 的 PIX<br/></td>
<td>適用于 Windows 的 PIX 工具的取代現在是 Microsoft Visual Studio 中的一項功能，稱為 Visual Studio 圖形偵錯工具。 這項功能大幅改善了可用性、Windows 8 的支援及 Direct3D 11.1，以及與傳統的 Microsoft Visual Studio 功能（例如呼叫堆疊和偵錯工具視窗）的整合，以進行 <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> 的偵錯工具。 如需這項新功能的詳細資訊，請參閱偵測 <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">DirectX 圖形</a>。<br/><br/>針對 DirectX 12 開發，請參閱<a href="https://devblogs.microsoft.com/pix/">Windows 上</a>最新一代的 PIX<br/></td>
</tr>
<tr class="even">
<td><span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span>適用于 Windows 的<a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a><br/></td>
<td><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> API 現在是 Windows 8. x 和 Windows 10 的系統元件。 XAudio2 的標頭和程式庫可在 Windows SDK 中取得。 如需 Windows 7 的支援，請參閱 <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>。<br/></td>
</tr>
<tr class="odd">
<td><span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span>適用于 Windows 的<a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a><br/></td>
<td><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> 1.4 API 現在是 Windows 8. x 和 Windows 10 的系統元件。 XInput 的標頭和程式庫可在 Windows SDK 中取得。<br/>
<blockquote>
[!Note]<br />
舊版 XInput 9.1.0 也可在 Windows 7 或更新版本中取得。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="XNAMATH"></span><span id="xnamath"></span>XNAMATH<br/></td>
<td>XNAMATH 的最新版本（已針對新的指令集和 ARM/ARM64 更新）現在已 <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a>。 DirectXMath 的標頭可在 Windows SDK 和 <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>上取得。<br/></td>
</tr>
<tr class="odd">
<td><span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>DirectX 主控台和 DirectX 功能檢視器<br/></td>
<td>[DirectX 主控台] 和 [DirectX 功能檢視器] 公用程式會包含在 Windows SDK 之 bin 資料夾底下的適當架構子目錄中。 DirectX 功能檢視器也可在 <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>上取得。<br/></td>
</tr>
<tr class="even">
<td><span id="XACT"></span><span id="xact"></span>XACT<br/></td>
<td>不再支援在 Windows 上使用 Xbox 音訊跨平臺工具 (的交易) 。<br/></td>
</tr>
<tr class="odd">
<td><span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">遊戲瀏覽器</a> 和 GDFMAKER<br/></td>
<td><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">遊戲瀏覽器</a>API 為 Windows 的使用者提供遊戲。 只有在 Windows Vista 和 Windows 7 上才支援遊戲瀏覽器 API。 使用遊戲定義檔案製作工具 (GDFMAKER.EXE) 來宣告 Windows Store 應用程式的遊戲評等。 <br/> 遊戲定義檔案製作工具 (GDFMaker.exe) 包含在 Windows SDK 的 bin 資料夾下的 x86 子目錄中，並且支援 Windows Store 應用程式和 Win32 桌面應用程式。<br/>
<br/></td>
</tr>
<tr class="even">
<td><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>範例<br/></td>
<td>您可以在 <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">directx 範例</a> 存放庫中，找到醒目提示 Windows 上的 directx 12 技術的範例應用程式。 舊版 Direct3D 的大部分範例也都可在線上取得。 如需這些範例的詳細資訊，請參閱 <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">DIRECTX SDK 範例目錄</a>。<br/></td>
</tr>
<tr class="odd">
<td><span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>受控 DirectX 1。1<br/></td>
<td>.NET DirectX 元件已被取代，不建議用於新的應用程式。 有一些替代方案可用。 請參閱 <a href="https://walbourn.github.io/directx-and-net/">DirectX 和 .net</a>。 <br/></td>
</tr>
</tbody>
</table>



 

如有必要，可從 [Microsoft 下載中心](http://go.microsoft.com/fwlink/?LinkId=226640) 下載舊版 DirectX SDK，但不建議用於新專案。

> [!Note]  
> 如果您已安裝特定版本的 Visual C++ 2010 可轉散發套件，則無法安裝 DirectX SDK。 如需和修正此問題的解決方案的詳細資訊，請參閱 [ (2010 年6月) 安裝 DIRECTX SDK 時發生的「S1023」錯誤 ](https://support.microsoft.com/kb/2728613)。

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>搭配 Visual Studio 使用 DirectX SDK 專案

您可以在2010年6月的 DirectX SDK 中使用 premium Visual Studio Sku 的範例 (Microsoft Visual Studio Professional 2012、Microsoft Visual Studio Ultimate 2012、Microsoft Visual Studio Professional 2013，或 Windows 7 上的 Microsoft Visual Studio Ultimate 2013) 和 Windows 8 和更新版本。 由於 DirectX 標頭和程式庫轉換成 Windows SDK，因此需要變更專案設定，才能正確地建立這些範例，以及如何將 Windows 8 SDK 和更新版本與 premium Visual Studio Sku 封裝在一起。

這些步驟也適用于相依于 DirectX SDK 的您自己的專案。

1.  確定您的開發電腦上已安裝2010年6月版的 DirectX SDK。 如果您安裝在執行 Windows 8 和更新版本的電腦上，系統將會提示您啟用 .NET 3.5 作為 DirectX SDK 的必要條件安裝。

    > [!Note]  
    > 如果您已安裝特定版本的 Visual C++ 2010 可轉散發套件，則無法安裝 DirectX SDK。 如需和修正此問題的解決方案的詳細資訊，請參閱 [ (2010 年6月) 安裝 DIRECTX SDK 時發生的「S1023」錯誤 ](https://support.microsoft.com/kb/2728613)。

     

2.  請確定您使用的是其中一個 premium Visual Studio Sku。 適用于 Windows 8 的 Microsoft Visual Studio Express 2012 或適用于 Windows 的 Microsoft Visual Studio Express 2013 將不會建立 Windows 8 和更新版本的桌面應用程式，例如 DirectX SDK 範例。 若要安裝其中一個 premium Visual Studio Sku，請移至： [Visual Studio 下載](https://www.microsoft.com/visualstudio/11/downloads) ，並遵循指示進行。

3.  使用 DirectX SDK 範例瀏覽器來安裝所需範例的專案檔。 開啟範例的 Microsoft Visual Studio 2010 相容解決方案檔 (尾碼為 **\_ 2010**) 。

4.  如果您要在只安裝 Microsoft Visual Studio 2012 或 Microsoft Visual Studio 2013 的系統上開啟範例，您會收到下列訊息：「此方案包含一或多個使用舊版 VC + + 編譯器和程式庫的專案。 您可以更新每個專案，以使用 VC + + 編譯器和程式庫 (v110) ）。 在開啟專案之前，請從這個對話方塊中選擇 [ **更新** ] 選項以進行更新。

    否則，您可以在載入後，以滑鼠右鍵按一下方案，然後選擇 [ **更新 VC + + 專案**]，以更新至 Visual Studio 2012 或 Visual Studio 2013 c + + 11 編譯器和程式庫。

5.  D3DX 不會被視為在 Windows 8 和更新版本中使用 Direct3D 的標準 API，因此不會包含在對應的 Windows SDK 中。 調查使用 Direct3D API 的替代解決方案。 針對舊版專案，例如 Windows 7 (及舊版的) DirectX SDK 範例，使用 DirectX SDK 以 D3DX 建立應用程式時，必須執行下列步驟：

    1.  依照下列方式修改專案的 **VC + +** 目錄，以針對 SDK 標頭和程式庫使用正確的順序。

        <dl> i. 開啟專案的 **屬性** ，然後選取 [ **VC + + 目錄** ] 頁面。  
        ii. 選取 [所有設定] **和 [所有平臺**]。  
        iii. 設定這些目錄，如下所示：

        -   可執行檔目錄： **<inherit from parent or project defaults>** 在右邊的下拉式) 上 (
        -   Include 目錄： **$ (IncludePath) ; $ (DXSDK \_ DIR) Include**
        -   包含程式庫目錄： **$ (LibraryPath) ; $ (DXSDK \_ DIR) Lib \\ x86**

          
        iv. 按一下 [套用]。  
        v. 選擇 **X64 平臺**。  
        vi. 設定連結 **庫目錄** ，如下所示：

        -   程式庫目錄： **$ (LibraryPath) ; $ (DXSDK \_ DIR) Lib \\ x64**

          
        </dl>

    2.  在專案中包含 "d3dx9"、"d3dx10" 或 "d3dx11" 時，請務必明確地包含 "d3d9 .h"、"d3d10 .h" 和 "dxgi. h"，或 "d3d11 .h" 和 "dxgi. h"，以確保您會挑選較新的版本。 您可以視需要停用 **警告 C4005** ;不過，此警告表示您使用的是這些標頭的較舊版本。
    3.  移除專案中 DXGIType 的所有參考。 此標頭不存在於 Windows SDK 中，且 DirectX SDK 版本與新的 winerror.h 衝突。
    4.  所有的 D3DX Dll 都安裝在您的開發電腦上（由 DirectX SDK 安裝）。 確定必要的 D3DX 相依性會隨任何範例或應用程式一起轉散發至另一部電腦。
    5.  請注意，目前使用 D3DX11 的取代技術包括 [DirectXTex](https://github.com/Microsoft/DirectXTex)、 [DirectXTK](https://github.com/Microsoft/DirectXTK)、 [DirectXMesh](https://github.com/Microsoft/DirectXMesh)和 [UVAtlas](https://github.com/Microsoft/UVAtlas)。 D3DXMath 會被 [DirectXMath](./dxmath/directxmath-portal.md)取代。

6.  請確認您使用的是新版本的 HLSL 著色器編譯器，方法是觀察下列條件：

    1.  依步驟5變更可執行檔目錄，會導致專案組建使用 Windows SDK 安裝的 FXC.EXE。 請注意，Visual Studio 現在已正式辨識 HLSL 檔。 您可以將它們新增為專案檔，並透過專案系統設定編譯器選項。

    2.  透過舊版 D3DX DLL 叫用執行時間編譯，將會使用不正確的較舊版本的 HLSL 編譯器。 將 \* 程式碼中 D3DXCompile、D3DX10Compile 和 D3DX11Compile api 的所有參考，取代為 \* \* D3DCOMPILER \_46.DLL 或 D3DCOMPILER47.DLL 中的 D3DCompile 函數 \_ 。

    3.  使用執行時間著色器編譯的任何專案都必須有 D3DCOMPILER \_xx.DLL 複製到專案的本機可執行檔路徑。 此 DLL 可在 Windows SDK 安裝的這個子目錄中，于 **% ProgramFiles (x86) % \\ Windows 套件 \\ 8.0 \\ \\ \\ <arch>** 可轉散發套件 d3d 或 **% ProgramFiles (\\ \\ \\ \\ \\ <arch> x86) % windows 套件 8.1** 可轉散發套件（ **<arch>** **x86** 和 **x64**）。

        \_來自 Windows SDK 的 D3DCOMPILER46.DLL 或 D3DCOMPILER47.DLL 不是 \_ 系統元件，不應該複製到 Windows 系統目錄。 您可以將此 DLL 以並存 DLL 的形式，轉散發至其他電腦。

7.  任何使用 XInput API 且要在 Windows 7 或舊版 Windows 上執行的專案，都必須使用舊版 (9.1.0) 或必須明確地將此元件的標頭和程式庫包含在 DirectX SDK 中。 XInput 標頭和 XINPUT。Windows SDK 中包含的 LIB 只會以 Windows 8 和更新版本隨附的 (1.4) 版本為目標。 相同的標頭可以與 XINPUT9 \_ 1 \_ 0 .lib 搭配使用，以使用舊版 Windows 隨附的舊版。 舊版的 XInput 不會偵測到完整的功能，也不會支援控制器整合音訊，因此，如果需要支援這些功能，您必須使用 (1.3) 的 DirectX SDK 版本。

    若要使用完整功能的下層 XInput API，您應該 `#include` 直接從 DIRECTX SDK 進行特定的 XInput 標頭：

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ...然後，在您的連結器選項中有其他相依性，直接連結至 DirectX SDK XInput 程式庫：

    **% DXSDK \_ DIR% Include \\ <arch> \\ xinput .lib**

    XINPUT1 \_3.DLL 二進位檔是由開發電腦上的 DIRECTX SDK 安裝安裝到 Windows 系統目錄。 您必須使用 directx SDK 的 DirectX 安裝程式安裝，將此二進位檔與您的應用程式一起轉散發。

8.  任何使用 XAudio2 API 且要在 Windows 7 或較舊版本的 Windows 上執行的專案，都必須使用舊版 (9.1.0) 或從 DirectX SDK 明確地包含此元件的標頭和程式庫。 Windows SDK 中包含的 XAudio2 標頭和程式庫只會以 Windows 8 所包含 (2.8) 版本為目標。

    例如，使用 XAudio2 時，您應該 `#include` 直接從 DIRECTX SDK 取得特定 XAudio2 標頭：

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ...然後，在您的連結器選項中有其他相依性，直接連結至 DirectX SDK XAudio2 程式庫：

    **% DXSDK \_ DIR% Include \\ <arch> \\ xaudio2 .lib**

    XAUDIO2 \_7.DLL 二進位檔是由開發電腦上的 DIRECTX SDK 安裝安裝到 Windows 系統目錄。 您必須使用 directx SDK 的 DirectX 安裝程式，將這些程式庫與您的應用程式一起轉散發。

9.  如果您已使用 DirectX SDK 搭配舊版的 Visual Studio，Visual Studio 2010 升級可能會將 DirectX SDK 路徑遷移至預設的專案設定。 建議您移除這些設定，以防止未來的組建錯誤。 在 **% USERPROFILE% \\ AppData \\ 本機 \\ Microsoft \\ MSBuild \\ V4.0** 目錄中，修改 DXSDK  DIR 路徑的所有參考，以修改目錄路徑的參考 \_ 。 或者，您可以移除 <PropertyGroup> 包含路徑專案（例如和）的整個節點 <ExecutablePath> ， <IncludePath> 以還原為標準預設值。 如果您在這些檔案中看不到 DXSDK DIR 的參考 \_ ，則不需要進行任何變更。

10. 如果產生的應用程式支援 Windows Vista Service Pack 2 (SP2) 以及 Windows 7 Windows 8 和更新版本，請將名為 **\_ WIN32 \_ WINNT** 的預處理器定義設定為0x600。 如果它只支援 Windows 7 Windows 8 和更新版本，請將它設定為0x601。

    例如：

    1.  開啟專案的 **屬性**，然後選取 [ **C/c + +**  >  **預處理器**]。
    2.  選取 [ **所有** 設定] 和 [ **所有平臺**]。
    3.  移至 [ **預處理器定義** ] 區段，並設定 [ \_ WIN32 \_ WINNT = 0x600]。
    4.  按一下 [套用]。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**適用於 Windows 與 DirectX SDK 的遊戲**
</dt> <dt>

[ (2021 版的 DirectX SDK) 在哪裡？](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[特定年齡的 DirectX Sdk](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[生活不 D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
