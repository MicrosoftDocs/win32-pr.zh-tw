---
title: 間接繪圖
description: 間接繪圖可讓您將一些場景遍歷和剔除從 CPU 移至 GPU，進而改善效能。 命令緩衝區可以由 CPU 或 GPU 產生。
ms.assetid: F8D6C88A-101E-4F66-999F-43206F6527B6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55070bead6f848777cb81dd7fb33878ddcf7954a7f8a4fbb55f4ab9c01d4cea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123843"
---
# <a name="indirect-drawing"></a>間接繪圖

間接繪圖可讓您將一些場景遍歷和剔除從 CPU 移至 GPU，進而改善效能。 命令緩衝區可以由 CPU 或 GPU 產生。

-   [命令簽章](#command-signatures)
-   [間接引數緩衝區結構](#indirect-argument-buffer-structures)
-   [建立命令簽名](#command-signature-creation)
    -   [無引數變更](#no-argument-changes)
    -   [根常數和頂點緩衝區](#root-constants-and-vertex-buffers)
-   [相關主題](#related-topics)

## <a name="command-signatures"></a>命令簽章

命令簽名物件 ([**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)) 可讓應用程式指定間接繪圖，特別是設定下列各項：

-   間接引數緩衝區格式。
-   將從 [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 方法 [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)、 [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)或 [**分派**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch))  (使用的命令類型。
-   這組資源系結會變更每個命令的呼叫，以及將繼承的集合。

在啟動時，應用程式會建立一組小型的 **命令** 簽章。 應用程式會在執行時間使用命令 (，透過應用程式開發人員選擇) 的任何方式來填滿緩衝區。 命令（選擇性）包含要為頂點緩衝區視圖設定的狀態、索引緩衝區查看、根常數和根描述項， (原始或結構化的 SRV/UAV/CBVs) 。 這些引數配置並非硬體專屬，因此應用程式可以直接產生緩衝區。 命令簽章會從命令清單繼承剩餘的狀態。 然後，應用程式會呼叫 [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) 來指示 GPU 根據特定命令簽章所定義的格式來解讀間接引數緩衝區的內容。

如果命令簽章變更任何根引數，則會以根簽章的子集的形式儲存在命令簽章中。

請注意，當執行完成時，命令簽章狀態不會流失回命令清單。

例如，假設應用程式開發人員想要在間接引數緩衝區中指定每個繪製呼叫的唯一根常數。 應用程式會建立命令簽章，讓間接引數緩衝區指定每個繪製呼叫的下列參數：

-   一個根常數的值。
-   Draw 引數 (頂點計數、實例計數等) 。

應用程式所產生的間接引數緩衝區會包含固定大小記錄的陣列。 每個結構都對應至一個繪製呼叫。 每個結構都包含繪圖引數，以及根常數的值。 繪製呼叫的數目是在個別 GPU 可見的緩衝區中指定。

應用程式所產生的命令緩衝區範例如下：

![命令緩衝區格式](images/indirect-drawing-command-buffer.png)

## <a name="indirect-argument-buffer-structures"></a>間接引數緩衝區結構

下列結構會定義特定引數在間接引數緩衝區中的顯示方式。 這些結構不會出現在任何 D3D12 API 中。 應用程式會在寫入具有 CPU 或 GPU) 的間接引數緩衝區 (時，使用這些定義：

-   [**D3D12 \_ DRAW \_ 引數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments)
-   [**D3D12 \_ 繪製 \_ 索引 \_ 引數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments)
-   [**D3D12 \_ 分派 \_ 引數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments)
-   [**D3D12 \_ 頂點 \_ 緩衝區 \_ 查看**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)
-   [**D3D12 \_ 索引 \_ 緩衝區 \_ 查看**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view)
-   D3D12 \_ GPU \_ 虛擬 \_ 位址 (typedef) 的同義字。
-   [**D3D12 \_ 常數 \_ 緩衝區 \_ 查看**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc)

## <a name="command-signature-creation"></a>建立命令簽名

若要建立命令簽名，請使用下列 API 專案：

-   [**ID3D12Device：： CreateCommandSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) (輸出 [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)) 
-   [**D3D12 \_ 間接 \_ 引數 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type)
-   [**D3D12 \_ 間接 \_ 引數 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc)
-   [**D3D12 \_ 命令 \_ 簽名 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

間接引數緩衝區內引數的順序定義為完全符合 [**D3D12 \_ 命令 \_ 簽名 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)的 *pArguments* 參數中指定的引數順序。 在間接引數緩衝區內，一個繪製 (圖形) /dispatch (計算) 呼叫的所有引數都會緊密地封裝。 但是，應用程式可以指定間接引數緩衝區中繪製/分派命令之間的任意位元組跨距。

只有當命令簽名變更其中一個根引數時，才必須指定根簽章。

對於根目錄 SRV/UAV/CBV，應用程式指定的大小是以位元組為單位。 Debug 層會驗證位址的下列限制：

-   CBV – address 必須是256個位元組的倍數。
-   原始 SRV/UAV – address 必須是4個位元組的倍數。
-   結構化 SRV/UAV – address 必須是在著色器) 中宣告 (結構位元組跨距的倍數。

給定的命令簽章可以是 draw 或 compute 命令簽章。 如果命令簽章包含繪圖作業，則它是圖形命令簽章。 否則，命令簽章必須包含分派作業，而且它是計算命令簽章。

下列各節顯示一些範例命令簽章。

### <a name="no-argument-changes"></a>無引數變更

在此範例中，應用程式所產生的間接引數緩衝區會保存36位元組結構的陣列。 每個結構只包含傳遞給 [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) (加上填補) 的五個參數。

建立命令簽名描述的程式碼如下：

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[1];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 36;
ProgramDesc.NumArgumentDescs = 1;
ProgramDesc.pArguments = Args;
```

間接引數緩衝區內單一結構的版面配置如下：



| 位元組 | 描述           |
|-------|-----------------------|
| 0:3   | IndexCountPerInstance |
| 4:7   | InstanceCount         |
| 8:11  | StartIndexLocation    |
| 12:15 | BaseVertexLocation    |
| 16:19 | StartInstanceLocation |
| 20:35 | 填補               |



 

### <a name="root-constants-and-vertex-buffers"></a>根常數和頂點緩衝區

在此範例中，間接引數緩衝區中的每個結構都會變更兩個根常數、變更一個頂點緩衝區系結，以及執行一個繪圖非索引作業。 結構之間沒有任何填補。

建立命令簽名描述的程式碼為：

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[4];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[0].Constant.RootParameterIndex = 2;
Args[0].Constant.DestOffsetIn32BitValues = 0;
Args[0].Constant.Num32BitValuesToSet = 1;

Args[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[1].Constant.RootParameterIndex = 6;
Args[1].Constant.DestOffsetIn32BitValues = 0;
Args[1].Constant.Num32BitValuesToSet = 1;

Args[2].Type = D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW;
Args[2].VertexBuffer.Slot = 3;

Args[3].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 40;
ProgramDesc.NumArgumentDescs = 4;
ProgramDesc.pArguments = Args;
```

間接引數緩衝區內的單一結構版面配置如下所示：



| 位元組 | 描述                               |
|-------|-------------------------------------------|
| 0:3   | 根參數索引2的資料           |
| 4:7   | 根參數索引6的資料           |
| 8:15  | 位於插槽3的 VB 的虛擬位址 (64 位)   |
| 16:19 | VB 大小                                   |
| 20:23 | VB stride                                 |
| 24:27 | VertexCountPerInstance                    |
| 28:31 | InstanceCount                             |
| 32:35 | StartVertexLocation                       |
| 36:39 | StartInstanceLocation                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX advanced learning 影片教學課程：執行間接和非同步 GPU 剔除](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[間接繪圖和 GPU 剔除：程式碼逐步解說](indirect-drawing-and-gpu-culling-.md)
</dt> <dt>

[轉譯](rendering.md)
</dt> </dl>

 

 
