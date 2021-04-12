---
description: 使用 USB DV Video 裝置
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: 使用 USB DV Video 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75647aa7b53bac45c155b4e0a9283418c9af58b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191743"
---
# <a name="working-with-usb-dv-video-devices"></a><span data-ttu-id="668f1-103">使用 USB DV Video 裝置</span><span class="sxs-lookup"><span data-stu-id="668f1-103">Working with USB DV Video Devices</span></span>

<span data-ttu-id="668f1-104">本主題說明如何針對可捕獲 DV 影片的通用序列匯流排 (USB) 影片裝置，撰寫應用程式。</span><span class="sxs-lookup"><span data-stu-id="668f1-104">This topic describes how to write applications for Universal Serial Bus (USB) video devices that capture DV video.</span></span>

<span data-ttu-id="668f1-105">標準 DV 格式的資料速率大約是每秒 25 mb (Mbps) 。</span><span class="sxs-lookup"><span data-stu-id="668f1-105">Standard DV format has a data rate of about 25 megabits per second (Mbps).</span></span> <span data-ttu-id="668f1-106">第一次引進 USB 時，沒有足夠的頻寬可支援 DV 影片。</span><span class="sxs-lookup"><span data-stu-id="668f1-106">When USB was first introduced, it did not have enough bandwidth to support DV video.</span></span> <span data-ttu-id="668f1-107">不過，USB 2.0 最多可支援 480 Mbps，而這對 DV 影片而言就已足夠。</span><span class="sxs-lookup"><span data-stu-id="668f1-107">However, USB 2.0 can support up to 480 Mbps, which is more than sufficient for DV video.</span></span> <span data-ttu-id="668f1-108">USB Video 裝置類別 (UVC) 規格（在2003中發行）會定義 USB DV 影片裝置的裝載格式。</span><span class="sxs-lookup"><span data-stu-id="668f1-108">The USB Video Device Class (UVC) specification, released in 2003, defines the payload format for USB DV video devices.</span></span> <span data-ttu-id="668f1-109">在 Windows XP Service Pack 2 中引進了 Windows Driver Model 的 UVC 裝置 (WDM) 類別驅動程式。</span><span class="sxs-lookup"><span data-stu-id="668f1-109">A Windows Driver Model (WDM) class driver for UVC devices was introduced in Windows XP Service Pack 2.</span></span>

<span data-ttu-id="668f1-110">在大部分的情況下，UVC 驅動程式支援的程式設計模型與適用于 IEEE 1394 裝置的 MSDV 驅動程式相同。</span><span class="sxs-lookup"><span data-stu-id="668f1-110">In most respects, the UVC driver supports the same programming model as the MSDV driver for IEEE 1394 devices.</span></span> <span data-ttu-id="668f1-111">針對 MSDV 撰寫的應用程式應該只需要稍微修改才能支援 UVC 裝置。</span><span class="sxs-lookup"><span data-stu-id="668f1-111">Applications written for MSDV should require only minor modifications to support UVC devices.</span></span>

<span data-ttu-id="668f1-112">UVC 驅動程式的運作方式與下欄區域中的 MSDV 驅動程式不同：</span><span class="sxs-lookup"><span data-stu-id="668f1-112">The UVC driver behaves differently from the MSDV driver in the following areas:</span></span>

-   [<span data-ttu-id="668f1-113">裝置模式</span><span class="sxs-lookup"><span data-stu-id="668f1-113">Device Mode</span></span>](device-mode.md)
-   [<span data-ttu-id="668f1-114">資料流程格式</span><span class="sxs-lookup"><span data-stu-id="668f1-114">Stream Format</span></span>](stream-format.md)
-   [<span data-ttu-id="668f1-115">信號格式</span><span class="sxs-lookup"><span data-stu-id="668f1-115">Signal Format</span></span>](signal-format.md)
-   [<span data-ttu-id="668f1-116">磁帶位置搜尋</span><span class="sxs-lookup"><span data-stu-id="668f1-116">Tape Location Search</span></span>](tape-location-search.md)
-   <span data-ttu-id="668f1-117">[從檔案傳輸 DV 至磁帶](transmit-dv-from-file-to-tape.md)。</span><span class="sxs-lookup"><span data-stu-id="668f1-117">[Transmit DV from File to Tape](transmit-dv-from-file-to-tape.md).</span></span>

