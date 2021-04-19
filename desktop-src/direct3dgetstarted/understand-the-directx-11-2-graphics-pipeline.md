---
title: 瞭解 Direct3D 11 轉譯管線
description: 先前，您已瞭解如何建立可用於在使用 DirectX 裝置資源的工作中繪製的視窗。 現在，您將瞭解如何建立圖形管線，以及您可以將它連結到哪裡。
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50f9a387b2d44fe750abcf5a8856f75e6d0110e
ms.sourcegitcommit: 07b756a2f350efa5cfd5024a723ef392274ac3d9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/17/2021
ms.locfileid: "106989107"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a><span data-ttu-id="ecf50-104">瞭解 Direct3D 11 轉譯管線</span><span class="sxs-lookup"><span data-stu-id="ecf50-104">Understand the Direct3D 11 rendering pipeline</span></span>

<span data-ttu-id="ecf50-105">先前，您已瞭解如何建立可用於在使用 [DirectX 裝置資源的工作](work-with-dxgi.md)中繪製的視窗。</span><span class="sxs-lookup"><span data-stu-id="ecf50-105">Previously, you looked at how to create a window you can use for drawing in [Work with DirectX device resources](work-with-dxgi.md).</span></span> <span data-ttu-id="ecf50-106">現在，您將瞭解如何建立圖形管線，以及您可以將它連結到哪裡。</span><span class="sxs-lookup"><span data-stu-id="ecf50-106">Now, you learn how to build the graphics pipeline, and where you can hook into it.</span></span>

<span data-ttu-id="ecf50-107">您會回想一下，有兩個可定義圖形管線的 Direct3D 介面： [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2)，可提供 GPU 及其資源的虛擬標記法;和 [**>id3d11devicecoNtext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2)，代表管線的圖形處理。</span><span class="sxs-lookup"><span data-stu-id="ecf50-107">You'll recall that there are two Direct3D interfaces that define the graphics pipeline: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), which provides a virtual representation of the GPU and its resources; and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), which represents the graphics processing for the pipeline.</span></span> <span data-ttu-id="ecf50-108">一般來說，您會使用 **ID3D11Device** 的實例來設定和取得在場景中開始處理圖形所需的 GPU 資源，並且使用 **>id3d11devicecoNtext** 在圖形管線中的每個適當著色器階段處理這些資源。</span><span class="sxs-lookup"><span data-stu-id="ecf50-108">Typically, you use an instance of **ID3D11Device** to configure and obtain the GPU resources you need to start processing the graphics in a scene, and you use **ID3D11DeviceContext** to process those resources at each appropriate shader stage in the graphics pipeline.</span></span> <span data-ttu-id="ecf50-109">您通常不常呼叫 **ID3D11Device** 方法，也就是當您設定場景或裝置變更時。</span><span class="sxs-lookup"><span data-stu-id="ecf50-109">You usually call **ID3D11Device** methods infrequently—that is, only when you set up a scene or when the device changes.</span></span> <span data-ttu-id="ecf50-110">另一方面，您會在每次處理框架以顯示時呼叫 **>id3d11devicecoNtext** 。</span><span class="sxs-lookup"><span data-stu-id="ecf50-110">On the other hand, you'll call **ID3D11DeviceContext** every time you process a frame for display.</span></span>

<span data-ttu-id="ecf50-111">這個範例會建立並設定適合用來顯示簡單旋轉、頂點陰影 cube 的基本圖形管線。</span><span class="sxs-lookup"><span data-stu-id="ecf50-111">This example creates and configures a minimal graphics pipeline suitable for displaying a simple spinning, vertex-shaded cube.</span></span> <span data-ttu-id="ecf50-112">它會示範大約最小的一組需要顯示的資源。</span><span class="sxs-lookup"><span data-stu-id="ecf50-112">It demonstrates approximately the smallest set of resources necessary for display.</span></span> <span data-ttu-id="ecf50-113">當您閱讀這裡的資訊時，請注意指定範例的限制，您可能必須將它擴充以支援您想要轉譯的場景。</span><span class="sxs-lookup"><span data-stu-id="ecf50-113">As you read the info here, note the limitations of the given example where you may have to extend it to support the scene you want to render.</span></span>

<span data-ttu-id="ecf50-114">此範例涵蓋兩個適用于圖形的 c + + 類別：裝置資源管理員類別和3D 場景轉譯器類別。</span><span class="sxs-lookup"><span data-stu-id="ecf50-114">This example covers two C++ classes for graphics: a device resource manager class, and 3D scene renderer class.</span></span> <span data-ttu-id="ecf50-115">本主題特別著重于3D 場景轉譯器。</span><span class="sxs-lookup"><span data-stu-id="ecf50-115">This topic focuses specifically on the 3D scene renderer.</span></span>

## <a name="what-does-the-cube-renderer-do"></a><span data-ttu-id="ecf50-116">Cube 轉譯器的用途為何？</span><span class="sxs-lookup"><span data-stu-id="ecf50-116">What does the cube renderer do?</span></span>

