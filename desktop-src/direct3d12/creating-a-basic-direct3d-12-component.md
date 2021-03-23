---
title: 建立基本的 Direct3D 12 元件
description: 本主題說明建立基本 Direct3D 12 元件的呼叫流程。
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "104758858"
---
# <a name="creating-a-basic-direct3d-12-component"></a><span data-ttu-id="0db3d-103">建立基本的 Direct3D 12 元件</span><span class="sxs-lookup"><span data-stu-id="0db3d-103">Creating a basic Direct3D 12 component</span></span>

> [!NOTE]
> <span data-ttu-id="0db3d-104">請參閱適用于 DirectX 12 圖形範例的 [Directx 圖形範例](https://github.com/Microsoft/DirectX-Graphics-Samples) 存放庫，其示範如何針對 Windows 10 建立需要大量圖形的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0db3d-104">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="0db3d-105">本主題說明建立基本 Direct3D 12 元件的呼叫流程。</span><span class="sxs-lookup"><span data-stu-id="0db3d-105">This topic describes the call flow to create a basic Direct3D 12 component.</span></span>

-   [<span data-ttu-id="0db3d-106">簡單應用程式的程式碼流程</span><span class="sxs-lookup"><span data-stu-id="0db3d-106">Code flow for a simple app</span></span>](#code-flow-for-a-simple-app)
    -   [<span data-ttu-id="0db3d-107">初始化</span><span class="sxs-lookup"><span data-stu-id="0db3d-107">Initialize</span></span>](#initialize)
    -   [<span data-ttu-id="0db3d-108">更新</span><span class="sxs-lookup"><span data-stu-id="0db3d-108">Update</span></span>](#update)
    -   [<span data-ttu-id="0db3d-109">轉譯</span><span class="sxs-lookup"><span data-stu-id="0db3d-109">Render</span></span>](#render)
    -   [<span data-ttu-id="0db3d-110">摧毀</span><span class="sxs-lookup"><span data-stu-id="0db3d-110">Destroy</span></span>](#destroy)
-   [<span data-ttu-id="0db3d-111">簡單應用程式的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="0db3d-111">Code example for a simple app</span></span>](#code-example-for-a-simple-app)
    -   [<span data-ttu-id="0db3d-112">類別 D3D12HelloTriangle</span><span class="sxs-lookup"><span data-stu-id="0db3d-112">class D3D12HelloTriangle</span></span>](#class-d3d12hellotriangle)
    -   [<span data-ttu-id="0db3d-113">OnInit () </span><span class="sxs-lookup"><span data-stu-id="0db3d-113">OnInit()</span></span>](#oninit)
    -   [<span data-ttu-id="0db3d-114">LoadPipeline () </span><span class="sxs-lookup"><span data-stu-id="0db3d-114">LoadPipeline()</span></span>](#loadpipeline)
    -   [<span data-ttu-id="0db3d-115">LoadAssets () </span><span class="sxs-lookup"><span data-stu-id="0db3d-115">LoadAssets()</span></span>](#loadassets)
    -   [<span data-ttu-id="0db3d-116">OnUpdate () </span><span class="sxs-lookup"><span data-stu-id="0db3d-116">OnUpdate()</span></span>](#onupdate)
    -   [<span data-ttu-id="0db3d-117">OnRender () </span><span class="sxs-lookup"><span data-stu-id="0db3d-117">OnRender()</span></span>](#onrender)
    -   [<span data-ttu-id="0db3d-118">PopulateCommandList () </span><span class="sxs-lookup"><span data-stu-id="0db3d-118">PopulateCommandList()</span></span>](#populatecommandlist)
    -   [<span data-ttu-id="0db3d-119">WaitForPreviousFrame () </span><span class="sxs-lookup"><span data-stu-id="0db3d-119">WaitForPreviousFrame()</span></span>](#waitforpreviousframe)
    -   [<span data-ttu-id="0db3d-120">OnDestroy () </span><span class="sxs-lookup"><span data-stu-id="0db3d-120">OnDestroy()</span></span>](#ondestroy)
-   [<span data-ttu-id="0db3d-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="0db3d-121">Related topics</span></span>](#related-topics)

## <a name="code-flow-for-a-simple-app"></a><span data-ttu-id="0db3d-122">簡單應用程式的程式碼流程</span><span class="sxs-lookup"><span data-stu-id="0db3d-122">Code flow for a simple app</span></span>

<span data-ttu-id="0db3d-123">D3D 12 程式的最外層迴圈遵循非常標準的圖形流程：</span><span class="sxs-lookup"><span data-stu-id="0db3d-123">The outermost loop of a D3D 12 program follows a very standard graphics process:</span></span>

> [!TIP]
> <span data-ttu-id="0db3d-124">Direct3D 12 的新功能後面會加上附注。</span><span class="sxs-lookup"><span data-stu-id="0db3d-124">Features new to Direct3D 12 are followed by a note.</span></span>

-   [<span data-ttu-id="0db3d-125">初始化</span><span class="sxs-lookup"><span data-stu-id="0db3d-125">Initialize</span></span>](#initialize)
-   <span data-ttu-id="0db3d-126">**重複**</span><span class="sxs-lookup"><span data-stu-id="0db3d-126">**Repeat**</span></span>
    -   [<span data-ttu-id="0db3d-127">更新</span><span class="sxs-lookup"><span data-stu-id="0db3d-127">Update</span></span>](#update)
    -   [<span data-ttu-id="0db3d-128">轉譯</span><span class="sxs-lookup"><span data-stu-id="0db3d-128">Render</span></span>](#render)
-   [<span data-ttu-id="0db3d-129">摧毀</span><span class="sxs-lookup"><span data-stu-id="0db3d-129">Destroy</span></span>](#destroy)

### <a name="initialize"></a><span data-ttu-id="0db3d-130">初始化</span><span class="sxs-lookup"><span data-stu-id="0db3d-130">Initialize</span></span>

<span data-ttu-id="0db3d-131">初始化牽涉到先設定全域變數和類別，而 initialize 函數必須準備管線和資產。</span><span class="sxs-lookup"><span data-stu-id="0db3d-131">Initialization involves first setting up the global variables and classes, and an initialize function must prepare the pipeline and assets.</span></span>

-   <span data-ttu-id="0db3d-132">初始化管線。</span><span class="sxs-lookup"><span data-stu-id="0db3d-132">Initialize the pipeline.</span></span>
    -   <span data-ttu-id="0db3d-133">啟用 debug 層。</span><span class="sxs-lookup"><span data-stu-id="0db3d-133">Enable the debug layer.</span></span>
    -   <span data-ttu-id="0db3d-134">建立裝置。</span><span class="sxs-lookup"><span data-stu-id="0db3d-134">Create the device.</span></span>
    -   <span data-ttu-id="0db3d-135">建立命令佇列。</span><span class="sxs-lookup"><span data-stu-id="0db3d-135">Create the command queue.</span></span>
    -   <span data-ttu-id="0db3d-136">建立交換鏈。</span><span class="sxs-lookup"><span data-stu-id="0db3d-136">Create the swap chain.</span></span>
    -   <span data-ttu-id="0db3d-137">建立呈現目標視圖 (RTV) 描述元堆積。</span><span class="sxs-lookup"><span data-stu-id="0db3d-137">Create a render target view (RTV) descriptor heap.</span></span>
        > [!Note]  
        > <span data-ttu-id="0db3d-138">[描述元堆積](descriptor-heaps.md)可以視為[描述](descriptors.md)項的陣列。</span><span class="sxs-lookup"><span data-stu-id="0db3d-138">A [descriptor heap](descriptor-heaps.md) can be thought of as an array of [descriptors](descriptors.md).</span></span> <span data-ttu-id="0db3d-139">其中，每個描述項會完整地描述 GPU 的物件。</span><span class="sxs-lookup"><span data-stu-id="0db3d-139">Where each descriptor fully describes an object to the GPU.</span></span>

    -   <span data-ttu-id="0db3d-140">針對每個畫面格)  (呈現目標視圖建立框架資源。</span><span class="sxs-lookup"><span data-stu-id="0db3d-140">Create frame resources (a render target view for each frame).</span></span>
    -   <span data-ttu-id="0db3d-141">建立命令配置器。</span><span class="sxs-lookup"><span data-stu-id="0db3d-141">Create a command allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="0db3d-142">命令配置器會管理 [命令清單和](recording-command-lists-and-bundles.md)組合的基礎儲存體。</span><span class="sxs-lookup"><span data-stu-id="0db3d-142">A command allocator manages the underlying storage for [command lists and bundles](recording-command-lists-and-bundles.md).</span></span>
         
-   <span data-ttu-id="0db3d-143">將資產初始化。</span><span class="sxs-lookup"><span data-stu-id="0db3d-143">Initialize the assets.</span></span>
    -   <span data-ttu-id="0db3d-144">建立空的根簽章。</span><span class="sxs-lookup"><span data-stu-id="0db3d-144">Create an empty root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="0db3d-145">圖形 [根](root-signatures.md) 簽章會定義哪些資源系結至圖形管線。</span><span class="sxs-lookup"><span data-stu-id="0db3d-145">A graphics [root signature](root-signatures.md) defines what resources are bound to the graphics pipeline.</span></span>

    -   <span data-ttu-id="0db3d-146">編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="0db3d-146">Compile the shaders.</span></span>
    -   <span data-ttu-id="0db3d-147">建立頂點輸入版面配置。</span><span class="sxs-lookup"><span data-stu-id="0db3d-147">Create the vertex input layout.</span></span>
    -   <span data-ttu-id="0db3d-148">建立 [管線狀態物件](managing-graphics-pipeline-state-in-direct3d-12.md) 描述，然後建立物件。</span><span class="sxs-lookup"><span data-stu-id="0db3d-148">Create a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) description, then create the object.</span></span>
        > [!Note]  
        > <span data-ttu-id="0db3d-149">管線狀態物件會維護所有目前設定著色器的狀態，以及特定的固定函式狀態物件 (例如 *輸入* 組合語言、 *tesselator* *、轉譯* 器和 *輸出合併*) 。</span><span class="sxs-lookup"><span data-stu-id="0db3d-149">A pipeline state object maintains the state of all currently set shaders as well as certain fixed function state objects (such as the *input assembler*, *tesselator*, *rasterizer* and *output merger*).</span></span>

    -   <span data-ttu-id="0db3d-150">建立命令清單。</span><span class="sxs-lookup"><span data-stu-id="0db3d-150">Create the command list.</span></span>
    -   <span data-ttu-id="0db3d-151">關閉命令清單。</span><span class="sxs-lookup"><span data-stu-id="0db3d-151">Close the command list.</span></span>
    -   <span data-ttu-id="0db3d-152">建立和載入頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0db3d-152">Create and load the vertex buffers.</span></span>
    -   <span data-ttu-id="0db3d-153">建立頂點緩衝區查看。</span><span class="sxs-lookup"><span data-stu-id="0db3d-153">Create the vertex buffer views.</span></span>
    -   <span data-ttu-id="0db3d-154">建立隔離。</span><span class="sxs-lookup"><span data-stu-id="0db3d-154">Create a fence.</span></span>
        > [!Note]  
        > <span data-ttu-id="0db3d-155">使用範圍將 CPU 與 GPU 同步處理 (查看 [多引擎同步](./user-mode-heap-synchronization.md) 處理) 。</span><span class="sxs-lookup"><span data-stu-id="0db3d-155">A fence is used to synchronize the CPU with the GPU (see [Multi-engine synchronization](./user-mode-heap-synchronization.md)).</span></span>

    -   <span data-ttu-id="0db3d-156">建立事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="0db3d-156">Create an event handle.</span></span>
    -   <span data-ttu-id="0db3d-157">等候 GPU 完成。</span><span class="sxs-lookup"><span data-stu-id="0db3d-157">Wait for the GPU to finish.</span></span>
        > [!Note]  
        > <span data-ttu-id="0db3d-158">檢查範圍！</span><span class="sxs-lookup"><span data-stu-id="0db3d-158">Check on the fence!</span></span>

<span data-ttu-id="0db3d-159">請參閱 [類別 D3D12HelloTriangle](#class-d3d12hellotriangle)、 [OnInit](#oninit)、 [LoadPipeline](#loadpipeline) 和 [LoadAssets](#loadassets)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-159">Refer to [class D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) and [LoadAssets](#loadassets).</span></span>

### <a name="update"></a><span data-ttu-id="0db3d-160">更新</span><span class="sxs-lookup"><span data-stu-id="0db3d-160">Update</span></span>

<span data-ttu-id="0db3d-161">更新自最後一個畫面格之後應變更的所有專案。</span><span class="sxs-lookup"><span data-stu-id="0db3d-161">Update everything that should change since the last frame.</span></span>

-   <span data-ttu-id="0db3d-162">視需要修改常數、頂點、索引緩衝區和其他專案。</span><span class="sxs-lookup"><span data-stu-id="0db3d-162">Modify the constant, vertex, index buffers, and everything else, as necessary.</span></span>

<span data-ttu-id="0db3d-163">請參閱 [OnUpdate](#onupdate)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-163">Refer to [OnUpdate](#onupdate).</span></span>

### <a name="render"></a><span data-ttu-id="0db3d-164">轉譯</span><span class="sxs-lookup"><span data-stu-id="0db3d-164">Render</span></span>

<span data-ttu-id="0db3d-165">繪製新世界。</span><span class="sxs-lookup"><span data-stu-id="0db3d-165">Draw the new world.</span></span>

-   <span data-ttu-id="0db3d-166">填入命令清單。</span><span class="sxs-lookup"><span data-stu-id="0db3d-166">Populate the command list.</span></span>
    -   <span data-ttu-id="0db3d-167">重設命令清單配置器。</span><span class="sxs-lookup"><span data-stu-id="0db3d-167">Reset the command list allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="0db3d-168">重複使用與命令配置器相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="0db3d-168">Re-use the memory that is associated with the command allocator.</span></span>

         

    -   <span data-ttu-id="0db3d-169">重設命令清單。</span><span class="sxs-lookup"><span data-stu-id="0db3d-169">Reset the command list.</span></span>
    -   <span data-ttu-id="0db3d-170">設定圖形根簽章。</span><span class="sxs-lookup"><span data-stu-id="0db3d-170">Set the graphics root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="0db3d-171">設定要用於目前命令清單的圖形根簽章。</span><span class="sxs-lookup"><span data-stu-id="0db3d-171">Sets the graphics root signature to use for the current command list.</span></span>

         

    -   <span data-ttu-id="0db3d-172">設定 [視口] 和 [剪式矩形]。</span><span class="sxs-lookup"><span data-stu-id="0db3d-172">Set the viewport and scissor rectangles.</span></span>
    -   <span data-ttu-id="0db3d-173">設定資源關卡，表示將會使用背景緩衝區做為呈現目標。</span><span class="sxs-lookup"><span data-stu-id="0db3d-173">Set a resource barrier, indicating the back buffer is to be used as a render target.</span></span>
        > [!Note]  
        > <span data-ttu-id="0db3d-174">資源障礙可用來管理資源轉換。</span><span class="sxs-lookup"><span data-stu-id="0db3d-174">Resource barriers are used to manage resource transitions.</span></span>

         

    -   <span data-ttu-id="0db3d-175">將命令記錄到命令清單中。</span><span class="sxs-lookup"><span data-stu-id="0db3d-175">Record commands into the command list.</span></span>
    -   <span data-ttu-id="0db3d-176">指出在執行命令清單之後，會使用背景緩衝區來顯示。</span><span class="sxs-lookup"><span data-stu-id="0db3d-176">Indicate the back buffer will be used to present after the command list has executed.</span></span>
        > [!Note]  
        > <span data-ttu-id="0db3d-177">另一個設定資源屏障的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0db3d-177">Another call to set a resource barrier.</span></span>

         

    -   <span data-ttu-id="0db3d-178">關閉命令清單以進行進一步的錄製。</span><span class="sxs-lookup"><span data-stu-id="0db3d-178">Close the command list to further recording.</span></span>
-   <span data-ttu-id="0db3d-179">執行命令清單。</span><span class="sxs-lookup"><span data-stu-id="0db3d-179">Execute the command list.</span></span>
-   <span data-ttu-id="0db3d-180">呈現畫面格。</span><span class="sxs-lookup"><span data-stu-id="0db3d-180">Present the frame.</span></span>
-   <span data-ttu-id="0db3d-181">等候 GPU 完成。</span><span class="sxs-lookup"><span data-stu-id="0db3d-181">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="0db3d-182">繼續更新和檢查隔離。</span><span class="sxs-lookup"><span data-stu-id="0db3d-182">Keep updating and checking the fence.</span></span>

<span data-ttu-id="0db3d-183">請參閱 [OnRender](#onrender)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-183">Refer to [OnRender](#onrender).</span></span>

### <a name="destroy"></a><span data-ttu-id="0db3d-184">損毀</span><span class="sxs-lookup"><span data-stu-id="0db3d-184">Destroy</span></span>

<span data-ttu-id="0db3d-185">完全關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="0db3d-185">Cleanly close down the app.</span></span>

-   <span data-ttu-id="0db3d-186">等候 GPU 完成。</span><span class="sxs-lookup"><span data-stu-id="0db3d-186">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="0db3d-187">對範圍的最終檢查。</span><span class="sxs-lookup"><span data-stu-id="0db3d-187">Final check on the fence.</span></span>

-   <span data-ttu-id="0db3d-188">關閉事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="0db3d-188">Close the event handle.</span></span>

<span data-ttu-id="0db3d-189">請參閱 [OnDestroy](#ondestroy)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-189">Refer to [OnDestroy](#ondestroy).</span></span>

## <a name="code-example-for-a-simple-app"></a><span data-ttu-id="0db3d-190">簡單應用程式的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="0db3d-190">Code example for a simple app</span></span>

<span data-ttu-id="0db3d-191">下列程式碼會展開上述的程式碼流程，以包含基本範例所需的程式碼。</span><span class="sxs-lookup"><span data-stu-id="0db3d-191">The following expands the code flow above to include the code required for a basic sample.</span></span>

### <a name="class-d3d12hellotriangle"></a><span data-ttu-id="0db3d-192">類別 D3D12HelloTriangle</span><span class="sxs-lookup"><span data-stu-id="0db3d-192">class D3D12HelloTriangle</span></span>

<span data-ttu-id="0db3d-193">首先，在標頭檔中定義類別，包括使用結構的視口、剪式矩形和頂點緩衝區：</span><span class="sxs-lookup"><span data-stu-id="0db3d-193">First define the class in a header file, including a viewport, scissor rectangle and vertex buffer using the structures:</span></span>

-   [<span data-ttu-id="0db3d-194">**D3D12 \_ 區**</span><span class="sxs-lookup"><span data-stu-id="0db3d-194">**D3D12\_VIEWPORT**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [<span data-ttu-id="0db3d-195">**D3D12 \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="0db3d-195">**D3D12\_RECT**</span></span>](d3d12-rect.md)
-   [<span data-ttu-id="0db3d-196">**D3D12 \_ 頂點 \_ 緩衝區 \_ 查看**</span><span class="sxs-lookup"><span data-stu-id="0db3d-196">**D3D12\_VERTEX\_BUFFER\_VIEW**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

```cpp
#include "DXSample.h"

using namespace DirectX;
using namespace Microsoft::WRL;

class D3D12HelloTriangle : public DXSample
{
public:
    D3D12HelloTriangle(UINT width, UINT height, std::wstring name);

    virtual void OnInit();
    virtual void OnUpdate();
    virtual void OnRender();
    virtual void OnDestroy();

private:
    static const UINT FrameCount = 2;

    struct Vertex
    {
        XMFLOAT3 position;
        XMFLOAT4 color;
    };

    // Pipeline objects.
    D3D12_VIEWPORT m_viewport;
    D3D12_RECT m_scissorRect;
    ComPtr<IDXGISwapChain3> m_swapChain;
    ComPtr<ID3D12Device> m_device;
    ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
    ComPtr<ID3D12CommandAllocator> m_commandAllocator;
    ComPtr<ID3D12CommandQueue> m_commandQueue;
    ComPtr<ID3D12RootSignature> m_rootSignature;
    ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
    ComPtr<ID3D12PipelineState> m_pipelineState;
    ComPtr<ID3D12GraphicsCommandList> m_commandList;
    UINT m_rtvDescriptorSize;

    // App resources.
    ComPtr<ID3D12Resource> m_vertexBuffer;
    D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;

    // Synchronization objects.
    UINT m_frameIndex;
    HANDLE m_fenceEvent;
    ComPtr<ID3D12Fence> m_fence;
    UINT64 m_fenceValue;

    void LoadPipeline();
    void LoadAssets();
    void PopulateCommandList();
    void WaitForPreviousFrame();
};
```

### <a name="oninit"></a><span data-ttu-id="0db3d-197">OnInit () </span><span class="sxs-lookup"><span data-stu-id="0db3d-197">OnInit()</span></span>

<span data-ttu-id="0db3d-198">在專案的主要來源檔案中，開始初始化物件：</span><span class="sxs-lookup"><span data-stu-id="0db3d-198">In the projects main source file, start initializing the objects:</span></span>

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a><span data-ttu-id="0db3d-199">LoadPipeline () </span><span class="sxs-lookup"><span data-stu-id="0db3d-199">LoadPipeline()</span></span>

<span data-ttu-id="0db3d-200">下列程式碼會建立圖形管線的基本概念。</span><span class="sxs-lookup"><span data-stu-id="0db3d-200">The following code creates the basics for a graphics pipeline.</span></span> <span data-ttu-id="0db3d-201">建立裝置和交換鏈的程式與 Direct3D 11 非常類似。</span><span class="sxs-lookup"><span data-stu-id="0db3d-201">The process of creating devices and swap chains is very similar to Direct3D 11.</span></span>

-   <span data-ttu-id="0db3d-202">啟用 debug 層，並呼叫：</span><span class="sxs-lookup"><span data-stu-id="0db3d-202">Enable the debug layer, with calls to:</span></span><dl>

[<span data-ttu-id="0db3d-203">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="0db3d-203">**D3D12GetDebugInterface**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [<span data-ttu-id="0db3d-204">**ID3D12Debug::EnableDebugLayer**</span><span class="sxs-lookup"><span data-stu-id="0db3d-204">**ID3D12Debug::EnableDebugLayer**</span></span>](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   <span data-ttu-id="0db3d-205">建立裝置：</span><span class="sxs-lookup"><span data-stu-id="0db3d-205">Create the device:</span></span><dl>

[<span data-ttu-id="0db3d-206">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="0db3d-206">**CreateDXGIFactory1**</span></span>](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [<span data-ttu-id="0db3d-207">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="0db3d-207">**D3D12CreateDevice**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   <span data-ttu-id="0db3d-208">填寫命令佇列描述，然後建立命令佇列：</span><span class="sxs-lookup"><span data-stu-id="0db3d-208">Fill out a command queue description, then create the command queue:</span></span><dl>

[<span data-ttu-id="0db3d-209">**D3D12 \_ 命令 \_ 佇列 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="0db3d-209">**D3D12\_COMMAND\_QUEUE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [<span data-ttu-id="0db3d-210">**ID3D12Device::CreateCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="0db3d-210">**ID3D12Device::CreateCommandQueue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   <span data-ttu-id="0db3d-211">填寫 swapchain 描述，然後建立交換鏈：</span><span class="sxs-lookup"><span data-stu-id="0db3d-211">Fill out a swapchain description, then create the swap chain:</span></span> <dl>

[<span data-ttu-id="0db3d-212">**DXGI \_ 交換 \_ 鏈 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="0db3d-212">**DXGI\_SWAP\_CHAIN\_DESC**</span></span>](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [<span data-ttu-id="0db3d-213">**IDXGIFactory::CreateSwapChain**</span><span class="sxs-lookup"><span data-stu-id="0db3d-213">**IDXGIFactory::CreateSwapChain**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [<span data-ttu-id="0db3d-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span><span class="sxs-lookup"><span data-stu-id="0db3d-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span></span>](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   <span data-ttu-id="0db3d-215">填寫堆積描述。</span><span class="sxs-lookup"><span data-stu-id="0db3d-215">Fill out a heap description.</span></span> <span data-ttu-id="0db3d-216">然後建立描述元堆積：</span><span class="sxs-lookup"><span data-stu-id="0db3d-216">then create a descriptor heap:</span></span> <dl>

[<span data-ttu-id="0db3d-217">**D3D12 \_ 描述元 \_ 堆積 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="0db3d-217">**D3D12\_DESCRIPTOR\_HEAP\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [<span data-ttu-id="0db3d-218">**ID3D12Device::CreateDescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="0db3d-218">**ID3D12Device::CreateDescriptorHeap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [<span data-ttu-id="0db3d-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span><span class="sxs-lookup"><span data-stu-id="0db3d-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   <span data-ttu-id="0db3d-220">建立轉譯目標視圖：</span><span class="sxs-lookup"><span data-stu-id="0db3d-220">Create the render target view:</span></span> <dl>

[<span data-ttu-id="0db3d-221">**CD3DX12 \_ CPU \_ 描述項 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="0db3d-221">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE**</span></span>](cd3dx12-cpu-descriptor-handle.md)  
    [<span data-ttu-id="0db3d-222">**GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="0db3d-222">**GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="0db3d-223">**IDXGISwapChain：： GetBuffer**</span><span class="sxs-lookup"><span data-stu-id="0db3d-223">**IDXGISwapChain::GetBuffer**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [<span data-ttu-id="0db3d-224">**ID3D12Device::CreateRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="0db3d-224">**ID3D12Device::CreateRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   <span data-ttu-id="0db3d-225">建立命令配置器： [**ID3D12Device：： CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-225">Create the command allocator: [**ID3D12Device::CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span></span>

<span data-ttu-id="0db3d-226">在稍後的步驟中，會從命令配置器取得命令清單，並提交至命令佇列。</span><span class="sxs-lookup"><span data-stu-id="0db3d-226">In later steps, command lists are obtained from the command allocator and submitted to the command queue.</span></span>

<span data-ttu-id="0db3d-227">載入轉譯管線相依性 (請注意，建立軟體變形裝置完全是選擇性的) 。</span><span class="sxs-lookup"><span data-stu-id="0db3d-227">Load the rendering pipeline dependencies (note that the creation of a software WARP device is entirely optional).</span></span>


```cpp
void D3D12HelloTriangle::LoadPipeline()
{
#if defined(_DEBUG)
    // Enable the D3D12 debug layer.
    {
        
        ComPtr<ID3D12Debug> debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
        {
            debugController->EnableDebugLayer();
        }
    }
#endif

    ComPtr<IDXGIFactory4> factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

    if (m_useWarpDevice)
    {
        ComPtr<IDXGIAdapter> warpAdapter;
        ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }
    else
    {
        ComPtr<IDXGIAdapter1> hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

    // Describe and create the swap chain.
    DXGI_SWAP_CHAIN_DESC swapChainDesc = {};
    swapChainDesc.BufferCount = FrameCount;
    swapChainDesc.BufferDesc.Width = m_width;
    swapChainDesc.BufferDesc.Height = m_height;
    swapChainDesc.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
    swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
    swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;
    swapChainDesc.OutputWindow = Win32Application::GetHwnd();
    swapChainDesc.SampleDesc.Count = 1;
    swapChainDesc.Windowed = TRUE;

    ComPtr<IDXGISwapChain> swapChain;
    ThrowIfFailed(factory->CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &swapChainDesc,
        &swapChain
        ));

    ThrowIfFailed(swapChain.As(&m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory->MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
            rtvHandle.Offset(1, m_rtvDescriptorSize);
        }
    }

    ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
}
```



### <a name="loadassets"></a><span data-ttu-id="0db3d-228">LoadAssets () </span><span class="sxs-lookup"><span data-stu-id="0db3d-228">LoadAssets()</span></span>

<span data-ttu-id="0db3d-229">載入和準備資產是很耗時的程式。</span><span class="sxs-lookup"><span data-stu-id="0db3d-229">Loading and preparing assets is a lengthy process.</span></span> <span data-ttu-id="0db3d-230">其中有許多階段與 D3D 11 很類似，但有些則是 D3D 12 的新階段。</span><span class="sxs-lookup"><span data-stu-id="0db3d-230">Many of these stages are similar to D3D 11, though some are new to D3D 12.</span></span>

<span data-ttu-id="0db3d-231">在 Direct3D 12 中，必要的管線狀態會透過 [管線狀態物件](managing-graphics-pipeline-state-in-direct3d-12.md) 附加至命令清單， (PSO) 。</span><span class="sxs-lookup"><span data-stu-id="0db3d-231">In Direct3D 12, required pipeline state is attached to a command list via a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span></span> <span data-ttu-id="0db3d-232">此範例顯示如何建立 PSO。</span><span class="sxs-lookup"><span data-stu-id="0db3d-232">This example shows how to create a PSO.</span></span> <span data-ttu-id="0db3d-233">您可以將 PSO 儲存為成員變數，並視需要重複使用它多次。</span><span class="sxs-lookup"><span data-stu-id="0db3d-233">You can store the PSO as a member variable and reuse it as many times as needed.</span></span>

<span data-ttu-id="0db3d-234">描述元堆積會定義視圖，以及如何存取資源 (例如，呈現目標視圖) 。</span><span class="sxs-lookup"><span data-stu-id="0db3d-234">A descriptor heap defines the views and how to access resources (for example, a render target view).</span></span>

<span data-ttu-id="0db3d-235">使用命令清單配置器和 PSO，您可以建立實際的命令清單，稍後將會執行。</span><span class="sxs-lookup"><span data-stu-id="0db3d-235">With the command list allocator and PSO, you can create the actual command list, which will be executed at a later time.</span></span>

<span data-ttu-id="0db3d-236">系統會連續呼叫下列 Api 和進程。</span><span class="sxs-lookup"><span data-stu-id="0db3d-236">The following APIs and processes are called in succession.</span></span>

-   <span data-ttu-id="0db3d-237">使用可用的 helper 結構，建立空白的根簽章：</span><span class="sxs-lookup"><span data-stu-id="0db3d-237">Create an empty root signature, using the available helper structure:</span></span> <dl>

[<span data-ttu-id="0db3d-238">**CD3DX12 \_ 根目錄 \_ 簽名 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="0db3d-238">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md)  
    [<span data-ttu-id="0db3d-239">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="0db3d-239">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [<span data-ttu-id="0db3d-240">**ID3D12Device::CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="0db3d-240">**ID3D12Device::CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   <span data-ttu-id="0db3d-241">載入並編譯著色器： [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-241">Load and compile the shaders: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span></span>
-   <span data-ttu-id="0db3d-242">建立頂點輸入版面配置： [**D3D12 \_ 輸入 \_ 元素 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-242">Create the vertex input layout: [**D3D12\_INPUT\_ELEMENT\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span></span>
-   <span data-ttu-id="0db3d-243">使用可用的協助程式結構填寫管線狀態原因，然後建立圖形管線狀態：</span><span class="sxs-lookup"><span data-stu-id="0db3d-243">Fill out a pipeline state description, using the helper structures available, then create the graphics pipeline state:</span></span> <dl>

[<span data-ttu-id="0db3d-244">**D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="0db3d-244">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [<span data-ttu-id="0db3d-245">**CD3DX12 轉譯器 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="0db3d-245">**CD3DX12\_RASTERIZER\_DESC**</span></span>](cd3dx12-rasterizer-desc.md)  
    [<span data-ttu-id="0db3d-246">**CD3DX12 \_ BLEND \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="0db3d-246">**CD3DX12\_BLEND\_DESC**</span></span>](cd3dx12-blend-desc.md)  
    [<span data-ttu-id="0db3d-247">**ID3D12Device::CreateGraphicsPipelineState**</span><span class="sxs-lookup"><span data-stu-id="0db3d-247">**ID3D12Device::CreateGraphicsPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   <span data-ttu-id="0db3d-248">建立並關閉命令清單：</span><span class="sxs-lookup"><span data-stu-id="0db3d-248">Create, then close, a command list:</span></span> <dl>

[<span data-ttu-id="0db3d-249">**ID3D12Device::CreateCommandList**</span><span class="sxs-lookup"><span data-stu-id="0db3d-249">**ID3D12Device::CreateCommandList**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [<span data-ttu-id="0db3d-250">**ID3D12GraphicsCommandList：： Close**</span><span class="sxs-lookup"><span data-stu-id="0db3d-250">**ID3D12GraphicsCommandList::Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   <span data-ttu-id="0db3d-251">建立頂點緩衝區： [**ID3D12Device：： CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-251">Create the vertex buffer: [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>
-   <span data-ttu-id="0db3d-252">將頂點資料複製到頂點緩衝區：</span><span class="sxs-lookup"><span data-stu-id="0db3d-252">Copy the vertex data to the vertex buffer:</span></span><dl>

[<span data-ttu-id="0db3d-253">**ID3D12Resource：： Map**</span><span class="sxs-lookup"><span data-stu-id="0db3d-253">**ID3D12Resource::Map**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [<span data-ttu-id="0db3d-254">**ID3D12Resource：：取消對應**</span><span class="sxs-lookup"><span data-stu-id="0db3d-254">**ID3D12Resource::Unmap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   <span data-ttu-id="0db3d-255">初始化頂點緩衝區視圖： [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-255">Initialize the vertex buffer view: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span></span>
-   <span data-ttu-id="0db3d-256">建立並初始化隔離： [**ID3D12Device：： CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-256">Create and initialize the fence: [**ID3D12Device::CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span></span>
-   <span data-ttu-id="0db3d-257">建立與框架同步處理搭配使用的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="0db3d-257">Create an event handle for use with frame synchronization.</span></span>
-   <span data-ttu-id="0db3d-258">等候 GPU 完成。</span><span class="sxs-lookup"><span data-stu-id="0db3d-258">Wait for the GPU to finish.</span></span>


```cpp
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_UPLOAD);
        auto desc = CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize);
        ThrowIfFailed(m_device->CreateCommittedResource(
            &heapProps,
            D3D12_HEAP_FLAG_NONE,
            &desc,
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



### <a name="onupdate"></a><span data-ttu-id="0db3d-259">OnUpdate () </span><span class="sxs-lookup"><span data-stu-id="0db3d-259">OnUpdate()</span></span>

<span data-ttu-id="0db3d-260">針對簡單的範例，不會更新任何專案。</span><span class="sxs-lookup"><span data-stu-id="0db3d-260">For a simple example, nothing is updated.</span></span>


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a><span data-ttu-id="0db3d-261">OnRender () </span><span class="sxs-lookup"><span data-stu-id="0db3d-261">OnRender()</span></span>

<span data-ttu-id="0db3d-262">在設定期間，會使用成員變數 **m \_ commandList** 來記錄及執行所有設定的命令。</span><span class="sxs-lookup"><span data-stu-id="0db3d-262">During set up, the member variable **m\_commandList** was used to record and execute all of the set up commands.</span></span> <span data-ttu-id="0db3d-263">您現在可以在主要呈現迴圈中重複使用該成員。</span><span class="sxs-lookup"><span data-stu-id="0db3d-263">You can now reuse that member in the main render loop.</span></span>

<span data-ttu-id="0db3d-264">轉譯牽涉到填入命令清單的呼叫，接著就可以執行命令清單，而交換鏈中的下一個緩衝區則會呈現出來：</span><span class="sxs-lookup"><span data-stu-id="0db3d-264">Rendering involves a call to populate the command list, then the command list can be executed and the next buffer in the swap chain presented:</span></span>

-   <span data-ttu-id="0db3d-265">填入命令清單。</span><span class="sxs-lookup"><span data-stu-id="0db3d-265">Populate the command list.</span></span>
-   <span data-ttu-id="0db3d-266">執行命令清單： [**ID3D12CommandQueue：： ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-266">Execute the command list: [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>
-   <span data-ttu-id="0db3d-267">[**IDXGISwapChain1：:P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) 畫面格。</span><span class="sxs-lookup"><span data-stu-id="0db3d-267">[**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) the frame.</span></span>
-   <span data-ttu-id="0db3d-268">等候 GPU 完成。</span><span class="sxs-lookup"><span data-stu-id="0db3d-268">Wait on the GPU to finish.</span></span>


```cpp
void D3D12HelloTriangle::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    WaitForPreviousFrame();
}
```



### <a name="populatecommandlist"></a><span data-ttu-id="0db3d-269">PopulateCommandList () </span><span class="sxs-lookup"><span data-stu-id="0db3d-269">PopulateCommandList()</span></span>

<span data-ttu-id="0db3d-270">您必須先重設命令清單配置器和命令清單本身，才能重複使用它們。</span><span class="sxs-lookup"><span data-stu-id="0db3d-270">You must reset the command list allocator and the command list itself before you can reuse them.</span></span> <span data-ttu-id="0db3d-271">在更先進的案例中，每隔幾個畫面重設配置器可能是合理的。</span><span class="sxs-lookup"><span data-stu-id="0db3d-271">In more advanced scenarios it might make sense to reset the allocator every several frames.</span></span> <span data-ttu-id="0db3d-272">記憶體與無法在執行命令清單之後立即釋放的配置器相關聯。</span><span class="sxs-lookup"><span data-stu-id="0db3d-272">Memory is associated with the allocator that can't be released immediately after executing a command list.</span></span> <span data-ttu-id="0db3d-273">此範例示範如何在每個畫面格之後重設配置器。</span><span class="sxs-lookup"><span data-stu-id="0db3d-273">This example shows how to reset the allocator after every frame.</span></span>

<span data-ttu-id="0db3d-274">現在，請重複使用目前框架的命令清單。</span><span class="sxs-lookup"><span data-stu-id="0db3d-274">Now, reuse the command list for the current frame.</span></span> <span data-ttu-id="0db3d-275">將此區重新附加至命令清單 (必須在每次重設命令清單時，以及執行命令清單之前完成) ，指出資源將作為轉譯目標使用、記錄命令，然後指出當命令清單執行完成時，轉譯目標將用來呈現。</span><span class="sxs-lookup"><span data-stu-id="0db3d-275">Reattach the viewport to the command list (which must be done whenever a command list is reset, and before the command list is executed), indicate that the resource will be in use as a render target, record commands, and then indicate that the render target will be used to present when the command list is done executing.</span></span>

<span data-ttu-id="0db3d-276">填入命令清單會依序呼叫下列方法和進程：</span><span class="sxs-lookup"><span data-stu-id="0db3d-276">Populating command lists calls the following methods and processes in turn:</span></span>

-   <span data-ttu-id="0db3d-277">重設命令配置器和命令清單：</span><span class="sxs-lookup"><span data-stu-id="0db3d-277">Reset the command allocator, and command list:</span></span> <dl>

[<span data-ttu-id="0db3d-278">**ID3D12CommandAllocator：： Reset**</span><span class="sxs-lookup"><span data-stu-id="0db3d-278">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [<span data-ttu-id="0db3d-279">**ID3D12GraphicsCommandList：： Reset**</span><span class="sxs-lookup"><span data-stu-id="0db3d-279">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   <span data-ttu-id="0db3d-280">設定根簽章、視口和剪刀矩形：</span><span class="sxs-lookup"><span data-stu-id="0db3d-280">Set the root signature, viewport and scissors rectangles:</span></span> <dl>

[<span data-ttu-id="0db3d-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span><span class="sxs-lookup"><span data-stu-id="0db3d-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [<span data-ttu-id="0db3d-282">**ID3D12GraphicsCommandList::RSSetViewports**</span><span class="sxs-lookup"><span data-stu-id="0db3d-282">**ID3D12GraphicsCommandList::RSSetViewports**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [<span data-ttu-id="0db3d-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span><span class="sxs-lookup"><span data-stu-id="0db3d-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   <span data-ttu-id="0db3d-284">指出將會使用背景緩衝區做為呈現目標：</span><span class="sxs-lookup"><span data-stu-id="0db3d-284">Indicate that the back buffer is to be used as a render target:</span></span> <dl>

[<span data-ttu-id="0db3d-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="0db3d-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [<span data-ttu-id="0db3d-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="0db3d-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="0db3d-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span><span class="sxs-lookup"><span data-stu-id="0db3d-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   <span data-ttu-id="0db3d-288">錄製命令：</span><span class="sxs-lookup"><span data-stu-id="0db3d-288">Record the commands:</span></span><dl>

[<span data-ttu-id="0db3d-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="0db3d-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [<span data-ttu-id="0db3d-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span><span class="sxs-lookup"><span data-stu-id="0db3d-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [<span data-ttu-id="0db3d-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="0db3d-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [<span data-ttu-id="0db3d-292">**ID3D12GraphicsCommandList：:D rawInstanced**</span><span class="sxs-lookup"><span data-stu-id="0db3d-292">**ID3D12GraphicsCommandList::DrawInstanced**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   <span data-ttu-id="0db3d-293">指出現在會使用背景緩衝區來呈現： [**ID3D12GraphicsCommandList：： ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-293">Indicate the back buffer will now be used to present: [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>
-   <span data-ttu-id="0db3d-294">關閉命令清單： [**ID3D12GraphicsCommandList：： close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-294">Close the command list: [**ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span></span>


```cpp
void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
    m_commandList->ResourceBarrier(1, &barrier);

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
    m_commandList->ResourceBarrier(1, &barrier);

    ThrowIfFailed(m_commandList->Close());
}
```



### <a name="waitforpreviousframe"></a><span data-ttu-id="0db3d-295">WaitForPreviousFrame () </span><span class="sxs-lookup"><span data-stu-id="0db3d-295">WaitForPreviousFrame()</span></span>

<span data-ttu-id="0db3d-296">下列程式碼顯示過度簡化的使用方式。</span><span class="sxs-lookup"><span data-stu-id="0db3d-296">The following code shows an over-simplified use of fences.</span></span>

> [!Note]  
> <span data-ttu-id="0db3d-297">等候框架完成對大部分的應用程式而言太沒有效率。</span><span class="sxs-lookup"><span data-stu-id="0db3d-297">Waiting for a frame to complete is too inefficient for most apps.</span></span>

 

<span data-ttu-id="0db3d-298">下列 Api 和進程會依序呼叫：</span><span class="sxs-lookup"><span data-stu-id="0db3d-298">The following APIs and processes are called in order:</span></span>

-   [<span data-ttu-id="0db3d-299">**ID3D12CommandQueue：：信號**</span><span class="sxs-lookup"><span data-stu-id="0db3d-299">**ID3D12CommandQueue::Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [<span data-ttu-id="0db3d-300">**ID3D12Fence::GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="0db3d-300">**ID3D12Fence::GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [<span data-ttu-id="0db3d-301">**ID3D12Fence::SetEventOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="0db3d-301">**ID3D12Fence::SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   <span data-ttu-id="0db3d-302">等候事件。</span><span class="sxs-lookup"><span data-stu-id="0db3d-302">Wait for the event.</span></span>
-   <span data-ttu-id="0db3d-303">更新框架索引： [**IDXGISwapChain3：： GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)。</span><span class="sxs-lookup"><span data-stu-id="0db3d-303">Update the frame index: [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span></span>


```cpp
void D3D12HelloTriangle::WaitForPreviousFrame()
{
    // WAITING FOR THE FRAME TO COMPLETE BEFORE CONTINUING IS NOT BEST PRACTICE.
    // This is code implemented as such for simplicity. More advanced samples 
    // illustrate how to use fences for efficient resource usage.

    // Signal and increment the fence value.
    const UINT64 fence = m_fenceValue;
    ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fence));
    m_fenceValue++;

    // Wait until the previous frame is finished.
    if (m_fence->GetCompletedValue() < fence)
    {
        ThrowIfFailed(m_fence->SetEventOnCompletion(fence, m_fenceEvent));
        WaitForSingleObject(m_fenceEvent, INFINITE);
    }

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();
}
```



### <a name="ondestroy"></a><span data-ttu-id="0db3d-304">OnDestroy () </span><span class="sxs-lookup"><span data-stu-id="0db3d-304">OnDestroy()</span></span>

<span data-ttu-id="0db3d-305">完全關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="0db3d-305">Cleanly close down the app.</span></span>

-   <span data-ttu-id="0db3d-306">等候 GPU 完成。</span><span class="sxs-lookup"><span data-stu-id="0db3d-306">Wait for the GPU to finish.</span></span>
-   <span data-ttu-id="0db3d-307">關閉事件。</span><span class="sxs-lookup"><span data-stu-id="0db3d-307">Close the event.</span></span>


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="0db3d-308">相關主題</span><span class="sxs-lookup"><span data-stu-id="0db3d-308">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0db3d-309">瞭解 Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0db3d-309">Understanding Direct3D 12</span></span>](directx-12-getting-started.md)
</dt> <dt>

[<span data-ttu-id="0db3d-310">工作範例</span><span class="sxs-lookup"><span data-stu-id="0db3d-310">Working Samples</span></span>](working-samples.md)
</dt> </dl>

 

 
