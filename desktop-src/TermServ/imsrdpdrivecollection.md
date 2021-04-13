---
title: IMsRdpDriveCollection 介面
description: 代表磁片磁碟機物件的集合。
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- IMsRdpDriveCollection 介面遠端桌面服務
- IMsRdpDriveCollection 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465988"
---
# <a name="imsrdpdrivecollection-interface"></a><span data-ttu-id="65b7d-105">IMsRdpDriveCollection 介面</span><span class="sxs-lookup"><span data-stu-id="65b7d-105">IMsRdpDriveCollection interface</span></span>

<span data-ttu-id="65b7d-106">代表磁片磁碟機物件的集合。</span><span class="sxs-lookup"><span data-stu-id="65b7d-106">Represents a collection of drive objects.</span></span>

## <a name="members"></a><span data-ttu-id="65b7d-107">成員</span><span class="sxs-lookup"><span data-stu-id="65b7d-107">Members</span></span>

<span data-ttu-id="65b7d-108">**IMsRdpDriveCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="65b7d-108">The **IMsRdpDriveCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="65b7d-109">**IMsRdpDriveCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="65b7d-109">**IMsRdpDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="65b7d-110">方法</span><span class="sxs-lookup"><span data-stu-id="65b7d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="65b7d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="65b7d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="65b7d-112">方法</span><span class="sxs-lookup"><span data-stu-id="65b7d-112">Methods</span></span>

<span data-ttu-id="65b7d-113">**IMsRdpDriveCollection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="65b7d-113">The **IMsRdpDriveCollection** interface has these methods.</span></span>



| <span data-ttu-id="65b7d-114">方法</span><span class="sxs-lookup"><span data-stu-id="65b7d-114">Method</span></span>                                                     | <span data-ttu-id="65b7d-115">描述</span><span class="sxs-lookup"><span data-stu-id="65b7d-115">Description</span></span>                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="65b7d-116">**RescanDrives**</span><span class="sxs-lookup"><span data-stu-id="65b7d-116">**RescanDrives**</span></span>](imsrdpdrivecollection-rescandrives.md) | <span data-ttu-id="65b7d-117">重新整理集合中的物件清單。</span><span class="sxs-lookup"><span data-stu-id="65b7d-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="65b7d-118">屬性</span><span class="sxs-lookup"><span data-stu-id="65b7d-118">Properties</span></span>

<span data-ttu-id="65b7d-119">**IMsRdpDriveCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="65b7d-119">The **IMsRdpDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="65b7d-120">屬性</span><span class="sxs-lookup"><span data-stu-id="65b7d-120">Property</span></span>                                                              | <span data-ttu-id="65b7d-121">存取類型</span><span class="sxs-lookup"><span data-stu-id="65b7d-121">Access type</span></span>          | <span data-ttu-id="65b7d-122">Description</span><span class="sxs-lookup"><span data-stu-id="65b7d-122">Description</span></span>                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="65b7d-123">**DriveByIndex**</span><span class="sxs-lookup"><span data-stu-id="65b7d-123">**DriveByIndex**</span></span>](imsrdpdrivecollection-drivebyindex.md)<br/> | <span data-ttu-id="65b7d-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="65b7d-124">Read-only</span></span><br/> | <span data-ttu-id="65b7d-125">抓取位於指定之索引處的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="65b7d-125">Retrieves the drive at the specified index.</span></span><br/>       |
| [<span data-ttu-id="65b7d-126">**DriveCount**</span><span class="sxs-lookup"><span data-stu-id="65b7d-126">**DriveCount**</span></span>](imsrdpdrivecollection-drivecount.md)<br/>     | <span data-ttu-id="65b7d-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="65b7d-127">Read-only</span></span><br/> | <span data-ttu-id="65b7d-128">抓取集合中的物件計數。</span><span class="sxs-lookup"><span data-stu-id="65b7d-128">Retrieves the count of objects in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="65b7d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="65b7d-129">Requirements</span></span>



| <span data-ttu-id="65b7d-130">需求</span><span class="sxs-lookup"><span data-stu-id="65b7d-130">Requirement</span></span> | <span data-ttu-id="65b7d-131">值</span><span class="sxs-lookup"><span data-stu-id="65b7d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b7d-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65b7d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="65b7d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65b7d-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="65b7d-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65b7d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="65b7d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65b7d-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="65b7d-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="65b7d-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="65b7d-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b7d-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="65b7d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="65b7d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65b7d-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b7d-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="65b7d-140">IID</span><span class="sxs-lookup"><span data-stu-id="65b7d-140">IID</span></span><br/>                      | <span data-ttu-id="65b7d-141">IID \_ IMsRdpDriveCollection 定義為 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="65b7d-141">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65b7d-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65b7d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b7d-143">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="65b7d-143">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="65b7d-144">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="65b7d-144">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