<span data-ttu-id="ecf50-117">圖形管線是由3D 場景轉譯器類別所定義。</span><span class="sxs-lookup"><span data-stu-id="ecf50-117">The graphics pipeline is defined by the 3D scene renderer class.</span></span> <span data-ttu-id="ecf50-118">場景轉譯器能夠：</span><span class="sxs-lookup"><span data-stu-id="ecf50-118">The scene renderer is able to:</span></span>

-   <span data-ttu-id="ecf50-119">定義常數緩衝區來儲存統一的資料。</span><span class="sxs-lookup"><span data-stu-id="ecf50-119">Define constant buffers to store your uniform data.</span></span>
-   <span data-ttu-id="ecf50-120">定義頂點緩衝區以保存您的物件頂點資料，並定義對應的索引緩衝區，讓頂點著色器能夠正確地引導三角形。</span><span class="sxs-lookup"><span data-stu-id="ecf50-120">Define vertex buffers to hold your object vertex data, and corresponding index buffers to enable the vertex shader to walk the triangles correctly.</span></span>
-   <span data-ttu-id="ecf50-121">建立材質資源和資源檢視。</span><span class="sxs-lookup"><span data-stu-id="ecf50-121">Create texture resources and resource views.</span></span>
-   <span data-ttu-id="ecf50-122">載入著色器物件。</span><span class="sxs-lookup"><span data-stu-id="ecf50-122">Load your shader objects.</span></span>
-   <span data-ttu-id="ecf50-123">更新圖形資料以顯示每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="ecf50-123">Update the graphics data to display each frame.</span></span>
-   <span data-ttu-id="ecf50-124">轉譯 (繪製) 圖形至交換鏈。</span><span class="sxs-lookup"><span data-stu-id="ecf50-124">Render (draw) the graphics to the swap chain.</span></span>

<span data-ttu-id="ecf50-125">前四個處理常式通常會使用 [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) 介面方法來初始化和管理圖形資源，最後兩個程式使用 [**>id3d11devicecoNtext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) 介面方法來管理和執行圖形管線。</span><span class="sxs-lookup"><span data-stu-id="ecf50-125">The first four processes typically use the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) interface methods for initializing and managing graphics resources, and the last two use the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) interface methods to manage and execute the graphics pipeline.</span></span>

<span data-ttu-id="ecf50-126">系統會建立並管理轉譯 **器類別的** 實例，做為主要專案類別的成員變數。</span><span class="sxs-lookup"><span data-stu-id="ecf50-126">An instance of the **Renderer** class is created and managed as a member variable on the main project class.</span></span> <span data-ttu-id="ecf50-127">**DeviceResources** 實例是以共用指標的形式在數個類別之間進行管理，包括主要專案類別、**應用** 程式視圖提供者類別和轉譯 **器。**</span><span class="sxs-lookup"><span data-stu-id="ecf50-127">The **DeviceResources** instance is managed as a shared pointer across several classes, including the main project class, the **App** view-provider class, and **Renderer**.</span></span> <span data-ttu-id="ecf50-128">如果您將轉譯 **器取代為您自己的類別** ，請考慮將 **DeviceResources** 實例宣告和指派為共用指標成員：</span><span class="sxs-lookup"><span data-stu-id="ecf50-128">If you replace **Renderer** with your own class, consider declaring and assigning the **DeviceResources** instance as a shared pointer member as well:</span></span>

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

<span data-ttu-id="ecf50-129">您只需將指標傳遞至類別的函式 (或其他初始化方法，) 在 **應用程式** 類別的 **Initialize** 方法中建立 **DeviceResources** 實例之後。</span><span class="sxs-lookup"><span data-stu-id="ecf50-129">Just pass the pointer into the class constructor (or other initialization method) after the **DeviceResources** instance is created in the **Initialize** method of the **App** class.</span></span> <span data-ttu-id="ecf50-130">如果您想要讓主要類別完全擁有 **DeviceResources** 實例，也可以傳遞 **弱式 \_ ptr** 參考。</span><span class="sxs-lookup"><span data-stu-id="ecf50-130">You can also pass a **weak\_ptr** reference if, instead, you want your main class to completely own the **DeviceResources** instance.</span></span>

## <a name="create-the-cube-renderer"></a><span data-ttu-id="ecf50-131">建立 cube 轉譯器</span><span class="sxs-lookup"><span data-stu-id="ecf50-131">Create the cube renderer</span></span>

<span data-ttu-id="ecf50-132">在此範例中，我們使用下列方法來組織場景轉譯器類別：</span><span class="sxs-lookup"><span data-stu-id="ecf50-132">In this example, we organize the scene renderer class with the following methods:</span></span>

