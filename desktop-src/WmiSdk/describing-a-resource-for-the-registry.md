---
description: 系統登錄包含與資源相關的資料。
ms.assetid: e66f1db8-a5f3-41d3-9835-34b81b9da5ed
ms.tgt_platform: multiple
title: 描述登錄的資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba175120b5abec238d1b9078010359effef8ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979276"
---
# <a name="describing-a-resource-for-the-registry"></a><span data-ttu-id="90576-103">描述登錄的資源</span><span class="sxs-lookup"><span data-stu-id="90576-103">Describing a Resource for the Registry</span></span>

<span data-ttu-id="90576-104">系統登錄包含與資源相關的資料。</span><span class="sxs-lookup"><span data-stu-id="90576-104">The system registry contains resource-related data.</span></span> <span data-ttu-id="90576-105">這項資料位於下列登錄機碼底下，並保留在名為 **REG \_ RESOURCE \_ LIST** 的特殊登錄資料類型中。</span><span class="sxs-lookup"><span data-stu-id="90576-105">This data is located under the following registry key and is kept in a special registry data type named **REG\_RESOURCE\_LIST**.</span></span> <span data-ttu-id="90576-106">應用程式可以透過系統登錄提供者取得與資源相關的資料。</span><span class="sxs-lookup"><span data-stu-id="90576-106">Applications can obtain the resource-related data through the System Registry provider.</span></span> <span data-ttu-id="90576-107">您可以新增和修改登錄中的系統資源。</span><span class="sxs-lookup"><span data-stu-id="90576-107">You can add and modify system resources in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Hardware
      ResourceMap
