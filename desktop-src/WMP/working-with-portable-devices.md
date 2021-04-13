---
title: 使用可攜式裝置
description: 使用可攜式裝置
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Windows Media Player，可攜式裝置
- Windows Media Player 物件模型，可攜式裝置
- 物件模型，可攜式裝置
- Windows Media Player 的 ActiveX 控制項、可攜式裝置
- ActiveX 控制項、可攜式裝置
- Windows Media Player Mobile ActiveX 控制項、可攜式裝置
- Windows Media Player Mobile、可攜式裝置
- 可攜式裝置，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64c6e7047864b899a2d7dca2ba4754cc7cb5dc2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311313"
---
# <a name="working-with-portable-devices"></a><span data-ttu-id="7f8dd-111">使用可攜式裝置</span><span class="sxs-lookup"><span data-stu-id="7f8dd-111">Working with Portable Devices</span></span>

<span data-ttu-id="7f8dd-112">本節說明如何使用遠端 Windows Media Player ActiveX 控制項來處理可攜式裝置。</span><span class="sxs-lookup"><span data-stu-id="7f8dd-112">This section describes how to use a remoted Windows Media Player ActiveX control to work with portable devices.</span></span>

<span data-ttu-id="7f8dd-113">本節中的程式碼範例會使用 Active Template Library (ATL) 類別，例如 **CComPtr**。</span><span class="sxs-lookup"><span data-stu-id="7f8dd-113">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="7f8dd-114">包含的標頭</span><span class="sxs-lookup"><span data-stu-id="7f8dd-114">Included Headers</span></span>

<span data-ttu-id="7f8dd-115">若要使用本節中的程式碼，請包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="7f8dd-115">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a><span data-ttu-id="7f8dd-116">IWMPPlayer 指標</span><span class="sxs-lookup"><span data-stu-id="7f8dd-116">IWMPPlayer Pointer</span></span>

<span data-ttu-id="7f8dd-117">**IWMPPlayer** 指標會儲存在成員變數中。</span><span class="sxs-lookup"><span data-stu-id="7f8dd-117">The **IWMPPlayer** pointer is stored in a member variable.</span></span>


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a><span data-ttu-id="7f8dd-118">裝置會儲存在陣列中</span><span class="sxs-lookup"><span data-stu-id="7f8dd-118">Devices are Stored in an Array</span></span>

<span data-ttu-id="7f8dd-119">範例程式碼會存取在專案標頭中宣告的下列成員變數：</span><span class="sxs-lookup"><span data-stu-id="7f8dd-119">The example code accesses the following member variable, to be declared in the project header:</span></span>


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



<span data-ttu-id="7f8dd-120">裝置計數會儲存在成員變數中。</span><span class="sxs-lookup"><span data-stu-id="7f8dd-120">The device count is stored in a member variable.</span></span>


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a><span data-ttu-id="7f8dd-121">正在抓取裝置指標</span><span class="sxs-lookup"><span data-stu-id="7f8dd-121">Retrieving a Device Pointer</span></span>

<span data-ttu-id="7f8dd-122">使用與下列類似的程式碼，透過其陣列索引來抓取特定裝置的指標：</span><span class="sxs-lookup"><span data-stu-id="7f8dd-122">A pointer to a particular device is retrieved through its array index by using code similar to the following:</span></span>


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



<span data-ttu-id="7f8dd-123">請注意，上述範例中所顯示的索引不是裝置的合作關係索引。</span><span class="sxs-lookup"><span data-stu-id="7f8dd-123">Note that the index shown in the preceding examples is not the partnership index for the device.</span></span> <span data-ttu-id="7f8dd-124">它是裝置在自訂陣列中的索引。</span><span class="sxs-lookup"><span data-stu-id="7f8dd-124">It is the index to the device in the custom array of devices.</span></span>

## <a name="cleaning-up"></a><span data-ttu-id="7f8dd-125">清理</span><span class="sxs-lookup"><span data-stu-id="7f8dd-125">Cleaning Up</span></span>

<span data-ttu-id="7f8dd-126">這些範例會使用下列函式釋放裝置陣列中的記憶體，並釋放介面指標：</span><span class="sxs-lookup"><span data-stu-id="7f8dd-126">The examples use the following function to free the memory in the device array and to release the interface pointers:</span></span>


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a><span data-ttu-id="7f8dd-127">裝置會顯示在清單方塊中</span><span class="sxs-lookup"><span data-stu-id="7f8dd-127">Devices are Displayed in a List Box</span></span>

<span data-ttu-id="7f8dd-128">GetSelectedDeviceIndex 函式會使用下列程式碼，傳回使用者在清單方塊中選取之裝置的索引：</span><span class="sxs-lookup"><span data-stu-id="7f8dd-128">The GetSelectedDeviceIndex function returns the index of the device the user selected in a list box by using the following code:</span></span>


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a><span data-ttu-id="7f8dd-129">消費者介面狀態是由單一函式管理</span><span class="sxs-lookup"><span data-stu-id="7f8dd-129">User Interface State is Managed by a Single Function</span></span>

<span data-ttu-id="7f8dd-130">SetUIState 函數會管理使用者介面。</span><span class="sxs-lookup"><span data-stu-id="7f8dd-130">The SetUIState function manages the user interface.</span></span>


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



<span data-ttu-id="7f8dd-131">此函數的詳細資料與本節中的討論無關，但請注意，此函式會執行工作，例如啟用或停用控制項，以及變更使用者介面中的顯示文字。</span><span class="sxs-lookup"><span data-stu-id="7f8dd-131">The details of this function are not relevant to the discussions in this section, but be aware that this function performs tasks like enabling or disabling controls and changing display text in the user interface.</span></span>

<span data-ttu-id="7f8dd-132">UIState 列舉的定義如下：</span><span class="sxs-lookup"><span data-stu-id="7f8dd-132">The UIState enumeration was defined as follows:</span></span>


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



<span data-ttu-id="7f8dd-133">*BConnected* 參數會指定是否要為連線的裝置設定使用者介面 (TRUE 表示裝置已連線) 。</span><span class="sxs-lookup"><span data-stu-id="7f8dd-133">The *bConnected* parameter specifies whether to configure the user interface for a connected device (TRUE means the device is connected).</span></span> <span data-ttu-id="7f8dd-134">*NewState* 和 *bConnected* 參數會傳達函數執行其工作所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="7f8dd-134">The *NewState* and *bConnected* parameters convey the information needed for the function to do its work.</span></span>

<span data-ttu-id="7f8dd-135">下列各節提供範例程式碼的說明：</span><span class="sxs-lookup"><span data-stu-id="7f8dd-135">The following sections provide explanations of the example code:</span></span>

-   [<span data-ttu-id="7f8dd-136">列舉裝置</span><span class="sxs-lookup"><span data-stu-id="7f8dd-136">Enumerating Devices</span></span>](enumerating-devices.md)
-   [<span data-ttu-id="7f8dd-137">正在抓取裝置屬性</span><span class="sxs-lookup"><span data-stu-id="7f8dd-137">Retrieving Device Attributes</span></span>](retrieving-device-attributes.md)
-   [<span data-ttu-id="7f8dd-138">顯示同步處理進度</span><span class="sxs-lookup"><span data-stu-id="7f8dd-138">Showing Synchronization Progress</span></span>](showing-synchronization-progress.md)
-   [<span data-ttu-id="7f8dd-139">管理同步播放清單</span><span class="sxs-lookup"><span data-stu-id="7f8dd-139">Managing Synchronization Playlists</span></span>](managing-synchronization-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="7f8dd-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f8dd-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f8dd-141">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="7f8dd-141">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