-   <span data-ttu-id="ecf50-133">**CreateDeviceDependentResources**：每當必須初始化或重新開機場景時呼叫。</span><span class="sxs-lookup"><span data-stu-id="ecf50-133">**CreateDeviceDependentResources**: Called whenever the scene must be initialized or restarted.</span></span> <span data-ttu-id="ecf50-134">這個方法會載入您的初始頂點資料、紋理、著色器和其他資源，並建立初始常數和頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ecf50-134">This method loads your initial vertex data, textures, shaders, and other resources, and constructs the initial constant and vertex buffers.</span></span> <span data-ttu-id="ecf50-135">一般來說，大部分的工作都是使用 [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) 方法來完成，而不是 [**>id3d11devicecoNtext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) 方法。</span><span class="sxs-lookup"><span data-stu-id="ecf50-135">Typically, most of the work here is done with [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) methods, not [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) methods.</span></span>
-   <span data-ttu-id="ecf50-136">**CreateWindowSizeDependentResources**：每當視窗狀態變更時呼叫，例如調整大小或方向變更時。</span><span class="sxs-lookup"><span data-stu-id="ecf50-136">**CreateWindowSizeDependentResources**: Called whenever the window state changes, such as when resizing occurs or when orientation changes.</span></span> <span data-ttu-id="ecf50-137">這個方法會重建轉換矩陣，例如相機的矩陣。</span><span class="sxs-lookup"><span data-stu-id="ecf50-137">This method rebuilds transform matrices, such as those for your camera.</span></span>
-   <span data-ttu-id="ecf50-138">**Update**：通常是從管理立即遊戲狀態的程式部分呼叫;在此範例中，我們只會從 **主要** 類別呼叫它。</span><span class="sxs-lookup"><span data-stu-id="ecf50-138">**Update**: Typically called from the part of the program that manages immediate game state; in this example, we just call it from the **Main** class.</span></span> <span data-ttu-id="ecf50-139">讓這個方法從任何影響轉譯的遊戲狀態資訊讀取，例如物件位置或動畫框架的更新，以及任何全域遊戲資料（例如淺色或遊戲物理的變更）。</span><span class="sxs-lookup"><span data-stu-id="ecf50-139">Have this method read from any game-state information that affects rendering, such as updates to object position or animation frames, plus any global game data like light levels or changes to game physics.</span></span> <span data-ttu-id="ecf50-140">這些輸入會用來更新每個框架的常數緩衝區和物件資料。</span><span class="sxs-lookup"><span data-stu-id="ecf50-140">These inputs are used to update the per-frame constant buffers and object data.</span></span>
-   <span data-ttu-id="ecf50-141">轉譯 **：通常** 是從管理遊戲迴圈的程式部分呼叫;在此情況下，它是從 **主要** 類別呼叫。</span><span class="sxs-lookup"><span data-stu-id="ecf50-141">**Render**: Typically called from the part of the program that manages the game loop; in this case, it's called from the **Main** class.</span></span> <span data-ttu-id="ecf50-142">這個方法會建立圖形管線：它會系結著色器、將緩衝區和資源系結至著色器階段，以及叫用目前框架的繪圖。</span><span class="sxs-lookup"><span data-stu-id="ecf50-142">This method constructs the graphics pipeline: it binds shaders, binds buffers and resources to shader stages, and invokes drawing for the current frame.</span></span>

<span data-ttu-id="ecf50-143">這些方法會組成行為的主體，以使用您的資產來呈現具有 Direct3D 的場景。</span><span class="sxs-lookup"><span data-stu-id="ecf50-143">These methods comprise the body of behaviors for rendering a scene with Direct3D using your assets.</span></span> <span data-ttu-id="ecf50-144">如果您使用新的轉譯類別來延伸此範例，請在主要專案類別上進行宣告。</span><span class="sxs-lookup"><span data-stu-id="ecf50-144">If you extend this example with a new rendering class, declare it on the main project class.</span></span> <span data-ttu-id="ecf50-145">這是：</span><span class="sxs-lookup"><span data-stu-id="ecf50-145">So this:</span></span>

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="ecf50-146">變成：</span><span class="sxs-lookup"><span data-stu-id="ecf50-146">becomes this:</span></span>

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="ecf50-147">同樣地，請注意，此範例假設在您的執行中，這些方法具有相同的簽章。</span><span class="sxs-lookup"><span data-stu-id="ecf50-147">Again, note that this example assumes that the methods have the same signatures in your implementation.</span></span> <span data-ttu-id="ecf50-148">如果簽章已變更，請檢查 **主要** 迴圈，並據以進行變更。</span><span class="sxs-lookup"><span data-stu-id="ecf50-148">If the signatures have changed, review the **Main** loop and make the changes accordingly.</span></span>

<span data-ttu-id="ecf50-149">讓我們更詳細地查看場景呈現方法。</span><span class="sxs-lookup"><span data-stu-id="ecf50-149">Let's take a look at scene-rendering methods in more detail.</span></span>

## <a name="create-device-dependent-resources"></a><span data-ttu-id="ecf50-150">建立裝置相依資源</span><span class="sxs-lookup"><span data-stu-id="ecf50-150">Create device dependent resources</span></span>

