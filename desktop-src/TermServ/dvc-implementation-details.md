---
title: DVC 執行詳細資料
description: 本節包含有關如何 (DVC) 用戶端模組寫入動態虛擬通道的資訊。
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969648"
---
# <a name="dvc-implementation-details"></a><span data-ttu-id="674cb-103">DVC 執行詳細資料</span><span class="sxs-lookup"><span data-stu-id="674cb-103">DVC Implementation Details</span></span>

<span data-ttu-id="674cb-104">本節包含有關如何 (DVC) 用戶端模組寫入動態虛擬通道的資訊。</span><span class="sxs-lookup"><span data-stu-id="674cb-104">This section contains information about how to write a dynamic virtual channel (DVC) client module.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="674cb-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="674cb-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="674cb-106">撰寫用戶端 DVC 模組</span><span class="sxs-lookup"><span data-stu-id="674cb-106">Writing a Client DVC Module</span></span>](writing-a-client-dvc-component.md)
</dt> <dd>

<span data-ttu-id="674cb-107">若要 (DVC) 用戶端模組寫入動態虛擬通道，您必須先執行並註冊遠端桌面連線 (RDC) 用戶端外掛程式。</span><span class="sxs-lookup"><span data-stu-id="674cb-107">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="674cb-108">DVC 外掛程式註冊</span><span class="sxs-lookup"><span data-stu-id="674cb-108">DVC plug-in registration</span></span>](dvc-plug-in-registration.md)
</dt> <dd>

<span data-ttu-id="674cb-109">描述遠端桌面連線 (RDC) 用戶端的動態虛擬通道 (DVC) 外掛程式專案的語法。</span><span class="sxs-lookup"><span data-stu-id="674cb-109">Describes syntax for the dynamic virtual channel (DVC) plug-in entry for the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="674cb-110">啟動 DVC 接聽程式</span><span class="sxs-lookup"><span data-stu-id="674cb-110">Starting a DVC Listener</span></span>](starting-a-dvc-listener.md)
</dt> <dd>

<span data-ttu-id="674cb-111">若要建立兩個動態虛擬通道之間的成功連接 (DVC) 遠端桌面連線 (RDC) 用戶端和伺服器上執行的模組，則 DVC 接聽程式必須正在執行且處於接聽狀態。</span><span class="sxs-lookup"><span data-stu-id="674cb-111">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

</dd> <dt>

[<span data-ttu-id="674cb-112">接受連接</span><span class="sxs-lookup"><span data-stu-id="674cb-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> <dd>

<span data-ttu-id="674cb-113">在某個時間點，動態虛擬通道 (DVC) 用戶端會要求 DVC 接聽程式的連接。</span><span class="sxs-lookup"><span data-stu-id="674cb-113">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span>

</dd> <dt>

[<span data-ttu-id="674cb-114">使用 DVC 通道寫入資料</span><span class="sxs-lookup"><span data-stu-id="674cb-114">Writing Data by Using a DVC Channel</span></span>](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

<span data-ttu-id="674cb-115">使用動態虛擬通道來寫入通道資料 (DVC) 是遠端桌面工作階段主機 (RD 工作階段主機) 伺服器和用戶端的對稱。</span><span class="sxs-lookup"><span data-stu-id="674cb-115">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span>

</dd> <dt>

[<span data-ttu-id="674cb-116">測試和調試</span><span class="sxs-lookup"><span data-stu-id="674cb-116">Testing and Debugging</span></span>](testing-and-debugging.md)
</dt> <dd>

<span data-ttu-id="674cb-117">有一個由遠端桌面連線 (RDC) 用戶端所執行的「echo」接聽程式，其一律存在並接聽連入連線。</span><span class="sxs-lookup"><span data-stu-id="674cb-117">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span>

</dd> <dt>

[<span data-ttu-id="674cb-118">DVC 用戶端外掛程式範例</span><span class="sxs-lookup"><span data-stu-id="674cb-118">DVC Client Plug-in Example</span></span>](dvc-client-plug-in-example.md)
</dt> <dd>

<span data-ttu-id="674cb-119">C + + 程式碼範例，說明如何) 用戶端動態虛擬通道 (DVC) 外掛程式建立遠端桌面連線 (RDC。</span><span class="sxs-lookup"><span data-stu-id="674cb-119">C++ code sample that shows how to create a Remote Desktop Connection (RDC) client dynamic virtual channel (DVC) plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="674cb-120">DVC 伺服器模組範例</span><span class="sxs-lookup"><span data-stu-id="674cb-120">DVC Server Module Example</span></span>](dvc-server-component-example.md)
</dt> <dd>

<span data-ttu-id="674cb-121">C + + 程式碼範例，說明如何建立伺服器端動態虛擬通道 (DVC) 模組。</span><span class="sxs-lookup"><span data-stu-id="674cb-121">C++ code sample that shows how to create the server-side dynamic virtual channel (DVC) module.</span></span>

</dd> </dl>

 

 