```

<span data-ttu-id="90576-108">下列程式說明如何在系統登錄中儲存與資源相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="90576-108">The following procedure describes how to store resource-related information in the system registry.</span></span>

<span data-ttu-id="90576-109">**在系統登錄中儲存與資源相關的資訊**</span><span class="sxs-lookup"><span data-stu-id="90576-109">**To store resource-related information in the system registry**</span></span>

1.  <span data-ttu-id="90576-110">建立包含下欄欄位的字串。</span><span class="sxs-lookup"><span data-stu-id="90576-110">Create a string that contains the following fields.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="90576-111">欄位</span><span class="sxs-lookup"><span data-stu-id="90576-111">Field</span></span></th>
    <th><span data-ttu-id="90576-112">包含</span><span class="sxs-lookup"><span data-stu-id="90576-112">Contains</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="90576-113">介面類型</span><span class="sxs-lookup"><span data-stu-id="90576-113">Interface type</span></span></td>
    <td><span data-ttu-id="90576-114">下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="90576-114">One of the following values:</span></span><br/> <dl> <span data-ttu-id="90576-115">內部</span><span class="sxs-lookup"><span data-stu-id="90576-115">Internal</span></span><br />
    <span data-ttu-id="90576-116">Isa</span><span class="sxs-lookup"><span data-stu-id="90576-116">Isa</span></span><br />
    <span data-ttu-id="90576-117">Eisa</span><span class="sxs-lookup"><span data-stu-id="90576-117">Eisa</span></span><br />
    <span data-ttu-id="90576-118">MicroChannel</span><span class="sxs-lookup"><span data-stu-id="90576-118">MicroChannel</span></span><br />
    <span data-ttu-id="90576-119">TurboChannel</span><span class="sxs-lookup"><span data-stu-id="90576-119">TurboChannel</span></span><br />
    <span data-ttu-id="90576-120">PCIBus</span><span class="sxs-lookup"><span data-stu-id="90576-120">PCIBus</span></span><br />
    <span data-ttu-id="90576-121">VMEBus</span><span class="sxs-lookup"><span data-stu-id="90576-121">VMEBus</span></span><br />
    <span data-ttu-id="90576-122">NuBus</span><span class="sxs-lookup"><span data-stu-id="90576-122">NuBus</span></span><br />
    <span data-ttu-id="90576-123">PCMCIABus</span><span class="sxs-lookup"><span data-stu-id="90576-123">PCMCIABus</span></span><br />
    <span data-ttu-id="90576-124">CBus</span><span class="sxs-lookup"><span data-stu-id="90576-124">CBus</span></span><br />
    <span data-ttu-id="90576-125">MPIBus</span><span class="sxs-lookup"><span data-stu-id="90576-125">MPIBus</span></span><br />
    <span data-ttu-id="90576-126">MPSABus</span><span class="sxs-lookup"><span data-stu-id="90576-126">MPSABus</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="90576-127">匯流排編號</span><span class="sxs-lookup"><span data-stu-id="90576-127">Bus number</span></span></td>
    <td><span data-ttu-id="90576-128">指定匯流排編號的整數。</span><span class="sxs-lookup"><span data-stu-id="90576-128">Integer specifying the bus number.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="90576-129">部分描述元編號</span><span class="sxs-lookup"><span data-stu-id="90576-129">Partial descriptor number</span></span></td>
    <td><span data-ttu-id="90576-130">指定描述項編號的整數。</span><span class="sxs-lookup"><span data-stu-id="90576-130">Integer specifying the descriptor number.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="90576-131">Offset 或 union 類型</span><span class="sxs-lookup"><span data-stu-id="90576-131">Offset or union type</span></span></td>
    <td><span data-ttu-id="90576-132">下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="90576-132">One of the following values:</span></span><br/> <dl> <span data-ttu-id="90576-133">埠。啟動</span><span class="sxs-lookup"><span data-stu-id="90576-133">Port.Start</span></span><br />
    <span data-ttu-id="90576-134">Port. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="90576-134">Port.PhysicalAddress</span></span><br />
    <span data-ttu-id="90576-135">埠。長度</span><span class="sxs-lookup"><span data-stu-id="90576-135">Port.Length</span></span><br />
    <span data-ttu-id="90576-136">中斷。層級</span><span class="sxs-lookup"><span data-stu-id="90576-136">Interrupt.Level</span></span><br />
    <span data-ttu-id="90576-137">插斷向量</span><span class="sxs-lookup"><span data-stu-id="90576-137">Interrupt.Vector</span></span><br />
    <span data-ttu-id="90576-138">插斷的親和性</span><span class="sxs-lookup"><span data-stu-id="90576-138">Interrupt.Affinity</span></span><br />
    <span data-ttu-id="90576-139">記憶體。開始</span><span class="sxs-lookup"><span data-stu-id="90576-139">Memory.Start</span></span><br />
    <span data-ttu-id="90576-140">Memory. PhysicalAddress</span><span class="sxs-lookup"><span data-stu-id="90576-140">Memory.PhysicalAddress</span></span><br />
    <span data-ttu-id="90576-141">記憶體。長度</span><span class="sxs-lookup"><span data-stu-id="90576-141">Memory.Length</span></span><br />
    <span data-ttu-id="90576-142">Dma。通道</span><span class="sxs-lookup"><span data-stu-id="90576-142">Dma.Channel</span></span><br />
    <span data-ttu-id="90576-143">Dma。埠</span><span class="sxs-lookup"><span data-stu-id="90576-143">Dma.Port</span></span><br />
    <span data-ttu-id="90576-144">Dma. Reserved1</span><span class="sxs-lookup"><span data-stu-id="90576-144">Dma.Reserved1</span></span><br />
    <span data-ttu-id="90576-145">DeviceSpecificData</span><span class="sxs-lookup"><span data-stu-id="90576-145">DeviceSpecificData.DataSize</span></span><br />
    <span data-ttu-id="90576-146">DeviceSpecificData. Reserved1</span><span class="sxs-lookup"><span data-stu-id="90576-146">DeviceSpecificData.Reserved1</span></span><br />
    <span data-ttu-id="90576-147">DeviceSpecificData. Reserved2</span><span class="sxs-lookup"><span data-stu-id="90576-147">DeviceSpecificData.Reserved2</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="90576-148">將字串放在登錄機碼底下的適當機碼中。</span><span class="sxs-lookup"><span data-stu-id="90576-148">Place the string in the appropriate key under the registry key.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Hardware
          ResourceMap
    ```

<span data-ttu-id="90576-149">下列程式碼範例說明有效的資源描述項。</span><span class="sxs-lookup"><span data-stu-id="90576-149">The following code example describes a valid resource descriptor.</span></span>

``` syntax
local|hkey_local_machine\hardware\resourcemap\
  hardware abstraction layer\
  pc compatible eisa/isa HAL|.raw("eisa",0,0,"interrupt.affinity")
```

<span data-ttu-id="90576-150">下列程式碼範例顯示用於抓取資源描述項的有效 MOF 語法。</span><span class="sxs-lookup"><span data-stu-id="90576-150">The following code example shows valid MOF syntax for retrieving a resource descriptor.</span></span>

``` syntax
[DYNPROPS] 
class MyRegProp
{    
   [KEY]  
   STRING MyKey; 
   STRING MyReservedTranslated;
};

[DYNPROPS] 
instance of MyRegProp
{
   MyKey = "1";
   [PropertyContext("local|hkey_local_Machine\\hardware\\ResourceMap\\
                   System Resources\\Reserved|.Translated
                   (\"Internal\")(0)(1)(\"Memory.PhysicalAddress\")"),
   Dynamic, Provider("RegPropProv")] 
   MyReservedTranslated;
};
```

 

 