<span data-ttu-id="ecf50-151">**CreateDeviceDependentResources** 合併使用 [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) 呼叫來初始化場景及其資源的所有作業。</span><span class="sxs-lookup"><span data-stu-id="ecf50-151">**CreateDeviceDependentResources** consolidates all the operations for initializing the scene and its resources using [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) calls.</span></span> <span data-ttu-id="ecf50-152">這個方法會假設 Direct3D 裝置剛剛已初始化 (或已針對場景重新建立) 。</span><span class="sxs-lookup"><span data-stu-id="ecf50-152">This method assumes that the Direct3D device has just been initialized (or has been recreated) for a scene.</span></span> <span data-ttu-id="ecf50-153">它會重新建立或重載所有場景特定圖形資源，例如頂點和圖元著色器、物件的頂點和索引緩衝區，以及任何其他資源 (例如紋理及其對應的視圖) 。</span><span class="sxs-lookup"><span data-stu-id="ecf50-153">It recreates or reloads all scene-specific graphics resources, such as the vertex and pixel shaders, the vertex and index buffers for objects, and any other resources (for example, as textures and their corresponding views).</span></span>

<span data-ttu-id="ecf50-154">以下是 **CreateDeviceDependentResources** 的範例程式碼：</span><span class="sxs-lookup"><span data-stu-id="ecf50-154">Here's example code for **CreateDeviceDependentResources**:</span></span>


```C++
void Renderer::CreateDeviceDependentResources()
{
    // Compile shaders using the Effects library.
    auto CreateShadersTask = Concurrency::create_task(
            [this]( )
            {
                CreateShaders();
            }
        );

    // Load the geometry for the spinning cube.
    auto CreateCubeTask = CreateShadersTask.then(
            [this]()
            {
                CreateCube();
            }
        );
}

void Renderer::CreateWindowSizeDependentResources()
{
    // Create the view matrix and the perspective matrix.
    CreateViewAndPerspective();
}
```



<span data-ttu-id="ecf50-155">當您從磁片載入資源時（像是已編譯的著色器物件 (的資源）或) 檔案或紋理的資源，則會以非同步方式進行。</span><span class="sxs-lookup"><span data-stu-id="ecf50-155">Any time you load resources from disk—resources like compiled shader object (CSO, or .cso) files or textures—do so asynchronously.</span></span> <span data-ttu-id="ecf50-156">這可讓您繼續進行其他工作 (像是其他的設定工作) ，而且因為主要迴圈不會被封鎖，所以您可以持續顯示 (使用者的視覺效果，例如遊戲) 的載入動畫。</span><span class="sxs-lookup"><span data-stu-id="ecf50-156">This allows you to keep other work going at the same time (like other setup tasks), and because the main loop isn't blocked you can keep displaying something visually interesting to the user (like a loading animation for your game).</span></span> <span data-ttu-id="ecf50-157">此範例會使用從 Windows 8 開始提供的 Concurrency：： Tasks API。請注意用來封裝非同步載入工作的 lambda 語法。</span><span class="sxs-lookup"><span data-stu-id="ecf50-157">This example uses the Concurrency::Tasks API that is available starting in Windows 8; note the lambda syntax used to encapsulate asynchronous loading tasks.</span></span> <span data-ttu-id="ecf50-158">這些 lambda 代表稱為「非執行緒」的函式，因此會明確地捕捉 **此**)  (目前類別物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ecf50-158">These lambdas represent the functions called off-thread, so a pointer to the current class object (**this**) is explicitly captured.</span></span>

<span data-ttu-id="ecf50-159">以下是您可以如何載入著色器位元組程式碼的範例：</span><span class="sxs-lookup"><span data-stu-id="ecf50-159">Here's an example of how you can load shader bytecode:</span></span>


```C++
HRESULT hr = S_OK;

// Use the Direct3D device to load resources into graphics memory.
ID3D11Device* device = m_deviceResources->GetDevice();

// You'll need to use a file loader to load the shader bytecode. In this
// example, we just use the standard library.
FILE* vShader, * pShader;
BYTE* bytes;

size_t destSize = 4096;
size_t bytesRead = 0;
bytes = new BYTE[destSize];

fopen_s(&vShader, "CubeVertexShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, vShader);
hr = device->CreateVertexShader(
    bytes,
    bytesRead,
    nullptr,
    &m_pVertexShader
    );

D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );

delete bytes;


bytes = new BYTE[destSize];
bytesRead = 0;
fopen_s(&pShader, "CubePixelShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, pShader);
hr = device->CreatePixelShader(
    bytes,
    bytesRead,
    nullptr,
    m_pPixelShader.GetAddressOf()
    );

delete bytes;

CD3D11_BUFFER_DESC cbDesc(
    sizeof(ConstantBufferStruct),
    D3D11_BIND_CONSTANT_BUFFER
    );

hr = device->CreateBuffer(
    &cbDesc,
    nullptr,
    m_pConstantBuffer.GetAddressOf()
    );

fclose(vShader);
fclose(pShader);
```



<span data-ttu-id="ecf50-160">以下是如何建立頂點和索引緩衝區的範例：</span><span class="sxs-lookup"><span data-stu-id="ecf50-160">Here's an example of how to create vertex and index buffers:</span></span>


