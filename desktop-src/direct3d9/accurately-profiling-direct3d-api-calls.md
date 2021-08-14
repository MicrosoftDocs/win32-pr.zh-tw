---
description: 當您擁有可運作的 Microsoft Direct3D 應用程式，並想要改善其效能之後，通常會使用現成的程式碼剖析工具或某些自訂度量技術來測量執行一或多個應用程式開發介面 (API) 呼叫所需的時間。 如果您已完成這項作業，但正在取得不同于下一個轉譯順序的計時結果，或您正在進行假設而不是實際的實驗結果，下列資訊可能有助於您瞭解原因。
ms.assetid: f969be42-d541-4e8d-aec4-eb9508bcc7cf
title: 正確分析 Direct3D API 呼叫 (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6457e47da58a3614270f89eefa1cfa33fbf30cf26544c1013d010696a68e4602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097462"
---
# <a name="accurately-profiling-direct3d-api-calls-direct3d-9"></a>正確分析 Direct3D API 呼叫 (Direct3D 9)

-   [很難正確分析 Direct3D](#accurately-profiling-direct3d-is-difficult)
-   [如何精確地分析 Direct3D 轉譯順序](#how-to-accurately-profile-a-direct3d-render-sequence)
-   [分析 Direct3D 狀態變更](#profiling-direct3d-state-changes)
-   [總結](#summary)
-   [附錄](#appendix)

當您擁有可運作的 Microsoft Direct3D 應用程式，並想要改善其效能之後，通常會使用現成的程式碼剖析工具或某些自訂度量技術來測量執行一或多個應用程式開發介面 (API) 呼叫所需的時間。 如果您已完成這項作業，但正在取得不同于下一個轉譯順序的計時結果，或您正在進行假設而不是實際的實驗結果，下列資訊可能有助於您瞭解原因。

此處提供的資訊是根據您對下列各項的瞭解和經驗所做的假設：

-   C/c + + 程式設計
-   Direct3D API 程式設計
-   測量 API 時間
-   視訊卡及其軟體驅動程式
-   先前分析體驗可能的無法解釋結果

## <a name="accurately-profiling-direct3d-is-difficult"></a>很難正確分析 Direct3D

分析工具會報告在每個 API 呼叫中花費的時間量。 這樣做的目的是為了改善效能，方法是尋找並微調作用點。 有不同類型的分析工具和分析技術。

-   取樣分析工具處於閒置狀態，喚醒到取樣 (的特定間隔，或是記錄正在執行的函式) 。 它會傳回每次呼叫所花費的時間百分比。 一般情況下，取樣分析工具並不會對應用程式造成極大的衝擊，對應用程式的額外負荷造成最大的影響。
-   檢測 profiler 會測量呼叫傳回的實際時間。 它需要將開始和停止分隔符號編譯成應用程式。 檢測分析工具相較于取樣分析工具，與應用程式的侵入性更高。
-   您也可以搭配高效能計時器使用自訂程式碼剖析技術。 這會產生與檢測分析工具很類似的結果。

使用的程式碼剖析工具或程式碼剖析技術，只是產生精確度量的挑戰的一部分。

分析提供可協助您預算效能的解答。 比方說，假設您知道 API 呼叫的平均1000頻率迴圈要執行。 您可以判斷提示有關效能的一些結論，如下所示：

-   2 GHz CPU (，其花了50% 的時間轉譯) 限制為每秒呼叫此 API 1000000 次。
-   若要達到每秒30個畫面格，您無法在每個畫面上呼叫此 API 33000 次以上。
-   您只能針對每個畫面轉譯 3.3 K 物件 (假設每個物件的轉譯順序) 有10個 API 呼叫。

換句話說，如果您的每個 API 呼叫都有足夠的時間，您可以回答預算問題，例如可透過互動方式轉譯的基本專案數。 但是，檢測分析工具所傳回的原始數位將無法準確回答預算問題。 這是因為圖形管線有複雜的設計問題，例如需要執行工作的元件數目、控制工作在元件之間流動方式的處理器數目，以及在執行時間中執行的優化策略，以及設計來讓管線更有效率的驅動程式。

### <a name="each-api-call-goes-through-several-components"></a>每個 API 呼叫都會經歷數個元件

每次呼叫都會由數個元件從應用程式處理至視訊卡。 例如，請考慮下列轉譯順序，其中包含兩個繪製單一三角形的呼叫：


```
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
```



下列概念圖表顯示呼叫必須通過的不同元件。

![api 呼叫經過的圖形元件圖表](images/microbenchmarkinstructionflow2.png)

應用程式會叫用 Direct3D 來控制場景、處理使用者互動，並決定轉譯的完成方式。 所有這項工作都是在轉譯順序中指定，使用 Direct3D API 呼叫傳送到執行時間。 轉譯順序幾乎是硬體獨立的 (也就是說，API 呼叫與硬體無關，但應用程式知道視訊卡支援哪些功能) 。

執行時間會將這些呼叫轉換成與裝置無關的格式。 執行時間會處理應用程式與驅動程式之間的所有通訊，如此一來，應用程式就會根據) 所需的功能，在多個硬體 (上執行。 測量函式呼叫時，檢測分析工具會測量其花費在函數中的時間，以及函式傳回的時間。 檢測分析工具有一項限制，就是它可能不會包含驅動程式將產生的工作傳送至視訊卡的時間，或視訊卡處理工作的時間。 換句話說，現成的檢測分析工具無法屬性與每個函式呼叫相關聯的所有工作。

軟體驅動程式會使用有關視訊卡的硬體特定知識，將裝置獨立的命令轉換成一連串的視訊卡命令。 驅動程式也可以優化傳送至視訊卡的命令順序，以便有效率地在視訊卡上進行轉譯。 這些優化可能會造成程式碼剖析問題，因為完成的工作量不會 (您可能需要瞭解) 的優化。 驅動程式通常會在視訊卡完成所有命令的處理之前，將控制權傳回給執行時間。

視訊卡會藉由合併頂點和索引緩衝區、材質、轉譯狀態資訊和圖形命令的資料，來執行大部分的呈現。 當視訊卡完成轉譯時，從轉譯順序建立的工作會完成。

每個元件都必須處理每個 Direct3D API 呼叫 (執行時間、驅動程式和視訊卡) 轉譯任何事物。

### <a name="there-is-more-than-one-processor-controlling-the-components"></a>有一個以上的處理器控制元件

這些元件之間的關聯性更為複雜，因為應用程式、執行時間和驅動程式是由一個處理器所控制，而視訊卡是由不同的處理器控制。 下圖顯示兩種處理器：中央處理器 (CPU) 和圖形處理單元 (GPU) 。

![cpu 和 gpu 及其元件的圖表](images/microbenchmarkprocessors.png)

電腦系統至少有一個 CPU 和一個 GPU，但可以有一或兩個以上的其中一個。 Cpu 位於主機板上，而 Gpu 位於主機板或視訊卡上。 CPU 的速度取決於主機板上的時鐘晶片，GPU 的速度取決於不同的時鐘晶片。 CPU 時鐘可控制應用程式、執行時間和驅動程式完成工作的速度。 應用程式會透過執行時間和驅動程式，將工作傳送至 GPU。

CPU 和 GPU 通常會以不同的速度執行，而不受彼此影響。 當工作可供使用時，GPU 可以立即回應工作 (假設 GPU 已完成處理先前的工作) 。 GPU 工作會與上圖中的曲線所反白顯示的 CPU 工作平行完成。 分析工具通常會測量 CPU 的效能，而不是 GPU 的效能。 這使得分析變得很困難，因為檢測分析工具所做的測量包括 CPU 時間，但可能不包含 GPU 時間。

GPU 的目的是要將 CPU 的處理，從 CPU 載入到專為圖形工作而設計的處理器。 在新式視訊卡上，GPU 會將管線中的大部分轉換和燈光工作取代為 GPU 的 CPU。 這可大幅減少 CPU 工作負載，讓更多的 CPU 週期可供其他處理使用。 若要調整圖形應用程式的尖峰效能，您需要測量 CPU 和 GPU 的效能，並在這兩種類型的處理器之間平衡工作。

本檔未涵蓋與測量 GPU 效能或平衡 CPU 與 GPU 之間的工作相關的主題。 如果您想要進一步瞭解 GPU (或特定視訊卡) 的效能，請造訪廠商的網站，尋找有關 GPU 效能的詳細資訊。 相反地，這份檔著重于執行時間和驅動程式所完成的工作，方法是將 GPU 工作縮減為可忽略的量。 這部分是根據發生效能問題的應用程式，通常是 CPU 限制的體驗。

### <a name="runtime-and-driver-optimizations-can-mask-api-measurements"></a>執行時間和驅動程式優化可以遮罩 API 度量

執行時間有內建的效能優化，可能會讓個別呼叫的測量量過高。 以下是示範此問題的範例案例。 請考慮下列轉譯順序：


```
  BeginScene();
    ...
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
    ...
  EndScene();
  Present();
```



範例1：簡單呈現順序

查看轉譯順序中兩個呼叫的結果，檢測分析工具可能會傳回類似下列的結果：


```
Number of cycles for SetTexture       : 100
Number of cycles for DrawPrimitive    : 950,500
```



分析工具會傳回處理與每個呼叫相關聯之工作所需的 CPU 週期數目 (請記住，由於 GPU 尚未開始處理這些命令) ，因此不會在這些數目中包含 GPU。 因為 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 需要將近一百萬個週期來處理，所以您可以得出結論，這並不是非常有效率。 不過，您很快就會看到這項結論不正確的原因，以及您可以如何產生可用於預算的結果。

### <a name="measuring-state-changes-requires-careful-render-sequences"></a>測量狀態變更需要小心轉譯順序

IDirect3DDevice9 以外的所有呼叫 [**:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)、 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)或 [**Clear**](/windows/desktop/api) (例如 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)、 [**SetVertexDeclaration**](/windows/desktop/api)和 [**graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) 會產生狀態變更。 每個狀態變更都會設定管線狀態，以控制如何完成轉譯。

執行時間及（或）驅動程式中的優化是設計來藉由減少所需的工作量來加速轉譯。 以下是一些可能會會污染設定檔平均值的狀態變更優化：

-   驅動程式 (或執行時間) 可能會將狀態變更儲存為本機狀態。 因為驅動程式可在「延遲」演算法中運作 (將工作延後到絕對必要) ，否則與某些狀態變更相關聯的工作可能會延遲。
-   執行時間 (或驅動程式) 可能會藉由優化來移除狀態變更。 其中一個範例可能是移除因為先前已停用光源而停用光源的重複狀態變更。

沒有萬無一失的方式可以查看轉譯順序，並結束哪些狀態變更將會設定中途位並延後工作，或只是藉由優化來移除。 即使您可以在目前的執行時間或驅動程式中識別優化狀態變更，仍可能會更新未來的執行時間或驅動程式。 您也不容易知道先前的狀態為何，因此很難識別多餘的狀態變更。 驗證狀態變更成本的唯一方法，就是測量包含狀態變更的呈現順序。

如您所見，由於有多個處理器、由多個元件處理的命令，以及元件內建的優化，使程式碼剖析難以預測，因此會造成複雜的問題。 在下一節中，將會解決這些分析挑戰。 將會顯示範例 Direct3D 轉譯序列，以及伴隨的測量技術。 透過這種知識，您將能夠針對個別呼叫產生精確、可重複的度量。

## <a name="how-to-accurately-profile-a-direct3d-render-sequence"></a>如何精確地分析 Direct3D 轉譯順序

現在已醒目提示某些程式碼剖析挑戰，本節將為您說明可協助您產生可用於預算的設定檔測量的技巧。 如果您瞭解 CPU 所控制元件之間的關聯性，以及如何避免執行時間和驅動程式所執行的效能優化，則可以精確、可重複的分析測量措施。

若要開始，您必須能夠精確地測量單一 API 呼叫的執行時間。

### <a name="pick-an-accurate-measurement-tool-like-queryperformancecounter"></a>挑選精確的測量工具，例如 QueryPerformanceCounter

Microsoft Windows 作業系統包含高解析度計時器，可用來測量高解析度的經過時間。 您可以使用 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)來傳回其中一個這類計時器的目前值。 叫用 **QueryPerformanceCounter** 來傳回開始和停止值之後，這兩個值之間的差異可以轉換成實際經過的時間， (秒) 使用 **QueryPerformanceCounter**。

使用 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的優點在於它可以在 Windows 中使用，而且很容易使用。 只要使用 **QueryPerformanceCounter** 呼叫來括住呼叫，並儲存開始和停止值即可。 因此，本文將示範如何使用 **QueryPerformanceCounter** 來分析執行時間，類似于檢測分析工具測量它的方式。 以下範例顯示如何在原始程式碼中內嵌 **QueryPerformanceCounter** ：


```
  BeginScene();
    ...
    // Start profiling
    LARGE_INTEGER start, stop, freq;
    QueryPerformanceCounter(&start);

    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1); 

    QueryPerformanceCounter(&stop);
    stop.QuadPart -= start.QuadPart;
    QueryPerformanceFrequency(&freq);
    // Stop profiling
    ...
  EndScene();
  Present();
```



範例2：使用 QPC 執行自訂分析

開始和停止是兩個大型整數，會保存高效能計時器傳回的開始和停止值。 請注意，QueryPerformanceCounter (&start) 只會在 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 QueryPerformanceCounter 之前呼叫， (&stop) 是在 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)之後呼叫。 取得停止值之後，會呼叫 QueryPerformanceFrequency 來傳回頻率，也就是高解析度計時器的頻率。 在此假設範例中，假設您取得開始、停止和頻率的下列結果：



| 區域變數 | 刻度數目 |
|----------------|-----------------|
| start          | 1792998845094   |
| stop           | 1792998845102   |
| 頻率           | 3579545         |



 

您可以將這些值轉換為執行 API 呼叫所需的迴圈次數，如下所示：


```
# ticks = (stop - start) = 1792998845102 - 1792998845094 = 8 ticks

# cycles = CPU speed * number of ticks / QPF
# 4568   = 2 GHz      * 8              / 3,579,545
```



換句話說，在此 2 GHz 電腦上處理 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 大約需要大約4568個時鐘週期。 您可以將這些值轉換為執行所有呼叫所花費的實際時間，如下所示：


```
(stop - start)/ freq = elapsed time
8 ticks / 3,579,545 = 2.2E-6 seconds or between 2 and 3 microseconds.
```



使用 QueryPerformanceCounter 時，您必須將開始和停止度量新增至轉譯順序，並使用 QueryPerformanceFrequency 將刻度的 (數目) 轉換為 CPU 週期數目或實際時間。 識別測量技術是開始開發自訂程式碼剖析的好開端。 但在您開始進行測量並開始進行測量之前，您必須先瞭解如何處理視訊卡。

### <a name="focus-on-cpu-measurements"></a>專注于 CPU 度量

如先前所述，CPU 和 GPU 會平行運作，以處理 API 呼叫所產生的工作。 真實世界的應用程式需要分析這兩種類型的處理器，以找出您的應用程式是否受 CPU 限制或 GPU 受限。 因為 GPU 效能是廠商專屬的，所以在本文中產生的結果會是很大的挑戰，其中涵蓋各種可用的視訊卡。

這份檔只會著重在分析 CPU 所執行的工作，方法是使用自訂技術來測量執行時間和驅動程式工作。 GPU 工作將會縮減為不重要的數量，讓 CPU 結果更明顯。 這種方法的其中一個優點是，這項技術會產生附錄中的結果，讓您能夠與您的度量相互關聯。 若要將視訊卡所需的工作減少到無意義的層級，只要將轉譯工作縮減至可能的最小數量即可。 這可以透過限制繪製呼叫來呈現單一三角形來完成，而且可以進一步限制，讓每個三角形只包含一個圖元。

本檔中用於測量 CPU 工作的測量單位，會是 CPU 頻率週期的數目，而不是實際時間。 CPU 頻率週期的優點是，cpu 延遲的應用程式) 的可攜性 (，與 CPU 速度不同的電腦上實際經過的時間。 您可以視需要輕鬆地將其轉換為實際時間。

本檔未涵蓋在 CPU 與 GPU 之間平衡工作負載的相關主題。 請記住，本文的目標不是要測量應用程式的整體效能，而是示範如何精確測量執行時間和驅動程式處理 API 呼叫所需的時間。 使用這些精確的測量，您就可以將 CPU 的預算工作列入考慮，以瞭解特定的效能案例。

### <a name="controlling-runtime-and-driver-optimizations"></a>控制執行時間和驅動程式優化

在識別測量技術的情況下，下一步是瞭解程式碼剖析時所取得的執行時間和驅動程式優化策略。

CPU 工作可以分為三個值區：應用程式工作、執行時間運作和驅動程式運作。 因為這是在程式設計人員控制項下，所以請略過應用程式的工作。 從應用程式的觀點來看，執行時間和驅動程式就像黑色方塊一樣，因為應用程式無法控制在其中執行的專案。 重要的是瞭解可在執行時間和驅動程式中執行的優化技術。 如果您不了解這些優化，很容易就能根據設定檔量值，跳到 CPU 所執行之工作量的錯誤結論。 尤其是，有兩個主題與所謂的命令緩衝區相關，以及它可以如何進行程式碼剖析。 這些主題包括：

-   使用命令緩衝區的執行時間優化。 命令緩衝區是執行時間優化，可減少模式轉換的影響。 若要控制模式轉換的時間，請參閱 [控制命令緩衝區](#controlling-the-command-buffer)。
-   否定命令緩衝區的計時效果。 模式轉換的經過時間可能會對分析量測測量造成很大的影響。 這項策略的策略是 [讓轉譯順序比模式轉換更大](#make-the-render-sequence-large-compared-to-the-mode-transition)。

### <a name="controlling-the-command-buffer"></a>控制命令緩衝區

當應用程式進行 API 呼叫時，執行時間會將 API 呼叫轉換為與裝置無關的格式， (我們會呼叫命令) ，並將它儲存在命令緩衝區中。 命令緩衝區會新增至下圖。

![cpu 元件的圖表，包括命令緩衝區](images/microbenchmarkcommandbuffer2.png)

每次應用程式進行另一個 API 呼叫時，執行時間都會重複此順序，並將另一個命令新增至命令緩衝區。 在某個時間點，執行時間會清空緩衝區 (將命令傳送至驅動程式) 。 在 Windows XP 中，清空命令緩衝區會導致模式轉換，因為作業系統會在使用者) 模式中執行的 (切換至驅動程式 (以核心模式執行) ，如下圖所示。

-   使用者模式-執行應用程式程式碼的非特殊許可權處理器模式。 使用者模式應用程式無法取得系統資料的存取權（透過系統服務）。
-   核心模式-以 Windows 為基礎的執行程式碼執行時的特殊許可權處理器模式。 在核心模式中執行的驅動程式或執行緒可以存取所有系統記憶體、直接存取硬體，以及使用硬體來執行 i/o 的 CPU 指示。

![使用者模式和核心模式之間的轉換圖](images/microbenchmarkcommandbuffer3.png)

每次 CPU 從使用者切換至核心模式時，都會進行轉換 (相反地，) 而且其所需的週期數目很大，相較于個別的 API 呼叫會有很大的影響。 如果執行時間在叫用時，將每個 API 呼叫傳送至驅動程式，則每個 API 呼叫都會產生模式轉換的成本。

相反地，命令緩衝區是執行時間優化，其設計目的是要降低模式轉換的有效成本。 命令緩衝區會將許多驅動程式命令排入佇列，以準備單一模式轉換。 當執行時間將命令新增至命令緩衝區時，控制權會傳回給應用程式。 Profiler 無法得知驅動程式命令甚至可能尚未傳送至驅動程式。 如此一來，現成檢測分析工具所傳回的數位會造成誤導，因為它會測量執行時間的工作，但不會測量相關聯的驅動程式工作。

### <a name="profile-results-without-a-mode-transition"></a>不使用模式轉換剖析結果

使用範例2中的轉譯順序，以下是一些可說明模式轉換大小的一般計時度量。 假設 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 呼叫不會造成模式轉換，則現成的檢測分析工具可能會傳回類似下列的結果：


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
```



每個數位都是執行時間將這些呼叫新增至命令緩衝區所需的時間量。 因為沒有模式轉換，所以驅動程式尚未完成任何工作。 分析工具的結果是正確的，但它們並不會測量轉譯順序最終會造成 CPU 執行的所有工作。

### <a name="profile-results-with-a-mode-transition"></a>使用模式轉換剖析結果

現在，請看看發生模式轉換時，相同範例會發生什麼事。 這次，假設 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 會導致模式轉換。 同樣地，現成的檢測分析工具可能會傳回類似以下的結果：


```
Number of cycles for SetTexture           : 98 
Number of cycles for DrawPrimitive        : 946,900
```



針對 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 所測量的時間大約相同，不過， [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 所花費的時間量會大幅增加，因為模式轉換。 以下是發生的情況：

1.  假設在轉譯順序開始之前，命令緩衝區有一個命令的空間。
2.  [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 會轉換成與裝置無關的格式，並新增至命令緩衝區。 在此案例中，此呼叫會填入命令緩衝區。
3.  執行時間會嘗試將 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 新增至命令緩衝區，但無法將其新增至命令緩衝區，因為它已滿。 相反地，執行時間會清空命令緩衝區。 這會導致核心模式轉換。 假設轉換大約需要5000迴圈。 這段時間可因應 **DrawPrimitive** 所花費的時間。
4.  驅動程式接著會處理與從命令緩衝區清空的所有命令相關聯的工作。 假設處理近乎填滿命令緩衝區之命令的驅動程式時間大約是935000迴圈。 假設與 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 相關聯的驅動程式工作大約是2750迴圈。 這段時間可因應 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)所花費的時間。
5.  當驅動程式完成其工作時，使用者模式轉換會將控制權傳回到執行時間。 命令緩衝區現在是空的。 假設轉換大約需要5000迴圈。
6.  轉譯順序的完成方式是轉換 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ，並將它新增至命令緩衝區。 假設這大約需要900迴圈。 這段時間可因應 **DrawPrimitive** 所花費的時間。

總結結果之後，您會看到：


```
DrawPrimitive = kernel-transition + driver work    + user-transition + runtime work
DrawPrimitive = 5000              + 935,000 + 2750 + 5000            + 900
DrawPrimitive = 947,950  
```



就像在沒有模式轉換的情況下進行 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 的測量， (900 迴圈) ，採用模式轉換的 **DrawPrimitive** 測量 (947950 迴圈) 是精確的，但在預算的 CPU 工作方面毫無用處。 結果包含正確的執行時間工作、驅動程式適用于 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)、驅動程式適用于任何之前 **SetTexture** 的命令，以及兩個模式轉換。 不過，測量結果缺少 **DrawPrimitive** 驅動程式工作。

可能會發生模式轉換，以回應任何呼叫。 這取決於先前在命令緩衝區中的內容。 您必須控制模式轉換，以瞭解多少 CPU 工作 (執行時間和驅動程式) 與每個呼叫相關聯。 若要這樣做，您需要一種機制來控制命令緩衝區和模式轉換的時間。

### <a name="the-query-mechanism"></a>查詢機制

Microsoft Direct3D 9 中的查詢機制是設計來讓執行時間查詢 GPU 以進行處理，並從 GPU 傳回特定資料。 在分析期間，如果 GPU 工作最小化，使其對效能的影響降到最低，您可以從 GPU 傳回狀態，以協助測量驅動程式工作。 畢竟，當 GPU 看到驅動程式命令之後，驅動程式就會完成。 此外，您可以 coaxed 查詢機制來控制兩個對分析很重要的命令緩衝區特性：當命令緩衝區清空時，以及緩衝區中有多少工作。

以下是使用查詢機制的相同呈現順序：


```
// 1. Create an event query from the current device
IDirect3DQuery9* pEvent;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEvent);

// 2. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 3. Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

// 4. Start profiling
LARGE_INTEGER start, stop;
QueryPerformanceCounter(&start);

// 5. Invoke the API calls to be profiled.
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);

// 6. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 7. Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
    
// 8. End profiling
QueryPerformanceCounter(&stop);
```



範例3：使用查詢來控制命令緩衝區

以下是每一行程式碼的詳細說明：

1.  建立具有 D3DQUERYTYPE 事件的 query 物件來建立事件查詢 \_ 。
2.  藉由呼叫 ([**D3DISSUE \_ END**](d3dissue-end.md)) 的 [**問題**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)，將查詢事件標記新增至命令緩衝區。 此標記會指示驅動程式追蹤 GPU 何時完成執行標記之前的任何命令。
3.  第一個呼叫會清空命令緩衝區，因為 [**使用**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) [**D3DGETDATA \_ FLUSH 呼叫**](d3dgetdata-flush.md) 會強制清空命令緩衝區。 每個後續的呼叫都會檢查 GPU，以查看它何時完成處理所有命令緩衝區工作。 在 GPU 閒置之前，此迴圈不會傳回 S \_ 確定。
4.  範例開始時間。
5.  叫用正在分析的 API 呼叫。
6.  將第二個查詢事件標記新增至命令緩衝區。 此標記將用來追蹤完成的呼叫。
7.  第一個呼叫會清空命令緩衝區，因為 [**使用**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) [**D3DGETDATA \_ FLUSH 呼叫**](d3dgetdata-flush.md) 會強制清空命令緩衝區。 當 GPU 完成處理所有命令緩衝區工作 **時，[** 操作 \_ ] 會傳回 [確定]，而迴圈會因為 GPU 閒置而結束。
8.  取樣停止時間。

以下是以 QueryPerformanceCounter 和 QueryPerformanceFrequency 測量的結果：



| 區域變數 | 刻度數目 |
|----------------|-----------------|
| start          | 1792998845060   |
| stop           | 1792998845090   |
| 頻率           | 3579545         |



 

在 2 GHz 電腦上再次將刻度轉換成迴圈一次 () ：


```
# ticks  = (stop - start) = 1792998845090 - 1792998845060 = 30 ticks
# cycles = CPU speed * number of ticks / QPF
# 16,450 = 2 GHz      * 30             / 3,579,545
```



以下是每次呼叫的迴圈數細目：


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
Number of cycles for Issue                : 200
Number of cycles for GetData              : 16,450
```



查詢機制允許我們控制執行時間和所測量的驅動程式工作。 若要瞭解每個數位，以下是回應每個 API 呼叫時所發生的狀況，以及預估的時間：

1.  第一個呼叫會透過使用 [**D3DGETDATA \_ FLUSH 呼叫**](d3dgetdata-flush.md) [**，來**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)清空命令緩衝區。 當 GPU 完成處理所有命令緩衝區工作 **時，[** 操作 \_ ] 會傳回 [確定]，而迴圈會因為 GPU 閒置而結束。
2.  轉譯順序一開始會將 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 轉換成與裝置無關的格式，並將它新增至命令緩衝區。 假設這大約需要100迴圈。
3.  [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 會轉換並新增至命令緩衝區。 假設這大約需要900迴圈。
4.  [**問題**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) 會將查詢標記新增至命令緩衝區。 假設這大約需要200迴圈。
5.  [，][**會讓命令**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)緩衝區清空，以強制執行核心模式轉換。 假設這大約需要5000迴圈。
6.  驅動程式接著會處理與所有四個呼叫相關聯的工作。 假設處理 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 的驅動程式時間大約是2964迴圈， [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 大約是3600迴圈， [**問題**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) 大約是200週期。 因此，所有四個命令的總驅動程式時間大約是6450迴圈。
    > [!Note]  
    > 驅動程式也需要花一點時間來查看 GPU 的狀態。 因為 GPU 的運作方式很簡單，所以 GPU 應該已經完成。 [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) 「硬碟」會 \_ 根據 GPU 完成的可能性傳回「確定」。

     

7.  當驅動程式完成其工作時，使用者模式轉換會將控制權傳回到執行時間。 命令緩衝區現在是空的。 假設這大約需要5000迴圈。

數量 [**值包含：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)


```
GetData = kernel-transition + driver work + user-transition
GetData = 5000              + 6450        + 5000           
GetData = 16,450  

driver work = SetTexture + DrawPrimitive + Issue = 
driver work = 2964       + 3600          + 200   = 6450 cycles 
```



與 QueryPerformanceCounter 搭配使用的查詢機制會測量所有的 CPU 工作。 這是透過查詢標記和查詢狀態比較來完成。 新增至命令緩衝區的開始和停止查詢標記是用來控制緩衝區中有多少工作。 等到傳回正確的傳回碼時，才會在清除轉譯順序開始之前完成開始測量，並且在驅動程式完成與命令緩衝區內容相關聯的工作之後，才進行停止測量。 這可有效地捕捉執行時間和驅動程式所完成的 CPU 工作。

既然您知道命令緩衝區及其對分析的影響，您應該知道有一些其他條件可能會導致執行時間清空命令緩衝區。 您必須在轉譯順序中監看這些專案。 其中有些條件是為了回應 API 呼叫，而其他則是為了回應執行時間中的資源變更。 下列任何一項條件都會導致模式轉換：

-   當 ([**鎖定**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)) 的其中一個鎖定方法時，會在特定條件下使用特定旗標) ，在頂點緩衝區、索引緩衝區或材質 (上呼叫。
-   當裝置或頂點緩衝區、索引緩衝區或材質建立時。
-   當最後一個版本終結裝置或頂點緩衝區、索引緩衝區或紋理時。
-   當呼叫 [**ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) 時。
-   如果 [**有的話**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) ，則會呼叫。
-   當命令緩衝區填滿時。
-   使用 D3DGETDATA 排 [**清時，會呼叫**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) \_ 。

請小心在轉譯順序中監看這些條件。 每次新增模式轉換時，10000的驅動程式工作週期都會新增至分析測量。 此外，命令緩衝區不會以靜態方式調整大小。 執行時間可能會變更緩衝區大小，以回應應用程式所產生的工作量。 這也是另一個相依于轉譯順序的優化。

因此請小心控制分析期間的模式轉換。 查詢機制提供了一種健全的方法來清空命令緩衝區，讓您可以控制模式轉換的時間，以及緩衝區所包含的工作量。 但是，即使這項技術也可以藉由減少模式轉換時間來改善，以使其對測量的結果無關緊要。

### <a name="make-the-render-sequence-large-compared-to-the-mode-transition"></a>比模式轉換更大的呈現順序

在上述範例中，核心模式切換和使用者模式交換器耗用大約10000週期，與執行時間和驅動程式工作無關。 由於模式轉換是內建在作業系統中，因此無法縮減為零。 若要讓模式轉換成為無意義的，轉譯序列需要調整，讓驅動程式和執行時間工作的大小比模式切換的順序大。 您可以嘗試進行減法以移除轉換，但透過更大的轉譯順序成本來攤銷成本會更可靠。

減少模式轉換的策略（直到變成不重要的策略）會將迴圈加入至轉譯順序。 例如，如果新增了迴圈來重複轉譯順序1500次，讓我們看看分析結果：


```
// Initialize the array with two textures, same size, same format
IDirect3DTexture* texArray[2];

CreateQuery(D3DQUERYTYPE_EVENT, pEvent);
pEvent->Issue(D3DISSUE_END);
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

LARGE_INTEGER start, stop;
// Now start counting because the video card is ready
QueryPerformanceCounter(&start);

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  SetTexture(taxArray[i%2]);
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

pEvent->Issue(D3DISSUE_END);

while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
QueryPerformanceCounter(&stop);
```



範例4：將迴圈加入至轉譯順序

以下是以 QueryPerformanceCounter 和 QueryPerformanceFrequency 測量的結果：



| 區域變數 | Tics 數目 |
|----------------|----------------|
| start          | 1792998845000  |
| stop           | 1792998847084  |
| 頻率           | 3579545        |



 

立即使用 QueryPerformanceCounter 量值2840刻度。 將刻度轉換成迴圈和我們已經顯示的相同：


```
# ticks  = (stop - start) = 1792998847084 - 1792998845000 = 2840 ticks
# cycles    = machine speed * number of ticks / QPF
# 6,900,000 = 2 GHz          * 2840           / 3,579,545
```



換句話說，這 2 GHz 電腦上大約需要6900000個週期，才能處理轉譯迴圈中的1500呼叫。 在6900000週期中，模式轉換中的時間量大約是1萬，因此現在設定檔結果幾乎會完全測量與 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)相關聯的工作。

請注意，程式碼範例需要兩個材質的陣列。 為了避免在每次呼叫時都設定相同材質指標的執行時間優化，只要使用兩個材質的陣列，就會移除 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 。 如此一來，每次執行迴圈時，材質指標就會變更，並執行與 **SetTexture** 相關聯的完整工作。 請確定這兩個紋理都有相同的大小和格式，如此一來，材質不會變更其他狀態。

現在您已經有分析 Direct3D 的技巧。 它依賴高效能計數器 (QueryPerformanceCounter) 來記錄 CPU 處理工作所需的滴答數。 您可以使用查詢機制，小心地將工作控制為與 API 呼叫相關聯的執行時間和驅動程式。 查詢提供兩種控制方法：先在轉譯順序開始之前清空命令緩衝區，第二個則是在 GPU 工作完成時傳回。

到目前為止，本文已說明如何分析轉譯順序。 每個轉譯順序都相當簡單，其中包含單一 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 呼叫和 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 呼叫。 這樣做的目的是要將焦點放在命令緩衝區，並使用查詢機制來控制它。 以下是如何分析任意轉譯序列的簡短摘要：

-   使用高效能計數器（例如 QueryPerformanceCounter）來測量處理每個 API 呼叫所需的時間。 使用 QueryPerformanceFrequency 和 CPU 頻率速率，將此值轉換為每個 API 呼叫的 CPU 週期數目。
-   藉由轉譯三角形清單來將 GPU 工作的數量降到最低，其中每個三角形都包含一個圖元。
-   在轉譯順序之前，請使用查詢機制來清空命令緩衝區。 這可保證分析將會捕捉與轉譯順序相關聯的執行時間和驅動程式工作的正確數量。
-   使用查詢事件標記來控制新增至命令緩衝區的工作量。 這個相同的查詢會偵測 GPU 何時完成其工作。 因為 GPU 的工作很簡單，這幾乎相當於測量驅動程式工作完成的時間。

所有這些技術都是用來分析狀態變更。 假設您已閱讀並瞭解如何控制命令緩衝區，並已順利完成 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)的基準測量，您就可以將狀態變更新增至轉譯順序。 將狀態變更新增至轉譯順序時，有一些額外的程式碼剖析挑戰。 如果您想要將狀態變更新增至轉譯順序，請務必繼續進行下一節。

## <a name="profiling-direct3d-state-changes"></a>分析 Direct3D 狀態變更

Direct3D 使用許多轉譯狀態來控制幾乎所有的管線層面。 導致狀態變更的 Api 包括繪製基本呼叫以外的任何函數或方法 \* 。

狀態變更很棘手，因為您可能無法查看狀態變更的成本，而不會呈現。 這是延遲演算法的結果，驅動程式和 GPU 會使用這些演算法來延遲工作，直到絕對必須完成為止。 一般而言，您應該遵循下列步驟來測量單一狀態變更：

1.  先分析 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 。
2.  將一項狀態變更新增至轉譯順序，並分析新的序列。
3.  減去兩個序列之間的差異，以取得狀態變更的成本。

當然，您已瞭解如何使用查詢機制並將轉譯順序放在迴圈中，以消除模式轉換的成本。

### <a name="profiling-a-simple-state-change"></a>程式碼剖析簡單狀態變更

從包含 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)的轉譯順序開始，以下是測量新增 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)成本的程式碼序列：


```
// Get the start counter value as shown in Example 4 

// Initialize a texture array as shown in Example 4
IDirect3DTexture* texArray[2];

// Render sequence loop 
for(int i = 0; i < 1500; i++)
{
  SetTexture(0, texArray[i%2];
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

// Get the stop counter value as shown in Example 4 
```



範例5：測量一次狀態變更 API 呼叫

請注意，迴圈包含兩個呼叫： [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 和 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)。 轉譯順序會迴圈1500次，並產生類似以下的結果：



| 區域變數 | Tics 數目 |
|----------------|----------------|
| start          | 1792998860000  |
| stop           | 1792998870260  |
| 頻率           | 3579545        |



 

再次將刻度轉換成迴圈會產生：


```
# ticks  = (stop - start) = 1792998870260 - 1792998860000 = 10,260 ticks
# cycles    = machine speed * number of ticks / QPF
5,775,000   = 2 GHz          * 10,260         / 3,579,545
```



除以迴圈中的反覆運算次數會產生：


```
5,775,000 cycles / 1500 iterations = 3850 cycles for one iteration
```



迴圈的每個反復專案都包含狀態變更和繪製呼叫。 減去 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 轉譯序列的結果：


```
3850 - 1100 = 2750 cycles for SetTexture
```



這是將 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 新增至此轉譯順序的平均迴圈數目。 同樣的技巧也可以套用至其他狀態變更。

為什麼 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 稱為簡單狀態變更？ 由於正在設定的狀態受到限制，因此管線會在每次狀態變更時執行相同數量的工作。 將兩個材質限制為相同的大小和格式，可確保每個 **SetTexture** 呼叫都有相同數量的工作。

### <a name="profiling-a-state-change-that-needs-to-be-toggled"></a>分析需要切換的狀態變更

有其他狀態變更會導致圖形管線針對轉譯迴圈的每個反復專案變更圖形管線所執行的工作量。 例如，如果已啟用 z 測試，則只有在針對現有圖元的 z 值測試新圖元的 z 值之後，每個圖元色彩才會更新轉譯目標。 如果停用 z 測試，則不會執行每個圖元的測試，而且輸出的寫入速度會更快。 啟用或停用 z 測試狀態會大幅變更 CPU (完成的工作量，以及轉譯期間的 GPU) 。

[**Graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 需要特定的呈現狀態和狀態值，才能啟用或停用 z 測試。 特定狀態值會在執行時間評估，以判斷需要多少工作。 很難在轉譯迴圈中測量這項狀態變更，但仍會預先先決條件管線狀態，使其切換。 唯一的解決方法是在轉譯順序期間切換狀態變更。

例如，程式碼剖析技術需要重複兩次，如下所示：

1.  從分析 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 轉譯順序開始著手。 將基準稱為此。
2.  分析可切換狀態變更的第二個轉譯順序。 轉譯順序迴圈包含：
    -   將狀態變更為 "false" 條件的狀態變更。
    -   [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 就像原始順序一樣。
    -   將狀態變更為「true」條件的狀態變更。
    -   第二個 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ，以強制實現第二個狀態變更。
3.  找出這兩個轉譯序列之間的差異。 這是透過下列方式完成：
    -   將基準 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 序列乘以2，因為新序列中有兩個 **DrawPrimitive** 呼叫。
    -   從原始序列減去新序列的結果。
    -   將結果除以2，以取得「false」和「true」狀態變更的平均成本。

使用轉譯順序中所使用的迴圈技術時，需要測量變更管線狀態的成本，方法是將狀態從 "true" 切換為 "false" 條件，反之亦然，則針對轉譯順序中的每個反復專案。 "True" 和 "false" 的意義不是常值，這只是表示必須將狀態設定為相反的條件。 這會導致在分析期間測量狀態變更。 當然，您已瞭解如何使用查詢機制，並將轉譯順序放在迴圈中，以避免模式轉換的成本仍適用。

例如，以下是用來測量切換 z 測試開關成本的程式碼序列：


```
// Get the start counter value as shown in Example 4 

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the "false" condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Set the pipeline state to the "true" condition
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}

// Get the stop counter value as shown in Example 4 
```



範例5：測量切換狀態變更

迴圈會執行兩個 [**graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 呼叫來切換狀態。 第一個 **graphicsdevice** 呼叫會停用 z 測試，而第二個 **graphicsdevice** 則啟用 z 測試。 每個 **graphicsdevice** 後面都會接著 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ，如此一來，與狀態變更相關聯的工作就會由驅動程式處理，而不是只在驅動程式中設定中途的位。

這些數位對此轉譯順序而言是合理的：



| 區域變數 | 刻度數目 |
|----------------|-----------------|
| start          | 1792998845000   |
| stop           | 1792998861740   |
| 頻率           | 3579545         |



 

再次將刻度轉換成迴圈會產生：


```
# ticks  = (stop - start) = 1792998861740 - 1792998845000 = 15,120 ticks
# cycles    = machine speed * number of ticks / QPF
 9,300,000  = 2 GHz          * 16,740         / 3,579,545
```



除以迴圈中的反覆運算次數會產生：


```
9,300,000 cycles / 1500 iterations = 6200 cycles for one iteration
```



迴圈的每個反復專案都包含兩個狀態變更和兩個繪製呼叫。 將繪製呼叫減去 (假設1100迴圈) 離開：


```
6200 - 1100 - 1100 = 4000 cycles for both state changes
```



這是兩個狀態變更的平均週期數目，因此每個狀態變更的平均時間為：


```
4000 / 2  = 2000 cycles for each state change
```



因此，啟用或停用 z 測試的平均迴圈數目是2000週期。 值得注意的是，QueryPerformanceCounter 測量的是 z-啟用一半的時間和 z 停用半時間。 這項技術實際上會測量兩個狀態變更的平均值。 換句話說，您會測量切換狀態的時間。 使用這項技術，您就無法得知啟用和停用時間是否相等，因為您已測量兩者的平均值。 不過，這是合理的數位，可在將切換狀態的預算設為應用程式時使用，而此狀態變更只會切換此狀態來執行此作業。

現在您可以套用這些技術，並分析所有您想要的狀態變更，對吧？ 並不全是。 您仍然需要特別小心，其設計目的是要減少需要完成的工作量。 設計轉譯順序時，您應該注意兩種類型的優化。

### <a name="watch-out-for-state-change-optimizations"></a>留意狀態變更優化

上一節示範如何分析這兩種狀態變更：限制為每個反復專案產生相同工作量的簡單狀態變更，以及會大幅變更已完成工作量的切換狀態變更。 如果您採用先前的轉譯順序，並新增另一個狀態變更，會發生什麼事？ 比方說，這個範例會採用 z> 啟用轉譯順序，並對其新增 z func 比較：


```
// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZFUNC, D3DCMP_NEVER);

  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZFUNC, D3DCMP_ALWAYS);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}
```



當寫入至 z 緩衝區時，z-func 狀態會設定比較層級，在目前圖元的 z-值與深度緩衝區) 中圖元的 z 值之間 (之間。 D3DCMP \_ 絕對不會關閉 z 測試比較，D3DCMP \_ 一律會設定每次完成 z 測試時所發生的比較。

使用 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 來分析轉譯順序中的其中一個狀態變更，會產生類似以下的結果：



| 單一狀態變更 | 平均週期數 |
|---------------------|--------------------------|
| \_僅限 D3DRS ZENABLE | 2000                     |



 

或



| 單一狀態變更 | 平均週期數 |
|---------------------|--------------------------|
| \_僅限 D3DRS ZFUNC   | 600                      |



 

但是，如果您 \_ 在相同轉譯順序中同時分析 D3DRS ZENABLE 和 D3DRS \_ ZFUNC，您可能會看到如下所示的結果：



| 狀態變更            | 平均週期數 |
|-------------------------------|--------------------------|
| D3DRS \_ ZENABLE + D3DRS \_ ZFUNC | 2000                     |



 

您可能預期結果會是2000和 600 (或 2600) 迴圈的總和，因為驅動程式正在執行所有與設定這兩種轉譯狀態相關聯的工作。 相反地，平均是2000週期。

此結果反映在執行時間、驅動程式或 GPU 中實作為狀態變更優化。 在此情況下，驅動程式可能會看到第一個 [**graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 並設定變更狀態，以在稍後延遲工作。 當驅動程式看到第二個 **graphicsdevice** 時，相同的變更狀態可能是重複設定的，而且相同的工作也會再次延後。 呼叫 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 時，最後會處理與已變更狀態相關聯的工作。 驅動程式會執行工作一次，這表示驅動程式會將前兩個狀態變更有效地合併。 同樣地，當呼叫第二個 **DrawPrimitive** 時，驅動程式會將第三個和第四個狀態變更有效地合併為單一狀態變更。 最後的結果是，驅動程式和 GPU 會處理每個繪製呼叫的單一狀態變更。

這是與序列相依的驅動程式優化的良好範例。 驅動程式會藉由設定中途狀態進行延遲兩次，然後執行一次工作以清除變更狀態。 這是一個很好的範例，可在工作延遲到絕對必要時進行。

您如何知道哪些狀態變更會在內部設定變更狀態，因而將工作延後到稍後為止？ 只有透過測試轉譯順序 (或與驅動程式寫入器) 交談。 驅動程式會定期更新和改進，因此優化清單不是靜態的。 在一組特定的硬體上，有一個絕對知道特定轉譯順序中狀態變更成本的方式，也就是測量它。

### <a name="watch-out-for-drawprimitive-optimizations"></a>留意 DrawPrimitive 優化

除了狀態變更優化之外，執行時間會嘗試將驅動程式必須處理的繪圖呼叫數目優化。 例如，請將這些回送回 draw 呼叫：


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 3); // Draw 3 primitives, vertices 0 - 8
DrawPrimitive(D3DPT_TRIANGLELIST, 9, 4); // Draw 4 primitives, vertices 9 - 20
```



範例5a：兩個繪製呼叫

此序列包含兩個繪製呼叫，而執行時間會合並成單一呼叫，相當於：


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 7); // Draw 7 primitives, vertices 0 - 20
```



範例5b：單一串連的繪製呼叫

執行時間會將這兩個特定的繪製呼叫串連成單一呼叫，這會減少驅動程式的50%，因為驅動程式現在只需要處理一次繪製呼叫。

一般而言，執行時間會串連兩個或多個後端 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 呼叫：

1.  基本類型是 (D3DPT TRIANGLELIST) 的三角形清單 \_ 。
2.  每個後續的 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 呼叫都必須參考頂點緩衝區內的連續頂點。

同樣地，串連兩個或多個反向 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 呼叫的正確條件如下：

1.  基本類型是 (D3DPT TRIANGLELIST) 的三角形清單 \_ 。
2.  每個後續的 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 呼叫都必須連續參考索引緩衝區內的連續索引。
3.  每個後續的 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 呼叫都必須使用相同的 BaseVertexIndex 值。

若要在分析期間防止串連，請修改轉譯順序，讓基本型別不是三角形清單，或修改轉譯順序，如此一來，就不會使用連續頂點 (或索引) 的反向繪製呼叫。 更具體來說，執行時間也會串連符合下列兩個條件的繪製呼叫：

-   當先前的呼叫 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)時，如果下一個繪製呼叫：
    -   使用三角形清單，以及
    -   指定 StartVertex = previous StartVertex + previous PrimitiveCount \* 3
-   使用 [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)時，如果下一次繪製呼叫：
    -   使用三角形清單，以及
    -   指定 StartIndex = 上一個 StartIndex + 先前的 PrimitiveCount \* 3，以及
    -   指定 BaseVertexIndex = previous BaseVertexIndex

以下是更微妙的繪製呼叫串連範例，在分析時很容易忽略。 假設呈現順序如下所示：


```
  for(int i = 0; i < 1500; i++)
  {
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



範例5c：一個狀態變更和一個繪製呼叫

迴圈會逐一查看1500三角形、設定材質和繪製每個三角形。 這種轉譯迴圈大約需要2750迴圈來進行 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)的 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)和1100迴圈，如上一節所示。 您可能會認為，在轉譯迴圈外部移動 **SetTexture** 應該會減少驅動程式 1500 2750 週期所完成的工作量 \* ，也就是與呼叫 **SetTexture** 1500 時間相關聯的工作量。 程式碼片段看起來像這樣：


```
  SetTexture(...); // Set the state outside the loop
  for(int i = 0; i < 1500; i++)
  {
//    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



範例5d：在迴圈外部具有狀態變更的範例5c

在轉譯迴圈外部移動 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 可減少與 **SetTexture** 相關聯的工作量，因為它會被呼叫一次，而不是1500次。 較不明顯的次要效果是， [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 的工作也會從1500呼叫減少為1個呼叫，因為串連繪製呼叫的所有條件都已滿足。 處理轉譯順序時，執行時間會將1500呼叫處理成單一的驅動程式呼叫。 藉由移動這一行程式碼，就能大幅降低驅動程式的工作量：


```
total work done = runtime + driver work

Example 5c: with SetTexture in the loop:
runtime work = 1500 SetTextures + 1500 DrawPrimitives 
driver  work = 1500 SetTextures + 1500 DrawPrimitives 

Example 5d: with SetTexture outside of the loop:
runtime work = 1 SetTexture + 1 DrawPrimitive + 1499 Concatenated DrawPrimitives 
driver  work = 1 SetTexture + 1 DrawPrimitive 
```



這些結果都是正確的，但在原始問題的內容中非常誤導。 繪製呼叫優化造成大量的驅動程式工作量大幅減少。 這是執行自訂程式碼剖析時常見的問題。 從轉譯順序中刪除呼叫時，請小心避免繪製呼叫串連。 事實上，此案例是此執行時間優化可能改善驅動程式效能的強大範例。

現在您知道如何測量狀態變更。 從分析 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)開始。 然後，將每個額外的狀態變更新增至順序 (在某些情況下，新增一個呼叫，而在其他情況下，新增兩個呼叫) 並測量兩個序列之間的差異。 您可以將結果轉換成刻度或週期或時間。 就像使用 QueryPerformanceCounter 測量轉譯順序一樣，測量個別狀態變更依賴查詢機制來控制命令緩衝區，並將狀態變更放在迴圈中，以將模式轉換的影響降到最低。 這項技術會測量切換狀態的成本，因為分析工具會傳回啟用和停用狀態的平均值。

有了這項功能，您就可以開始產生任意轉譯順序，並精確地測量相關聯的執行時間和驅動程式工作。 然後，您可以使用這些數位來回答預算問題，例如「在轉譯順序中有多少以上的呼叫」，同時仍維持合理的畫面播放速率（假設 CPU 有限的案例）。

## <a name="summary"></a>摘要

本檔將示範如何控制命令緩衝區，以便能夠正確地分析個別呼叫。 程式碼剖析編號可以依滴答、迴圈或絕對時間產生。 它們代表與每個 API 呼叫相關聯的執行時間和驅動程式工作量。

一開始先分析轉譯 \* 順序中的繪製基本呼叫。 請記住：

1.  使用 QueryPerformanceCounter 測量每個 API 呼叫的刻度數目。 如果您想要的話，請使用 QueryPerformanceFrequency 將結果轉換為迴圈或時間。
2.  開始之前，請使用查詢機制清空命令緩衝區。
3.  在迴圈中包含轉譯順序，以將模式轉換的影響降至最低。
4.  使用查詢機制來測量 GPU 完成其工作的時間。
5.  請留意將對完成的工作量有重大影響的執行時間串連。

這可提供您 [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 的基準效能，可用於建立。 若要分析一個狀態變更，請遵循下列其他秘訣：

1.  將狀態變更新增至已知轉譯順序設定檔中的新序列。 由於測試是在迴圈中完成，因此必須將狀態設定為相反的值 (例如啟用和停用實例) 。
2.  比較兩個序列之間的週期時間差異。
3.  針對大幅變更管線 (如 [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) 的狀態變更，請減少兩個序列之間的差異，以取得狀態變更的時間。
4.  針對大幅變更管線 (的狀態變更，因此需要切換狀態，例如 [**graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) ，請減少轉譯序列和除以2之間的差異。 這會產生每個狀態變更的平均迴圈數目。

但請小心在分析時造成非預期結果的優化。 狀態變更優化可能會設定造成工作延遲的變更狀態。 這可能會導致不像預期般直覺的設定檔結果。 已串連的繪製呼叫會大幅減少驅動程式工作，這可能會導致誤導的結論。 仔細規劃的轉譯順序可用來防止狀態變更，以及繪製呼叫串連。 秘訣是避免在程式碼剖析期間進行優化，讓您產生的數位為合理的預算數位。

> [!Note]  
> 在沒有查詢機制的情況下，在應用程式中複製此程式碼剖析策略比較困難。 在 Direct3D 9 之前，唯一可預測的命令緩衝區方法是鎖定使用中的介面 (例如轉譯目標) 等候，直到 GPU 閒置為止。 這是因為鎖定介面會強制執行時間清空命令緩衝區，以防緩衝區中的任何轉譯命令都應該在鎖定之前更新介面，以及等待 GPU 完成。 這項技術可正常運作，但使用 Direct3D 9 所引進的查詢機制更內斂。

 

## <a name="appendix"></a>附錄

這份表格中的數位是與每個狀態變更相關聯的執行時間和驅動程式工作量的範圍。 近似值是根據使用紙張中所示技術在驅動程式上進行的實際度量。 這些數位是使用 Direct3D 9 執行時間產生的，而且與驅動程式相依。

這份檔中的技術是設計來測量執行時間和驅動程式的工作。 一般情況下，在每個應用程式中提供符合 CPU 和 GPU 效能的結果是不切實際的，因為這需要一組完整的轉譯順序。 此外，您也很難對 GPU 的效能進行基準測試，因為它在轉譯順序之前，會高度依賴管線中的狀態設定。 例如，啟用 Alpha 混合幾乎不會影響所需的 CPU 工作量，但可能對 GPU 所完成的工作量有很大的影響。 因此，本文中的技術會限制需要轉譯的資料量，以將 GPU 工作限制為最小數量。 這表示，資料表中的數位最符合 CPU 限制 (的應用程式所能達到的結果，而不是 GPU) 所限制的應用程式。

建議您使用所呈現的技巧，來涵蓋最重要的案例和設定。 資料表中的值可以用來與您產生的數位進行比較。 由於每個驅動程式都有變化，因此產生實際數位的唯一方法就是使用您的案例來產生分析結果。



| API 呼叫                             | 平均週期數 |
|--------------------------------------|--------------------------|
| SetVertexDeclaration                 | 6500-11250             |
| SetFVF                               | 6400-11200             |
| SetVertexShader                      | 3000-12100             |
| SetPixelShader                       | 6300-7000              |
| SPECULARENABLE                       | 1900-11200             |
| SetRenderTarget                      | 6000-6250              |
| SetPixelShaderConstant (1 常數)   | 1500-9000              |
| NORMALIZENORMALS                     | 2200-8100              |
| LightEnable                          | 1300-9000              |
| SetStreamSource                      | 3700-5800              |
| 照明                             | 1700-7500              |
| DIFFUSEMATERIALSOURCE                | 900-8300               |
| AMBIENTMATERIALSOURCE                | 900-8200               |
| COLORVERTEX                          | 800-7800               |
| SetLight                             | 2200-5100              |
| SetTransform                         | 3200-3750              |
| SetIndices                           | 900-5600               |
| 環境                              | 1150-4800              |
| SetTexture                           | 2500-3100              |
| SPECULARMATERIALSOURCE               | 900-4600               |
| EMISSIVEMATERIALSOURCE               | 900-4500               |
| SetMaterial                          | 1000-3700              |
| ZENABLE                              | 700-3900               |
| WRAP0                                | 1600-2700              |
| MINFILTER                            | 1700-2500              |
| MAGFILTER                            | 1700-2400              |
| SetVertexShaderConstant (1 常數)  | 1000-2700              |
| COLOROP                              | 1500-2100              |
| COLORARG2                            | 1300-2000              |
| COLORARG1                            | 1300-1980              |
| CULLMODE                             | 500-2570               |
| 裁剪                             | 500-2550               |
| DrawIndexedPrimitive                 | 1200-1400              |
| ADDRESSV                             | 1090-1500              |
| ADDRESSU                             | 1070-1500              |
| DrawPrimitive                        | 1050-1150              |
| SRGBTEXTURE                          | 150-1500               |
| STENCILMASK                          | 570-700                |
| STENCILZFAIL                         | 500-800                |
| STENCILREF                           | 550-700                |
| ALPHABLENDENABLE                     | 550-700                |
| STENCILFUNC                          | 560-680                |
| STENCILWRITEMASK                     | 520-700                |
| STENCILFAIL                          | 500-750                |
| ZFUNC                                | 510-700                |
| ZWRITEENABLE                         | 520-680                |
| STENCILENABLE                        | 540-650                |
| STENCILPASS                          | 560-630                |
| SRCBLEND                             | 500-685                |
| 雙 \_ 側 \_ StencilMODE              | 450-590                |
| ALPHATESTENABLE                      | 470-525                |
| ALPHAREF                             | 460-530                |
| ALPHAFUNC                            | 450-540                |
| DESTBLEND                            | 475-510                |
| COLORWRITEENABLE                     | 465-515                |
| CCW \_ STENCILFAIL                     | 340-560                |
| CCW \_ STENCILPASS                     | 340-545                |
| CCW \_ STENCILZFAIL                    | 330-495                |
| SCISSORTESTENABLE                    | 375-440                |
| CCW \_ STENCILFUNC                     | 250-480                |
| SetScissorRect                       | 150-340                |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced 主題](advanced-topics.md)
</dt> </dl>

 

 
