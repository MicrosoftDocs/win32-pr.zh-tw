---
title: 一般使用者控制點應用程式
description: 一般使用者控制點 (UCP) 應用程式可讓您探索裝置、控制這些探索到的裝置，以及查看相關的事件資訊，全都使用圖形化介面。
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104555859"
---
# <a name="generic-user-control-point-application"></a><span data-ttu-id="29b6f-103">一般使用者控制點應用程式</span><span class="sxs-lookup"><span data-stu-id="29b6f-103">Generic User Control Point Application</span></span>

<span data-ttu-id="29b6f-104">一般使用者控制點 (UCP) 應用程式可讓您探索裝置、控制這些探索到的裝置，以及查看相關的事件資訊，全都使用圖形化介面。</span><span class="sxs-lookup"><span data-stu-id="29b6f-104">The generic user control point (UCP) application allows you to discover devices, control those discovered devices, and view the related eventing information, all using a graphical interface.</span></span>

<span data-ttu-id="29b6f-105">**若要啟動泛型 UCP 應用程式**</span><span class="sxs-lookup"><span data-stu-id="29b6f-105">**To start the generic UCP application**</span></span>

1.  <span data-ttu-id="29b6f-106">建立並設定範例 \\ netds \\ upnp \\ GenericUCP \\ CPPdevtype.txt 檔 \\ (或 \\ \\ 使用裝置資訊) 的devtype.txt 檔。</span><span class="sxs-lookup"><span data-stu-id="29b6f-106">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\devtype.txt file (or the \\VisualBasic\\devtype.txt file) with device information.</span></span> <span data-ttu-id="29b6f-107">此檔案可讓您針對「依類型尋找」和「非同步尋找」搜尋設定泛型 UCP。</span><span class="sxs-lookup"><span data-stu-id="29b6f-107">This file allows you to configure the generic UCP for the "find by type" and "async find" searches.</span></span> <span data-ttu-id="29b6f-108">檔案的每一行都必須包含裝置類型和相關的描述。</span><span class="sxs-lookup"><span data-stu-id="29b6f-108">Each line of the file must contain a device type and the related description.</span></span> <span data-ttu-id="29b6f-109">例如：</span><span class="sxs-lookup"><span data-stu-id="29b6f-109">For example:</span></span>

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    <span data-ttu-id="29b6f-110">此範例適用于虛構的 media player 裝置。</span><span class="sxs-lookup"><span data-stu-id="29b6f-110">This example is for a fictitious media player device.</span></span> <span data-ttu-id="29b6f-111">第二行結尾的「媒體播放機」不是裝置類型的一部分，而是用於一般 UCP 應用程式中的資訊用途。</span><span class="sxs-lookup"><span data-stu-id="29b6f-111">The "Media Player" at the end of the second line is not a part of the device type, it is for informational purposes in the Generic UCP application.</span></span> <span data-ttu-id="29b6f-112">這同樣適用于第一行中的「所有根裝置」。</span><span class="sxs-lookup"><span data-stu-id="29b6f-112">The same applies to "All Root Devices" in the first line.</span></span>

    <span data-ttu-id="29b6f-113">加入一行，其中包含您的特定裝置類型和每個裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="29b6f-113">Add a line that contains your specific device type and description for each device.</span></span>

2.  <span data-ttu-id="29b6f-114">建立並設定範例 \\ netds \\ upnp \\ GenericUCP \\ CPPudn.txt 檔 \\ (或 \\ \\ 使用您裝置的 UDN 資訊) 的udn.txt 檔。</span><span class="sxs-lookup"><span data-stu-id="29b6f-114">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\udn.txt file (or the \\VisualBasic\\udn.txt file) with UDN information for your devices.</span></span> <span data-ttu-id="29b6f-115">此檔案可讓您設定 "find by UDN" 搜尋的一般 UCP。</span><span class="sxs-lookup"><span data-stu-id="29b6f-115">This file allows you to configure the generic UCP for the "find by UDN" search.</span></span> <span data-ttu-id="29b6f-116">每一行都會使用下列格式：</span><span class="sxs-lookup"><span data-stu-id="29b6f-116">Each line uses the following form:</span></span>

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    <span data-ttu-id="29b6f-117">新增包含每個裝置特定 UDN 的行。</span><span class="sxs-lookup"><span data-stu-id="29b6f-117">Add a line that contains your specific UDN for each device.</span></span>

3.  <span data-ttu-id="29b6f-118">執行 GenericUCP.exe。</span><span class="sxs-lookup"><span data-stu-id="29b6f-118">Run GenericUCP.exe.</span></span> <span data-ttu-id="29b6f-119">[ **一般 UCP** ] 視窗隨即出現。</span><span class="sxs-lookup"><span data-stu-id="29b6f-119">The **Generic UCP** window appears.</span></span>

    ![一般 ucp 視窗](images/generic-ucp.png)

> [!Note]  
> <span data-ttu-id="29b6f-121">**View Presentation** 和 **view Service Desc。** 功能不會在 c + + 範例程式碼中執行。</span><span class="sxs-lookup"><span data-stu-id="29b6f-121">The **View Presentation** and **View Service Desc.** functionality is not implemented in the C++ sample code.</span></span>

 

 

 