```C++
HRESULT Renderer::CreateCube()
{
    HRESULT hr = S_OK;

    // Use the Direct3D device to load resources into graphics memory.
    ID3D11Device* device = m_deviceResources->GetDevice();

    // Create cube geometry.
    VertexPositionColor CubeVertices[] =
    {
        {DirectX::XMFLOAT3(-0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  0,   0,   0),},
        {DirectX::XMFLOAT3(-0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  0,   0,   1),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  0,   1,   0),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  0,   1,   1),},

        {DirectX::XMFLOAT3( 0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  1,   0,   0),},
        {DirectX::XMFLOAT3( 0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  1,   0,   1),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  1,   1,   0),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  1,   1,   1),},
    };
    
    // Create vertex buffer:
    
    CD3D11_BUFFER_DESC vDesc(
        sizeof(CubeVertices),
        D3D11_BIND_VERTEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA vData;
    ZeroMemory(&vData, sizeof(D3D11_SUBRESOURCE_DATA));
    vData.pSysMem = CubeVertices;
    vData.SysMemPitch = 0;
    vData.SysMemSlicePitch = 0;

    hr = device->CreateBuffer(
        &vDesc,
        &vData,
        &m_pVertexBuffer
        );

    // Create index buffer:
    unsigned short CubeIndices [] = 
    {
        0,2,1, // -x
        1,2,3,

        4,5,6, // +x
        5,7,6,

        0,1,5, // -y
        0,5,4,

        2,6,7, // +y
        2,7,3,

        0,4,6, // -z
        0,6,2,

        1,3,7, // +z
        1,7,5,
    };

    m_indexCount = ARRAYSIZE(CubeIndices);

    CD3D11_BUFFER_DESC iDesc(
        sizeof(CubeIndices),
        D3D11_BIND_INDEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA iData;
    ZeroMemory(&iData, sizeof(D3D11_SUBRESOURCE_DATA));
    iData.pSysMem = CubeIndices;
    iData.SysMemPitch = 0;
    iData.SysMemSlicePitch = 0;
    
    hr = device->CreateBuffer(
        &iDesc,
        &iData,
        &m_pIndexBuffer
        );

    return hr;
}
```



<span data-ttu-id="ecf50-161">此範例不會載入任何網格或紋理。</span><span class="sxs-lookup"><span data-stu-id="ecf50-161">This example does not load any meshes or textures.</span></span> <span data-ttu-id="ecf50-162">您必須建立方法來載入遊戲專屬的網格和材質類型，並以非同步方式呼叫它們。</span><span class="sxs-lookup"><span data-stu-id="ecf50-162">You must create the methods for loading the mesh and texture types that are specific to your game, and call them asynchronously.</span></span>

<span data-ttu-id="ecf50-163">您也會在這裡填入個別場景常數緩衝區的初始值。</span><span class="sxs-lookup"><span data-stu-id="ecf50-163">Populate initial values for your per-scene constant buffers here, too.</span></span> <span data-ttu-id="ecf50-164">每場景常數緩衝區的範例包括固定光源或其他靜態場景元素和資料。</span><span class="sxs-lookup"><span data-stu-id="ecf50-164">Examples of per-scene constant buffer include fixed lights, or other static scene elements and data.</span></span>

## <a name="implement-the-createwindowsizedependentresources-method"></a><span data-ttu-id="ecf50-165">執行 CreateWindowSizeDependentResources 方法</span><span class="sxs-lookup"><span data-stu-id="ecf50-165">Implement the CreateWindowSizeDependentResources method</span></span>

<span data-ttu-id="ecf50-166">每次視窗大小、方向或解析度變更時，就會呼叫 **CreateWindowSizeDependentResources** 方法。</span><span class="sxs-lookup"><span data-stu-id="ecf50-166">**CreateWindowSizeDependentResources** methods are called every time the window size, orientation, or resolution changes.</span></span>

<span data-ttu-id="ecf50-167">視窗大小資源的更新方式如下：靜態訊息進程會取得數個可能事件的其中一個，表示視窗狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="ecf50-167">Window size resources are updated like so: The static message proc gets one of several possible events indicating a change in window state.</span></span> <span data-ttu-id="ecf50-168">然後會通知您的主要迴圈，並在主要類別實例上呼叫 **CreateWindowSizeDependentResources** ，然後在場景轉譯器類別上呼叫 **CreateWindowSizeDependentResources** 的實作為。</span><span class="sxs-lookup"><span data-stu-id="ecf50-168">Your main loop is then informed about the event and calls **CreateWindowSizeDependentResources** on the main class instance, which then calls the **CreateWindowSizeDependentResources** implementation on the scene renderer class.</span></span>

<span data-ttu-id="ecf50-169">此方法的主要工作是確定視覺效果不會因為視窗屬性變更而變得混淆或不正確。</span><span class="sxs-lookup"><span data-stu-id="ecf50-169">The primary job of this method is to make sure the visuals don't become confused or invalid because of a change in window properties.</span></span> <span data-ttu-id="ecf50-170">在此範例中，我們會使用新的 view 欄位來更新專案矩陣 (FOV) 適用于調整大小或方向視窗。</span><span class="sxs-lookup"><span data-stu-id="ecf50-170">In this example, we update the project matrices with a new field of view (FOV) for the resized or reoriented window.</span></span>

