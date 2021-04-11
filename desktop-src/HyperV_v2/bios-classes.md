---
description: 虛擬 BIOS 是載入 RAM 的軟體映射，可設定部分的基本層面，並將電腦系統開機。 每台電腦系統都有一個 BIOS 元素，而且無法取代或移除該元素。
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: BIOS 類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944300"
---
# <a name="bios-classes"></a><span data-ttu-id="b2e2d-104">BIOS 類別</span><span class="sxs-lookup"><span data-stu-id="b2e2d-104">BIOS classes</span></span>

<span data-ttu-id="b2e2d-105">虛擬 BIOS 是載入 RAM 的軟體映射，可設定部分的基本層面，並將電腦系統開機。</span><span class="sxs-lookup"><span data-stu-id="b2e2d-105">The virtual BIOS is a software image that is loaded into RAM to configure some of the basic aspects of and boot a computer system.</span></span> <span data-ttu-id="b2e2d-106">每台電腦系統都有一個 BIOS 元素，而且無法取代或移除該元素。</span><span class="sxs-lookup"><span data-stu-id="b2e2d-106">There is one BIOS element per computer system and that element cannot be replaced or removed.</span></span> <span data-ttu-id="b2e2d-107">因此，沒有任何資源集區可將新的 BIOS 元素新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b2e2d-107">Thus, there is no resource pool for adding new BIOS elements to the virtual machine.</span></span> <span data-ttu-id="b2e2d-108">BIOS 元素也沒有自己的 SettingData 類別來描述 BIOS 的設定。</span><span class="sxs-lookup"><span data-stu-id="b2e2d-108">The BIOS element also does not have its own SettingData class to describe the settings for the BIOS.</span></span> <span data-ttu-id="b2e2d-109">您可以在 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 類別中找到 BIOS 的設定，例如序號、開機順序和 num lock 狀態。</span><span class="sxs-lookup"><span data-stu-id="b2e2d-109">Settings for the BIOS, such as serial numbers, boot order, and num lock state, are found in the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span>

<span data-ttu-id="b2e2d-110">以下是與 BIOS 相關的虛擬化 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="b2e2d-110">The following are virtualization WMI classes related to the BIOS.</span></span> <span data-ttu-id="b2e2d-111">這些類別位於中 \\ \\ 。 \\根 \\ 虛擬化命名空間。</span><span class="sxs-lookup"><span data-stu-id="b2e2d-111">These classes are in the \\\\.\\Root\\Virtualization namespace.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b2e2d-112">本節內容</span><span class="sxs-lookup"><span data-stu-id="b2e2d-112">In this section</span></span>



| <span data-ttu-id="b2e2d-113">主題</span><span class="sxs-lookup"><span data-stu-id="b2e2d-113">Topic</span></span>                                                    | <span data-ttu-id="b2e2d-114">描述</span><span class="sxs-lookup"><span data-stu-id="b2e2d-114">Description</span></span>                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2e2d-115">**Msvm \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="b2e2d-115">**Msvm\_BIOSElement**</span></span>](msvm-bioselement.md)<br/> | <span data-ttu-id="b2e2d-116">代表載入 RAM 以設定及啟動系統的低層級軟體。</span><span class="sxs-lookup"><span data-stu-id="b2e2d-116">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span><br/> |
| [<span data-ttu-id="b2e2d-117">**Msvm \_ SystemBIOS**</span><span class="sxs-lookup"><span data-stu-id="b2e2d-117">**Msvm\_SystemBIOS**</span></span>](msvm-systembios.md)<br/>   | <span data-ttu-id="b2e2d-118">用來將虛擬機器與其 BIOS 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b2e2d-118">Used to associate a virtual machine with its BIOS.</span></span><br/>                                           |



 

 

 