<span data-ttu-id="668f1-118">若要判斷正在使用的驅動程式，請呼叫 [**IAMExtDevice：： get \_ DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport)。</span><span class="sxs-lookup"><span data-stu-id="668f1-118">To determine which driver is being used, call [**IAMExtDevice::get\_DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span></span> <span data-ttu-id="668f1-119">MSDV 驅動程式會傳回 DEV \_ port \_ 1394 旗標，而 UVC 驅動程式會傳回 dev \_ port \_ USB 旗標。</span><span class="sxs-lookup"><span data-stu-id="668f1-119">The MSDV driver returns the DEV\_PORT\_1394 flag, and the UVC driver returns the DEV\_PORT\_USB flag.</span></span>

<span data-ttu-id="668f1-120">**裝置節點**</span><span class="sxs-lookup"><span data-stu-id="668f1-120">**Device Nodes**</span></span>

<span data-ttu-id="668f1-121">在 USB 術語中，端點是指資料進入或離開裝置的點。</span><span class="sxs-lookup"><span data-stu-id="668f1-121">In USB terminology, endpoints are the points where data enters or leaves the device.</span></span> <span data-ttu-id="668f1-122">端點具有資料流程的方向，也就是從裝置到主機的輸入 (，) 或從主機到裝置) 的輸出 (。</span><span class="sxs-lookup"><span data-stu-id="668f1-122">An endpoint has a direction of data flow, either input (from device to host) or output (from host to device).</span></span> <span data-ttu-id="668f1-123">這可能有助於將這些指示視為相對於主機。</span><span class="sxs-lookup"><span data-stu-id="668f1-123">It may help to think of these directions as being relative to the host.</span></span> <span data-ttu-id="668f1-124">輸入進入主機;輸出來自主機。</span><span class="sxs-lookup"><span data-stu-id="668f1-124">Input goes to the host; output comes from the host.</span></span> <span data-ttu-id="668f1-125">下圖說明這兩個端點。</span><span class="sxs-lookup"><span data-stu-id="668f1-125">The following diagram illustrates the two endpoints.</span></span>

![usb 端點](images/ksnodes01.png)

<span data-ttu-id="668f1-127">在 UVC 裝置中，裝置的函式會以邏輯方式分成稱為單位和終端機的元件。</span><span class="sxs-lookup"><span data-stu-id="668f1-127">In a UVC device, the functions of the device are logically divided into components called units and terminals.</span></span> <span data-ttu-id="668f1-128">單位會接收一或多個資料流程做為輸入，並只傳遞一個資料流程作為輸出。</span><span class="sxs-lookup"><span data-stu-id="668f1-128">A unit receives one or more data streams as input and delivers exactly one stream as output.</span></span> <span data-ttu-id="668f1-129">終端機是資料流程的起點或結束點。</span><span class="sxs-lookup"><span data-stu-id="668f1-129">A terminal is the starting point or ending point for a data stream.</span></span> <span data-ttu-id="668f1-130">USB 端點對應到終端機，但方向相反：輸入端點是以輸出終端機表示，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="668f1-130">USB endpoints correspond to terminals, but the directions are reversed: an input endpoint is represented by an output terminal, and vice versa.</span></span> <span data-ttu-id="668f1-131">下圖顯示終端機和端點之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="668f1-131">The following diagram shows the relation between terminals and endpoints.</span></span>

![uvc 單位和終端機](images/ksnodes02.png)

<span data-ttu-id="668f1-133">此外，並非每個終端機都對應至 USB 端點。</span><span class="sxs-lookup"><span data-stu-id="668f1-133">Also, not every terminal corresponds to a USB endpoint.</span></span> <span data-ttu-id="668f1-134">「端點」（endpoint）專用於 USB 連線，而裝置可透過非 USB 連接傳送或接收資料。</span><span class="sxs-lookup"><span data-stu-id="668f1-134">The term endpoint refers specifically to USB connections, and a device may send or receive data through non-USB connections.</span></span> <span data-ttu-id="668f1-135">例如，攝影機是輸入終端機，而 LCD 畫面則是輸出終端機。</span><span class="sxs-lookup"><span data-stu-id="668f1-135">For example, a video camera is an input terminal and an LCD screen is an output terminal.</span></span>

<span data-ttu-id="668f1-136">在「KS Proxy」篩選中，單位和終端機會表示為篩選內的節點。</span><span class="sxs-lookup"><span data-stu-id="668f1-136">In the KS Proxy filter, units and terminals are represented as nodes inside the filter.</span></span> <span data-ttu-id="668f1-137">因為非 USB 裝置也可以有節點，所以「詞彙」這一詞的一般比「詞彙單位」和「終端機」更為普遍。</span><span class="sxs-lookup"><span data-stu-id="668f1-137">The term node is more general than the terms unit and terminal because non-USB devices can also have nodes.</span></span> <span data-ttu-id="668f1-138">若要取得篩選中節點的相關資訊，請查詢 [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) 介面的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="668f1-138">To get information about the nodes in a filter, query the filter for the [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) interface.</span></span> <span data-ttu-id="668f1-139">節點類型是由 Guid 所識別。</span><span class="sxs-lookup"><span data-stu-id="668f1-139">Node types are identified by GUIDs.</span></span> <span data-ttu-id="668f1-140">選取器節點是可在兩個或多個輸入之間切換的節點。</span><span class="sxs-lookup"><span data-stu-id="668f1-140">Selector nodes are nodes that can switch between two or more inputs.</span></span> <span data-ttu-id="668f1-141">選取器節點會公開 [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) 介面。</span><span class="sxs-lookup"><span data-stu-id="668f1-141">Selector nodes expose the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface.</span></span>

<span data-ttu-id="668f1-142">下列程式碼會測試篩選上的輸出釘選是否接收來自給定型別的節點輸入。</span><span class="sxs-lookup"><span data-stu-id="668f1-142">The following code tests whether an output pin on a filter receives input from a node of a given type.</span></span>


```C++
// Structure to hold topology information.
struct TopologyConnections
{
    KSTOPOLOGY_CONNECTION *connections; // Array of connections
    DWORD count;  // Number of elements in the array
};

/////////////////////////////////////////////////////////////////////
// Name: GetTopologyConnections
// Desc: Gets the topology information from a filter.
//
// pTopo:       Pointer to the filter's IKsTopologyInfo interface.
// connectInfo: Pointer to a TopologyConnections structure. The 
//              function fills in this structure.
//
// Note: If the function succeeds, call CoTaskMemFree to free the
//       pConnectInfo->connections array.
/////////////////////////////////////////////////////////////////////

HRESULT GetTopologyConnections(
    IKsTopologyInfo *pTopo, 
    TopologyConnections *pConnectInfo
    )
{
    DWORD count;
    HRESULT hr = pTopo->get_NumConnections(&count);
    if (FAILED(hr))
    {
        return hr;
    }

    pConnectInfo->count = count;
    pConnectInfo->connections = NULL;
    if (count > 0)
    {
        // Allocate an array for the connection information.
        SIZE_T cb = sizeof(KSTOPOLOGY_CONNECTION) * count;
        KSTOPOLOGY_CONNECTION *pConnections = 
            (KSTOPOLOGY_CONNECTION*) CoTaskMemAlloc(cb);
        if (pConnections == NULL)
        {
            return E_OUTOFMEMORY;
        }
        // Fill the array.
        for (DWORD ix = 0; ix < count; ix++)
        {
            hr = pTopo->get_ConnectionInfo(ix, &pConnections[ix]);
            if (FAILED(hr))
            {
                break;
            }
        }
        if (SUCCEEDED(hr))
        {
            pConnectInfo->connections = pConnections;
        }
        else
        {
           CoTaskMemFree(pConnections);
        }
    }
    return hr;
}

/////////////////////////////////////////////////////////////////////
// Name: IsNodeDownstreamFromNode
// Desc: Searches upstream from a node for a specified node type.
//
// pTopo:        Pointer to the filter's IKsTopologyInfo interface.
// connectInfo:  Contains toplogy information. To fill in this
//               structure, call GetTopologyConnections.
// nodeID:       ID of the starting node in the search.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected, or false otherwise.
//
// Note: If the source node matches the type, this function returns 
//       true without searching upstream.
/////////////////////////////////////////////////////////////////////

HRESULT IsNodeDownstreamFromNode(
    IKsTopologyInfo *pTopo,
    const TopologyConnections& connectInfo, 
    DWORD nodeID,
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    *pIsConnected = false;
    // Base case for recursion: check the source node.
    GUID type;
    HRESULT hr = pTopo->get_NodeType(nodeID, &type);
    if (FAILED(hr))
    {
        return hr;
    }
    if (type == nodeType)
    {
        *pIsConnected = true;
        return S_OK;
    }

    // If the source node is a selector, get the input node.
    CComPtr<ISelector> pSelector;
    hr = pTopo->CreateNodeInstance(nodeID, __uuidof(ISelector), 
        (void**)&pSelector);
    if (SUCCEEDED(hr))
    {
        DWORD sourceNodeID;
        hr = pSelector->get_SourceNodeId(&sourceNodeID);
        if (SUCCEEDED(hr))
        {
            // Recursive call with the selector's input node.
            return IsNodeDownstreamFromNode(pTopo, connectInfo, 
                       sourceNodeID, nodeType, pIsConnected);
        }
    }
    else if (hr == E_NOINTERFACE)
    {
        hr = S_OK;  // This node is not a selector. Not a failure.
    }
    else
    {
        return hr;
    }

    // Test all of the upstream connections on this pin. 
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == nodeID) &&
            (connectInfo.connections[ix].FromNode != KSFILTER_NODE))
        {
            // FromNode is connected to the source node.
            DWORD fromNode = connectInfo.connections[ix].FromNode;

            // Recursive call with the upstream node.
            bool bIsConnected;
            hr = IsNodeDownstreamFromNode(pTopo, connectInfo, 
                fromNode, nodeType, &bIsConnected);
            if (FAILED(hr))
            {
                break;
            }
            if (bIsConnected)
            {
                *pIsConnected = true;
                break;
            }
        }
    }
    return hr;
}


/////////////////////////////////////////////////////////////////////
// Name: GetNodeUpstreamFromPin
// Desc: Finds the node connected to an output pin.
//
// connectInfo: Contains toplogy information. To fill in this
//              structure, call GetTopologyConnections.
// nPinIndex:   Index of the output pin.
// pNodeID:     Receives the ID of the connected node.
/////////////////////////////////////////////////////////////////////

HRESULT GetNodeUpstreamFromPin(
    const TopologyConnections& connectInfo, 
    UINT nPinIndex, 
    DWORD *pNodeID
    )
{
    bool bFound = false;
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == KSFILTER_NODE) &&
            (connectInfo.connections[ix].ToNodePin == nPinIndex))
        {
            *pNodeID = connectInfo.connections[ix].FromNode;
            bFound = true;
            break;
        }
    }
    if (bFound)
    {
        return S_OK;
    }
    else
    {
        return E_FAIL;
    }
}


/////////////////////////////////////////////////////////////////////
// Name: IsPinDownstreamFromNode
// Desc: Tests whether an output pin gets data from a node of
//       a specified type.
// 
// pFilter:      Pointer to the filter's IBaseFilter interface.
// UINT:         Index of the output pin to test.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected; false otherwise.
/////////////////////////////////////////////////////////////////////

HRESULT IsPinDownstreamFromNode(
    IBaseFilter *pFilter, 
    UINT nPinIndex, 
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    CComQIPtr<IKsTopologyInfo> pTopo(pFilter);
    if (pTopo == NULL)
    {
        return E_NOINTERFACE;
    }

    // Get the topology connection information.
    TopologyConnections connectionInfo;
    HRESULT hr = GetTopologyConnections(pTopo, &connectionInfo);
    if (FAILED(hr))
    {
        return hr;
    }

    // Find the node upstream from this pin.
    DWORD nodeID;
    hr = GetNodeUpstreamFromPin(connectionInfo, nPinIndex, &nodeID);
    if (SUCCEEDED(hr))
    {
        bool isConnected;
        hr = IsNodeDownstreamFromNode(pTopo, connectionInfo, 
            nodeID, nodeType, &isConnected);
        if (SUCCEEDED(hr))
        {
            *pIsConnected = isConnected;
        }
    }
    CoTaskMemFree(connectionInfo.connections);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="668f1-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="668f1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="668f1-144">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="668f1-144">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