<span data-ttu-id="ecf50-171">我們已在 **DeviceResources** 中看到用來建立視窗資源的程式碼，也就是與背景緩衝區) 和轉譯目標視圖 (的交換鏈。</span><span class="sxs-lookup"><span data-stu-id="ecf50-171">We already saw the code for creating window resources in **DeviceResources** - that was the swap chain (with back buffer) and render target view.</span></span> <span data-ttu-id="ecf50-172">以下是轉譯器如何建立外觀比例相依的轉換：</span><span class="sxs-lookup"><span data-stu-id="ecf50-172">Here's how the renderer creates aspect ratio-dependent transforms:</span></span>


```C++
void Renderer::CreateViewAndPerspective()
{
    // Use DirectXMath to create view and perspective matrices.

    DirectX::XMVECTOR eye = DirectX::XMVectorSet(0.0f, 0.7f, 1.5f, 0.f);
    DirectX::XMVECTOR at  = DirectX::XMVectorSet(0.0f,-0.1f, 0.0f, 0.f);
    DirectX::XMVECTOR up  = DirectX::XMVectorSet(0.0f, 1.0f, 0.0f, 0.f);

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.view,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixLookAtRH(
                eye,
                at,
                up
                )
            )
        );

    float aspectRatioX = m_deviceResources->GetAspectRatio();
    float aspectRatioY = aspectRatioX < (16.0f / 9.0f) ? aspectRatioX / (16.0f / 9.0f) : 1.0f;

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.projection,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixPerspectiveFovRH(
                2.0f * std::atan(std::tan(DirectX::XMConvertToRadians(70) * 0.5f) / aspectRatioY),
                aspectRatioX,
                0.01f,
                100.0f
                )
            )
        );
}
```



<span data-ttu-id="ecf50-173">如果您的場景具有相依于外觀比例之元件的特定版面配置，則這是重新排列它們以符合該外觀比例的位置。</span><span class="sxs-lookup"><span data-stu-id="ecf50-173">If your scene has a specific layout of components that depends on the aspect ratio, this is the place to rearrange them to match that aspect ratio.</span></span> <span data-ttu-id="ecf50-174">您也可能想要在這裡變更後續處理行為的設定。</span><span class="sxs-lookup"><span data-stu-id="ecf50-174">You may want to change the configuration of post-processing behavior here also.</span></span>

## <a name="implement-the-update-method"></a><span data-ttu-id="ecf50-175">執行 Update 方法</span><span class="sxs-lookup"><span data-stu-id="ecf50-175">Implement the Update method</span></span>

<span data-ttu-id="ecf50-176">每個遊戲迴圈都會呼叫一次 **Update** 方法，在此範例中，會由相同名稱的主要類別方法來呼叫。</span><span class="sxs-lookup"><span data-stu-id="ecf50-176">The **Update** method is called once per game loop - in this example, it is called by the main class's method of the same name.</span></span> <span data-ttu-id="ecf50-177">它有一個簡單的用途：根據上一個畫面格的經過時間 (或經過時間步驟) 來更新場景幾何和遊戲狀態。</span><span class="sxs-lookup"><span data-stu-id="ecf50-177">It has a simple purpose: update scene geometry and game state based on the amount of elapsed time (or elapsed time steps) since the previous frame.</span></span> <span data-ttu-id="ecf50-178">在此範例中，我們只會針對每個畫面格旋轉一次 cube。</span><span class="sxs-lookup"><span data-stu-id="ecf50-178">In this example, we simply rotate the cube once per frame.</span></span> <span data-ttu-id="ecf50-179">在實際的遊戲場景中，這個方法會包含更多的程式碼來檢查遊戲狀態、更新每個畫面格 (或其他動態) 常數緩衝區、幾何緩衝區和其他記憶體中的資產。</span><span class="sxs-lookup"><span data-stu-id="ecf50-179">In a real game scene, this method contains a lot more code for checking game state, updating per-frame (or other dynamic) constant buffers, geometry buffers, and other in-memory assets accordingly.</span></span> <span data-ttu-id="ecf50-180">由於 CPU 與 GPU 之間的通訊會產生額外負荷，因此請確定您只會更新自最後一個畫面格之後實際變更的緩衝區-您可以視需要將常數緩衝區分組或分割，使其更有效率。</span><span class="sxs-lookup"><span data-stu-id="ecf50-180">Since communication between the CPU and GPU incurs overhead, make sure you only update buffers that have actually changed since the last frame - your constant buffers can be grouped, or split up, as needed to make this more efficient.</span></span>


```C++
void Renderer::Update()
{
    // Rotate the cube 1 degree per frame.
    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.world,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixRotationY(
                DirectX::XMConvertToRadians(
                    (float) m_frameCount++
                    )
                )
            )
        );

    if (m_frameCount == MAXUINT)  m_frameCount = 0;
}
```



<span data-ttu-id="ecf50-181">在此情況下， **旋轉** 會使用 cube 的新轉換矩陣來更新常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ecf50-181">In this case, **Rotate** updates the constant buffer with a new transformation matrix for the cube.</span></span> <span data-ttu-id="ecf50-182">在頂點著色器階段，矩陣將會乘以每個頂點。</span><span class="sxs-lookup"><span data-stu-id="ecf50-182">The matrix will be multiplied per-vertex during the vertex shader stage.</span></span> <span data-ttu-id="ecf50-183">由於每個框架都會呼叫這個方法，因此，這是匯總任何更新您的動態常數和頂點緩衝區之方法的理想位置，或執行任何其他作業來準備場景中的物件，以供圖形管線進行轉換。</span><span class="sxs-lookup"><span data-stu-id="ecf50-183">Since this method is called with every frame, this is a good place to aggregate any methods that update your dynamic constant and vertex buffers, or to perform any other operations that prepare the objects in the scene for transformation by the graphics pipeline.</span></span>

## <a name="implement-the-render-method"></a><span data-ttu-id="ecf50-184">執行 Render 方法</span><span class="sxs-lookup"><span data-stu-id="ecf50-184">Implement the Render method</span></span>

<span data-ttu-id="ecf50-185">呼叫 **Update** 之後，每個遊戲迴圈都會呼叫這個方法一次。</span><span class="sxs-lookup"><span data-stu-id="ecf50-185">This method is called once per game loop after calling **Update**.</span></span> <span data-ttu-id="ecf50-186">如同 **更新** 一樣，也會從主要類別呼叫 **Render** 方法。</span><span class="sxs-lookup"><span data-stu-id="ecf50-186">Like **Update**, the **Render** method is also called from the main class.</span></span> <span data-ttu-id="ecf50-187">這是使用 [**>id3d11devicecoNtext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) 實例上的方法為框架建立和處理圖形管線的方法。</span><span class="sxs-lookup"><span data-stu-id="ecf50-187">This is the method where the graphics pipeline is constructed and processed for the frame using methods on the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) instance.</span></span> <span data-ttu-id="ecf50-188">這最後在 [**>id3d11devicecoNtext：:D rawindexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed)的最後呼叫中。</span><span class="sxs-lookup"><span data-stu-id="ecf50-188">This culminates in a final call to [**ID3D11DeviceContext::DrawIndexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span></span> <span data-ttu-id="ecf50-189">請務必瞭解，此呼叫 (或其他類似的 **繪圖 \* *_ 呼叫（在 _ >id3d11devicecoNtext 上定義*** ）) 實際執行管線。</span><span class="sxs-lookup"><span data-stu-id="ecf50-189">It’s important to understand that this call (or other similar \**Draw\**_ calls defined on _\* ID3D11DeviceContext\*\*) actually executes the pipeline.</span></span> <span data-ttu-id="ecf50-190">具體而言，這是當 Direct3D 與 GPU 通訊以設定繪製狀態、執行每個管線階段，以及將圖元結果寫入轉譯目標緩衝區資源以供交換鏈顯示時。</span><span class="sxs-lookup"><span data-stu-id="ecf50-190">Specifically, this is when Direct3D communicates with the GPU to set drawing state, runs each pipeline stage, and writes the pixel results into the render-target buffer resource for display by the swap chain.</span></span> <span data-ttu-id="ecf50-191">由於 CPU 與 GPU 之間的通訊會產生額外負荷，因此，如果您可以的話，請將多個繪製呼叫合併成一個單一呼叫，尤其是當您的場景有許多轉譯的物件時。</span><span class="sxs-lookup"><span data-stu-id="ecf50-191">Since communication between the CPU and GPU incurs overhead, combine multiple draw calls into a single one if you can, especially if your scene has a lot of rendered objects.</span></span>


```C++
void Renderer::Render()
{
    // Use the Direct3D device context to draw.
    ID3D11DeviceContext* context = m_deviceResources->GetDeviceContext();

    ID3D11RenderTargetView* renderTarget = m_deviceResources->GetRenderTarget();
    ID3D11DepthStencilView* depthStencil = m_deviceResources->GetDepthStencil();

    context->UpdateSubresource(
        m_pConstantBuffer.Get(),
        0,
        nullptr,
        &m_constantBufferData,
        0,
        0
        );

    // Clear the render target and the z-buffer.
    const float teal [] = { 0.098f, 0.439f, 0.439f, 1.000f };
    context->ClearRenderTargetView(
        renderTarget,
        teal
        );
    context->ClearDepthStencilView(
        depthStencil,
        D3D11_CLEAR_DEPTH | D3D11_CLEAR_STENCIL,
        1.0f,
        0);

    // Set the render target.
    context->OMSetRenderTargets(
        1,
        &renderTarget,
        depthStencil
        );

    // Set up the IA stage by setting the input topology and layout.
    UINT stride = sizeof(VertexPositionColor);
    UINT offset = 0;

    context->IASetVertexBuffers(
        0,
        1,
        m_pVertexBuffer.GetAddressOf(),
        &stride,
        &offset
        );

    context->IASetIndexBuffer(
        m_pIndexBuffer.Get(),
        DXGI_FORMAT_R16_UINT,
        0
        );
    
    context->IASetPrimitiveTopology(
        D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST
        );

    context->IASetInputLayout(m_pInputLayout.Get());

    // Set up the vertex shader stage.
    context->VSSetShader(
        m_pVertexShader.Get(),
        nullptr,
        0
        );

    context->VSSetConstantBuffers(
        0,
        1,
        m_pConstantBuffer.GetAddressOf()
        );

    // Set up the pixel shader stage.
    context->PSSetShader(
        m_pPixelShader.Get(),
        nullptr,
        0
        );

    // Calling Draw tells Direct3D to start sending commands to the graphics device.
    context->DrawIndexed(
        m_indexCount,
        0,
        0
        );
}
```



<span data-ttu-id="ecf50-192">最好依序在內容上設定各種圖形管線階段。</span><span class="sxs-lookup"><span data-stu-id="ecf50-192">It's good practice to set the various graphics pipeline stages on the context in order.</span></span> <span data-ttu-id="ecf50-193">通常，順序為：</span><span class="sxs-lookup"><span data-stu-id="ecf50-193">Typically, the order is:</span></span>

-   <span data-ttu-id="ecf50-194">視需要使用新的資料重新整理常數緩衝區資源 (使用 **更新**) 的資料。</span><span class="sxs-lookup"><span data-stu-id="ecf50-194">Refresh constant buffer resources with new data as needed (using data from **Update**).</span></span>
-   <span data-ttu-id="ecf50-195">輸入元件 (IA) ：這是我們附加定義場景幾何之頂點和索引緩衝區的位置。</span><span class="sxs-lookup"><span data-stu-id="ecf50-195">Input assembly (IA): This is where we attach the vertex and index buffers that define the scene geometry.</span></span> <span data-ttu-id="ecf50-196">您必須為場景中的每個物件附加每個頂點和索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ecf50-196">You need to attach each vertex and index buffer for each object in the scene.</span></span> <span data-ttu-id="ecf50-197">因為這個範例只會有 cube，所以相當簡單。</span><span class="sxs-lookup"><span data-stu-id="ecf50-197">Because this example has just the cube, it's pretty simple.</span></span>
-   <span data-ttu-id="ecf50-198">頂點著色器 (VS) ：附加任何會轉換頂點緩衝區中資料的頂點著色器，並附加頂點著色器的常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ecf50-198">Vertex shader (VS): Attach any vertex shaders that will transform the data in the vertex buffers, and attach constant buffers for the vertex shader.</span></span>
-   <span data-ttu-id="ecf50-199">圖元著色器 (PS) ：連接會在點陣場景中執行每圖元作業的任何圖元著色器，並附加圖元著色器的裝置資源 (常數緩衝區、材質等) 。</span><span class="sxs-lookup"><span data-stu-id="ecf50-199">Pixel shader (PS): Attach any pixel shaders that will perform per-pixel operations in the rasterized scene, and attach device resources for the pixel shader (constant buffers, textures, and so on).</span></span>
-   <span data-ttu-id="ecf50-200">輸出合併 (OM) ：這是在著色器完成之後，混合圖元的階段。</span><span class="sxs-lookup"><span data-stu-id="ecf50-200">Output merger (OM): This is the stage where pixels are blended, after the shaders are finished.</span></span> <span data-ttu-id="ecf50-201">這是規則的例外狀況，因為您在設定任何其他階段之前，會先連接深度樣板並轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="ecf50-201">This is an exception to the rule, because you attach your depth stencils and render targets before setting any of the other stages.</span></span> <span data-ttu-id="ecf50-202">如果您有產生紋理的額外頂點和圖元著色器，例如陰影地圖、高度地圖或其他取樣技術，您可能會有多個樣板和目標-在此情況下，每個繪圖階段都必須先) 設定適當的目標 (，才能呼叫 draw 函數。</span><span class="sxs-lookup"><span data-stu-id="ecf50-202">You may have multiple stencils and targets if you have additional vertex and pixel shaders that generate textures such as shadow maps, height maps, or other sampling techniques - in this case, each drawing pass will need the appropriate target(s) set before you call a draw function.</span></span>

<span data-ttu-id="ecf50-203">接下來，在最後一節中 (使用 [著色器和著色器資源](work-with-shaders-and-shader-resources.md)) ，我們將探討著色器，並討論 Direct3D 如何執行這些著色器。</span><span class="sxs-lookup"><span data-stu-id="ecf50-203">Next, in the final section ([Work with shaders and shader resources](work-with-shaders-and-shader-resources.md)), we'll look at the shaders and discuss how Direct3D executes them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ecf50-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="ecf50-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ecf50-205">**接下來**</span><span class="sxs-lookup"><span data-stu-id="ecf50-205">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="ecf50-206">使用著色器和著色器資源</span><span class="sxs-lookup"><span data-stu-id="ecf50-206">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
