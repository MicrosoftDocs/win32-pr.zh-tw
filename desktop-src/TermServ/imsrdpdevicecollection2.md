---
title: IMsRdpDeviceCollection2 介面
description: 代表裝置物件的集合。 這是 IMsRdpDeviceCollection 介面的增強功能。
ms.assetid: df4d704c-e031-4df1-aed1-11aacf8a6992
ms.tgt_platform: multiple
keywords:
- IMsRdpDeviceCollection2 介面遠端桌面服務
- IMsRdpDeviceCollection2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea35c0a66ad8bf5d291062eafb7be3ceae4ac58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965504"
---
# <a name="imsrdpdevicecollection2-interface"></a><span data-ttu-id="94672-106">IMsRdpDeviceCollection2 介面</span><span class="sxs-lookup"><span data-stu-id="94672-106">IMsRdpDeviceCollection2 interface</span></span>

<span data-ttu-id="94672-107">代表裝置物件的集合。</span><span class="sxs-lookup"><span data-stu-id="94672-107">Represents a collection of device objects.</span></span> <span data-ttu-id="94672-108">這是 [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) 介面的增強功能。</span><span class="sxs-lookup"><span data-stu-id="94672-108">This is an enhancement to the [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="94672-109">成員</span><span class="sxs-lookup"><span data-stu-id="94672-109">Members</span></span>

<span data-ttu-id="94672-110">**IMsRdpDeviceCollection2** 介面繼承自 [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)。</span><span class="sxs-lookup"><span data-stu-id="94672-110">The **IMsRdpDeviceCollection2** interface inherits from [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span></span> <span data-ttu-id="94672-111">**IMsRdpDeviceCollection2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="94672-111">**IMsRdpDeviceCollection2** also has these types of members:</span></span>

-   [<span data-ttu-id="94672-112">方法</span><span class="sxs-lookup"><span data-stu-id="94672-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="94672-113">方法</span><span class="sxs-lookup"><span data-stu-id="94672-113">Methods</span></span>

<span data-ttu-id="94672-114">**IMsRdpDeviceCollection2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="94672-114">The **IMsRdpDeviceCollection2** interface has these methods.</span></span>



| <span data-ttu-id="94672-115">方法</span><span class="sxs-lookup"><span data-stu-id="94672-115">Method</span></span>                                                                         | <span data-ttu-id="94672-116">描述</span><span class="sxs-lookup"><span data-stu-id="94672-116">Description</span></span>                                                                                                 |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94672-117">**AddDeviceByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="94672-117">**AddDeviceByInstanceId**</span></span>](imsrdpdevicecollection2-adddevicebyinstanceid.md) | <span data-ttu-id="94672-118">將未列出的裝置新增至裝置集合。</span><span class="sxs-lookup"><span data-stu-id="94672-118">Adds an unlisted device to the device collection.</span></span><br/>                                                |
| [<span data-ttu-id="94672-119">**RedirectNow**</span><span class="sxs-lookup"><span data-stu-id="94672-119">**RedirectNow**</span></span>](imsrdpdevicecollection2-redirectnow.md)                     | <span data-ttu-id="94672-120">強制將從集合中選取或取消選取的裝置重新導向或移除。</span><span class="sxs-lookup"><span data-stu-id="94672-120">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="94672-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="94672-121">Requirements</span></span>



| <span data-ttu-id="94672-122">需求</span><span class="sxs-lookup"><span data-stu-id="94672-122">Requirement</span></span> | <span data-ttu-id="94672-123">值</span><span class="sxs-lookup"><span data-stu-id="94672-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="94672-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94672-124">Minimum supported client</span></span><br/> | <span data-ttu-id="94672-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="94672-125">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="94672-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94672-126">Minimum supported server</span></span><br/> | <span data-ttu-id="94672-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="94672-127">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="94672-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="94672-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="94672-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94672-129"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="94672-130">DLL</span><span class="sxs-lookup"><span data-stu-id="94672-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94672-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94672-131"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="94672-132">IID</span><span class="sxs-lookup"><span data-stu-id="94672-132">IID</span></span><br/>                      | <span data-ttu-id="94672-133">IID \_ IMsRdpDeviceCollection2 定義為 e0e5d68a-f2e7-4350-adfe-ac0e08d74de0</span><span class="sxs-lookup"><span data-stu-id="94672-133">IID\_IMsRdpDeviceCollection2 is defined as e0e5d68a-f2e7-4350-adfe-ac0e08d74de0</span></span><br/> |



 

 





