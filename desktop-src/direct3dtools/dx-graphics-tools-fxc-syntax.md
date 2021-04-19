---
title: Syntax
description: 以下是呼叫 FXC.exe （效果編譯器工具）的語法。 如需範例，請參閱離線編譯。
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- fxc.exe，語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106967502"
---
# <a name="syntax"></a>Syntax

以下是呼叫 FXC.exe （效果編譯器工具）的語法。 如需範例，請參閱 [離線編譯](dx-graphics-tools-fxc-using.md)。

-   [使用量](#usage)
-   [引數](#arguments)
-   [備註](#remarks)
-   [設定檔](#profiles)
-   [版本資訊](#version-notes)
-   [相關主題](#related-topics)

## <a name="usage"></a>使用方式

**Fxc.exe** *SwitchOptions* *檔案名*

## <a name="arguments"></a>引數
以空格或冒號分隔每個參數選項。

### <a name="switchoptions"></a>*SwitchOptions*
\[在 [ \] 編譯選項] 中。 只有一個必要選項，其他則是選擇性的。 以空格或冒號分隔每一個。

#### <a name="required-option"></a>必要選項
##### <a name="t-profile"></a>/T <*設定檔*>
著色器模型 (查看 [設定檔](#profiles)) 。

#### <a name="optional-options"></a>選擇性的選項
##### <a name="-help"></a>/?、/help
列印的說明 `FXC.exe` 。

##### <a name="commandoptionfile"></a>@<*command. file*>
包含其他編譯選項的檔案。 您可以使用其他命令列編譯選項來混合這個選項。 *命令*。檔案只能包含每行一個選項。 *命令。* 檔案不能包含任何空白行。 檔案中指定的選項不能包含任何開頭或尾端空格。

##### <a name="all_resources_bound"></a>/all_resources_bound
啟用 SM 5.1 + 中的積極壓平合併。 適用于 Direct3D 12 的新。

##### <a name="cc"></a>/Cc
輸出色彩標示的元件。

##### <a name="compress"></a>/compress
壓縮檔案中的 DX10 著色器位元組檔。

##### <a name="d-idtext"></a>/D <*識別碼* >=< *文字*>
定義宏。

##### <a name="decompress"></a>/decompress
從第一個檔案解壓縮 DX10 著色器位元組碼。 輸出檔案應該依壓縮期間的順序列出。

##### <a name="dumpbin"></a>/dumpbin
載入二進位檔案，而不是編譯著色器。

##### <a name="e-name"></a>/E <name>
著色器進入點。 如果未指定任何進入點，則會將 **main** 視為著色器專案名稱。

##### <a name="enable_unbounded_descriptor_tables"></a>/enable_unbounded_descriptor_tables
啟用未系結的描述中繼資料表。 適用于 Direct3D 12 的新。

##### <a name="extractrootsignature-file"></a>/extractrootsignature <*檔案*>
從著色器位元組路徑解壓縮根簽章。 適用于 Direct3D 12 的新。

##### <a name="fc-file"></a>/Fc <*檔案*>
輸出元件碼清單檔。

##### <a name="fd-file"></a>/Fd <*檔案*>
將著色器程式資料庫 (PDB) 資訊中解壓縮，並寫入至指定的檔案。當您編譯著色器時，請使用/Fd 來產生具有著色器調試資訊的 PDB 檔案。

##### <a name="fe-file"></a>/Fe <*檔案*>
將警告和錯誤輸出到指定的檔案。

##### <a name="fh-file"></a>/Fh <*檔案*>
包含物件代碼的輸出標頭檔。

##### <a name="fl-file"></a>/Fl <*檔案*
輸出程式庫。 需要 D3dcompiler \_47.dll 或更新版本的 DLL。

##### <a name="fo-file"></a>/Fo <*檔案*>
輸出物件檔案。 通常 &quot; 會提供 fxc.exe &quot; ，不過會使用其他副檔名，例如 &quot; ： o &quot; 、 &quot; .obj &quot; 或 &quot; . dxbc &quot; 。

##### <a name="fx-file"></a>/Fx <*檔案*>
輸出元件碼和十六進位清單檔。

##### <a name="gch"></a>/Gch
編譯為 fx_4_x 設定檔的子效果。

> [!NOTE]
> 舊版效果設定檔的支援已淘汰。

##### <a name="gdp"></a>/Gdp
停用效果效能模式。

##### <a name="gec"></a>/Gec
啟用回溯相容性模式。

##### <a name="ges"></a>/Ges
啟用 strict 模式。

##### <a name="getprivate-file"></a>/getprivate <*檔案*>
將著色器 blob (編譯的著色器二進位) 中的私用資料儲存至指定的檔案。 從著色器 blob 中，解壓縮先前由/setprivate 內嵌的私用資料。

您必須使用/getprivate. 指定/dumpbin 選項 例如：

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a>/Gfa
避免流量控制結構。

##### <a name="gfp"></a>/Gfp
偏好使用流程式控制制結構。

##### <a name="gis"></a>/Gis
強制執行 IEEE 嚴謹度。

##### <a name="gpp"></a>/Gpp
強制部分有效位數。
    
##### <a name="i-include"></a>/I <*包含*>
其他 include 路徑。

##### <a name="lx"></a>/Lx
輸出十六進位常值。 需要 D3dcompiler \_47.dll 或更新版本的 DLL。

##### <a name="matchuavs"></a>/matchUAVs
符合目前著色器中的範本著色器 UAV 位置配置。 如需詳細資訊，請參閱 <a href="#remarks">備註</a>。

##### <a name="mergeuavs"></a>/mergeUAVs
合併 UAV 位置配置範本著色器和目前的著色器。 如需詳細資訊，請參閱 <a href=""></a> <a href="#remarks">備註</a>。

##### <a name="ni"></a>/Ni
在元件清單中輸出指令編號。

##### <a name="no"></a>/No
元件清單中的輸出指示位元組位移。 當您產生元件時，請使用/No 來標注每個指令的位元組位移。

##### <a name="nologo"></a>/nologo
隱藏著作權訊息。

##### <a name="od"></a>/Od
停用最佳化。 /Od 意指/Gfp，不過輸出可能與/Od/Gfp. 相同

##### <a name="op"></a>/Op
停用 preshaders (已淘汰的) 。

##### <a name="o0-o1-o2-o3"></a>/O0/O1、/O2、/O3
優化層級。 [O1] 是預設設定。
- O0-停用指令重新排列。 這有助於減少暫存器負載，並啟用更快的迴圈模擬。
- O1-停用 ps_3_0 和更新的指令重新排列。
- O2-與 O1 相同。 保留供未來使用。
- O3-與 O1 相同。 保留供未來使用。

##### <a name="p-file"></a>/P <*檔案*>
前置處理至檔案 (必須單獨使用) 。

##### <a name="qstrip_debug"></a>/Qstrip_debug
從 4_0 + 設定檔的著色器位元組程式碼中去除偵錯工具資料。

##### <a name="qstrip_priv"></a>/Qstrip_priv
從 4_0 + 著色器位元組線中去除私用資料。 從著色器 blob 中移除私用資料 (任意) 位元組序列， (您先前以選項內嵌的編譯著色器二進位) `/setprivate <file>` 。

您必須使用/Qstrip_priv 指定/dumpbin 選項。 例如：

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a>/Qstrip_reflect
從 4_0 + 設定檔的著色器位元組程式碼中，去除反映資料。

##### <a name="qstrip_rootsignature"></a>/Qstrip_rootsignature
從著色器位元組路徑中去除根簽章。 適用于 Direct3D 12 的新。

##### <a name="res_may_alias"></a>/res_may_alias
假設 UAVs/SRVs 的別名可能是 cs_5_0 +。 需要 D3dcompiler \_47.dll 或更新版本的 DLL。

##### <a name="setprivate-file"></a>/setprivate <*檔案*>
將指定檔案中的私用資料新增至已編譯的著色器 blob。 將指定的檔案（被視為原始緩衝區）內嵌至著色器 blob。 當您編譯著色器時，請使用/setprivate 來新增私用資料。 或者，使用/dumpbin 選項搭配/setprivate 載入現有的著色器物件，然後在物件位於記憶體中之後，加入私用資料 blob。 例如，您可以使用單一命令搭配/setprivate，將私用資料新增至編譯的著色器 blob：

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
或者，使用第二個命令載入著色器物件，然後新增私用資料的兩個命令：

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a>/setrootsignature <*檔案*>
將根簽章附加到著色器位元組程式碼。 適用于 Direct3D 12 的新。

##### <a name="shtemplate-file"></a>/shtemplate <*檔案*>
使用指定的範本著色器檔案，將 (/mergeUAVs) 和相符的 (/matchUAVs) 資源合併。 如需詳細資訊，請參閱 <a href="#remarks">備註</a>。

##### <a name="vd"></a>/Vd
停用驗證。

##### <a name="verifyrootsignature-file"></a>/verifyrootsignature <*檔案*>
針對根簽章驗證著色器位元組的位元組。 適用于 Direct3D 12 的新。

##### <a name="vi"></a>/Vi
顯示包含進程的詳細資料。

##### <a name="vn-name"></a>/Vn <*名稱*>
在標頭檔中使用名稱作為變數名稱。

##### <a name="wx"></a>/WX
將警告視為錯誤。

##### <a name="zi"></a>/ZI
啟用偵錯資訊。

##### <a name="zpc"></a>/Zpc
在資料行中封裝矩陣-主要順序。

##### <a name="zpr"></a>/Zpr
封裝矩陣（依資料列排列）。

### <a name="filenames"></a>*檔案名稱*

\[在 \] 包含著色器 () 和/或 (s) 效果的檔案中。

## <a name="remarks"></a>備註

使用 `/mergeUAVs` 、 `/matchUAVs` 和 `/shtemplate` 選項來對齊一連串著色器的 UAV 系結位置。

假設您有一個 fx、b. fx 和 .C 的著色器。 若要對齊這一層著色器的 UAV 系結位置，您需要兩個編譯階段：

**對齊一連串著色器的 UAV 系結位置**

1.  使用/mergeUAVs 編譯著色器，並使用/shtemplate. 指定先前編譯的著色器 blob 例如：
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  使用/matchUAVs 編譯著色器，並使用/shtemplate. 從第一次行程指定最後一個著色器 blob 您可以依任何順序進行編譯。 例如：
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
在第二個階段中，您不需要重新編譯 c.。

在您執行上述兩個編譯階段之後，您可以使用. o、b. o 和 c. 做為具有對齊 UAV 位置的最終著色器 blob。

## <a name="profiles"></a>Profiles

每個著色器模型都會加上 HLSL 設定檔的標籤。 若要針對特定著色器模型編譯著色器，請從下表中選擇適當的著色器設定檔。

<table><thead><tr class="header"><th>著色器類型</th><th>Profiles</th></tr></thead><tbody><tr class="odd"><td>計算著色器</td><td><dl> cs_4_0<br />
cs_4_1<br />
cs_5_0<br />
cs_5_1<br />
</dl></td></tr><tr class="even"><td>網域著色器</td><td><dl> ds_5_0<br />
ds_5_1<br />
</dl></td></tr><tr class="odd"><td>幾何著色器</td><td><dl> gs_4_0<br />
gs_4_1<br />
gs_5_0<br />
gs_5_1<br />
</dl></td></tr><tr class="even"><td>HLSL 著色器連結 </td><td><dl> lib_4_0<br />
lib_4_1<br />
lib_4_0_level_9_1<br />
lib_4_0_level_9_1_vs_only<br />
lib_4_0_level_9_1_ps_only<br />
lib_4_0_level_9_3<br />
lib_4_0_level_9_3_vs_only<br />
lib_4_0_level_9_3_ps_only<br />
lib_5_0<br />
</dl> 如需著色器連結的詳細資訊，請參閱 <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> 和 <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>。 <br/></td></tr><tr class="odd"><td>輪廓著色器</td><td><dl> hs_5_0<br />
hs_5_1<br />
</dl></td></tr><tr class="even"><td>像素著色器</td><td><dl> ps_2_0<br />
ps_2_a<br />
ps_2_b<br />
ps_2_sw<br />
ps_3_0<br />
ps_3_sw<br />
ps_4_0<br />
ps_4_0_level_9_0<br />
ps_4_0_level_9_1<br />
ps_4_0_level_9_3<br />
ps_4_1<br />
ps_5_0<br />
ps_5_1<br />
</dl></td></tr><tr class="odd"><td>根簽章</td><td><dl> rootsig_1_0<br />
</dl></td></tr><tr class="even"><td>材質著色器</td><td><dl> tx_1_0<br />
</dl></td></tr><tr class="odd"><td>頂點著色器</td><td><dl> vs_1_1<br />
vs_2_0<br />
vs_2_a<br />
vs_2_sw<br />
vs_3_0<br />
vs_3_sw<br />
vs_4_0<br />
vs_4_0_level_9_0<br />
vs_4_0_level_9_1<br />
vs_4_0_level_9_3<br />
vs_4_1<br />
vs_5_0<br />
vs_5_1<br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a>版本資訊

針對 Direct3D 12，請參閱在 [HLSL 中指定根](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl)簽章、 [在 HLSL 中使用資源](/windows/desktop/direct3d12/resource-binding-in-hlsl) 系結，以及 [使用 HLSL 5.1 的動態索引](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1)。

在 Direct3D 10 中，藉由呼叫下列函式，使用 API 來取得最適合指定裝置的頂點、幾何和圖元著色器設定檔： [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile)、 [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)和 [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile)。

在 Direct3D 9 中，您可以使用 [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) 或 [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) 方法來取出裝置所支援的頂點和圖元著色器設定檔。 這些方法所傳回的 [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) 結構指出裝置在其 **VertexShaderVersion** 和 **PixelShaderVersion** 成員中所支援的頂點和圖元著色器設定檔。

如需範例，請參閱 [使用目前的編譯器進行編譯](dx-graphics-tools-fxc-using.md)。

## <a name="related-topics"></a>相關主題

* [效果-編譯器工具](fxc.md)