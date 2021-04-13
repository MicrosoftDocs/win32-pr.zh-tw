---
title: Direct3D 11 核心介面
description: 本節包含核心介面的相關資訊。
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- 介面，Direct3D 11 核心
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104463849"
---
# <a name="direct3d-11-core-interfaces"></a><span data-ttu-id="8a1a9-104">Direct3D 11 核心介面</span><span class="sxs-lookup"><span data-stu-id="8a1a9-104">Direct3D 11 core interfaces</span></span>

<span data-ttu-id="8a1a9-105">本節包含核心介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-105">This section contains information about the core interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8a1a9-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="8a1a9-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8a1a9-107">主題</span><span class="sxs-lookup"><span data-stu-id="8a1a9-107">Topic</span></span></th>
<th><span data-ttu-id="8a1a9-108">描述</span><span class="sxs-lookup"><span data-stu-id="8a1a9-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8a1a9-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-110">此介面會封裝以非同步方式從 GPU 取得資料的方法。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-110">This interface encapsulates methods for retrieving data from the GPU asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-112">Blend 介面會保存您可以系結至 <a href="d3d10-graphics-programming-guide-output-merger-stage.md">輸出合併階段</a>之混合狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-112">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-114">Blend 介面會保存您可以系結至 <a href="d3d10-graphics-programming-guide-output-merger-stage.md">輸出合併階段</a>之混合狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-114">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span> <span data-ttu-id="8a1a9-115">這個 blend 狀態介面支援邏輯作業以及混合作業。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-115">This blend-state interface supports logical operations as well as blending operations.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-117"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a>介面會封裝要播放之圖形命令的清單。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-117">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> interface encapsulates a list of graphics commands for play back.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-119">此介面會封裝用來測量 GPU 效能的方法。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-119">This interface encapsulates methods for measuring GPU performance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-121">深度樣板狀態介面會保存深度範本狀態的描述，您可以將其系結至 <a href="d3d10-graphics-programming-guide-output-merger-stage.md">輸出合併階段</a>。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-121">The depth-stencil-state interface holds a description for depth-stencil state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-123">裝置介面代表虛擬配接器;它是用來建立資源。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-123">The device interface represents a virtual adapter; it is used to create resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-125">裝置介面代表虛擬配接器;它是用來建立資源。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-125">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="8a1a9-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>中的方法。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-128">裝置介面代表虛擬配接器;它是用來建立資源。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-128">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="8a1a9-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>中的方法。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-131">裝置介面代表虛擬配接器;它是用來建立資源。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-131">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="8a1a9-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>中的方法。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-134">裝置介面代表虛擬配接器;它是用來建立資源。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-134">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="8a1a9-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>中的方法，例如 <strong>RegisterDeviceRemovedEvent</strong> 和 <strong>UnregisterDeviceRemoved</strong>。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, such as <strong>RegisterDeviceRemovedEvent</strong> and <strong>UnregisterDeviceRemoved</strong>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-137">裝置介面代表虛擬配接器;它是用來建立資源。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-137">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="8a1a9-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>中的方法。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-140">裝置子系介面可存取裝置所使用的資料。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-140">A device-child interface accesses data used by a device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-142"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>>id3d11devicecoNtext</strong></a>介面表示產生轉譯命令的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-142">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> interface represents a device context which generates rendering commands.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8a1a9-143">此介面的最新版本 <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceCoNtext4</strong></a> 引進 Windows 10 Creators Update 中。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-143">The latest version of this interface is <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduced in the Windows 10 Creators Update.</span></span> <span data-ttu-id="8a1a9-144">瞄準 Windows 10 Creators Update 的應用程式應該使用 <strong>ID3D11DeviceCoNtext4</strong> 介面，而不是 <strong>ID3D11Device</strong>。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-144">Applications targetting Windows 10 Creators Update should use the <strong>ID3D11DeviceContext4</strong> interface instead of <strong>ID3D11Device</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-146">裝置內容介面代表裝置內容;它是用來呈現命令。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-146">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="8a1a9-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceCoNtext1</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>>id3d11devicecoNtext</strong></a>中的方法。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-149">裝置內容介面代表裝置內容;它是用來呈現命令。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-149">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="8a1a9-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceCoNtext2</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceCoNtext1</strong></a>中的方法。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceCoNtext3</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-152">裝置內容介面代表裝置內容;它是用來呈現命令。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-152">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="8a1a9-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceCoNtext3</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceCoNtext2</strong></a>中的方法。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceCoNtext4</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-155">裝置內容介面代表裝置內容;它是用來呈現命令。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-155">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="8a1a9-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceCoNtext4</strong></a> 會將新方法新增至 <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceCoNtext3</strong></a>中的方法。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceCoNtextState</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-158"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceCoNtextState</strong></a>介面代表內容狀態物件，其保存有關 Microsoft Direct3D 裝置的狀態和行為資訊。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-158">The <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> interface represents a context state object, which holds state and behavior information about a Microsoft Direct3D device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-160">代表用來同步處理 CPU 的物件，以及一或多個 Gpu。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-160">Represents a fence, an object used for synchronization of the CPU and one or more GPUs.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-162">輸入配置介面會保存如何將在記憶體中配置的頂點資料摘要至<a href="overviews-direct3d-11-graphics-pipeline.md">圖形管線</a>的<a href="d3d10-graphics-programming-guide-input-assembler-stage.md">輸入組合語言階段</a>的定義。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-162">An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">input-assembler stage</a> of the <a href="overviews-direct3d-11-graphics-pipeline.md">graphics pipeline</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-164">為多執行緒應用程式的重要區段提供執行緒保護。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-164">Provides threading protection for critical sections of a multi-threaded application.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-166">述詞介面會根據上一次繪製呼叫的結果，判斷是否應該處理幾何。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-166">A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-168">查詢介面會從 GPU 查詢資訊。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-168">A query interface queries information from the GPU.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-170">表示查詢物件，用來從圖形處理器 (GPU) 查詢資訊。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-170">Represents a query object for querying information from the graphics processing unit (GPU).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-172">轉譯器狀態介面會保存您可以系結至轉譯器 <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">階段</a>的轉譯器狀態原因。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-172">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-174">轉譯器狀態介面會保存您可以系結至轉譯器 <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">階段</a>的轉譯器狀態原因。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-174">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="8a1a9-175">此轉譯器狀態介面支援強制取樣計數。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-175">This rasterizer-state interface supports forced sample count.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8a1a9-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-177">轉譯器狀態介面會保存您可以系結至轉譯器 <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">階段</a>的轉譯器狀態原因。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-177">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="8a1a9-178">此轉譯器狀態介面支援強制取樣計數和保守的點陣化模式。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-178">This rasterizer-state interface supports forced sample count and conservative rasterization mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8a1a9-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="8a1a9-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="8a1a9-180">取樣器狀態介面會保存取樣器狀態的描述，您可以系結至 <a href="overviews-direct3d-11-graphics-pipeline.md">管線</a> 的任何著色器階段，以供材質範例作業參考。</span><span class="sxs-lookup"><span data-stu-id="8a1a9-180">The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> for reference by texture sample operations.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8a1a9-181">Direct3D 11 的執行介面：</span><span class="sxs-lookup"><span data-stu-id="8a1a9-181">Direct3D 11 implements interfaces for:</span></span>

-   [<span data-ttu-id="8a1a9-182">資源</span><span class="sxs-lookup"><span data-stu-id="8a1a9-182">Resources</span></span>](d3d11-graphics-reference-resource-interfaces.md)
-   [<span data-ttu-id="8a1a9-183">著色器</span><span class="sxs-lookup"><span data-stu-id="8a1a9-183">Shaders</span></span>](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="8a1a9-184">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a1a9-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a1a9-185">核心參考</span><span class="sxs-lookup"><span data-stu-id="8a1a9-185">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

