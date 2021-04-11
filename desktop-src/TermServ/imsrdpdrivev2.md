---
title: IMsRdpDriveV2 介面
description: 包含磁片磁碟機物件的相關資訊。 這是 IMsRdpDrive 介面的增強功能。
ms.assetid: 0d804fcc-960f-48f7-9794-b7be8d7e258e
ms.tgt_platform: multiple
keywords:
- IMsRdpDriveV2 介面遠端桌面服務
- IMsRdpDriveV2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDriveV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c397e96d4f3b0dbb172c6e10eba4e09ff96e37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094035"
---
# <a name="imsrdpdrivev2-interface"></a><span data-ttu-id="1b2ae-106">IMsRdpDriveV2 介面</span><span class="sxs-lookup"><span data-stu-id="1b2ae-106">IMsRdpDriveV2 interface</span></span>

<span data-ttu-id="1b2ae-107">包含磁片磁碟機物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1b2ae-107">Contains information about a drive object.</span></span> <span data-ttu-id="1b2ae-108">這是 [**IMsRdpDrive**](imsrdpdrive.md) 介面的增強功能。</span><span class="sxs-lookup"><span data-stu-id="1b2ae-108">This is an enhancement of the [**IMsRdpDrive**](imsrdpdrive.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="1b2ae-109">成員</span><span class="sxs-lookup"><span data-stu-id="1b2ae-109">Members</span></span>

<span data-ttu-id="1b2ae-110">**IMsRdpDriveV2** 介面繼承自 [**IMsRdpDrive**](imsrdpdrive.md)。</span><span class="sxs-lookup"><span data-stu-id="1b2ae-110">The **IMsRdpDriveV2** interface inherits from [**IMsRdpDrive**](imsrdpdrive.md).</span></span> <span data-ttu-id="1b2ae-111">**IMsRdpDriveV2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1b2ae-111">**IMsRdpDriveV2** also has these types of members:</span></span>

-   [<span data-ttu-id="1b2ae-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1b2ae-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b2ae-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1b2ae-113">Properties</span></span>

<span data-ttu-id="1b2ae-114">**IMsRdpDriveV2** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1b2ae-114">The **IMsRdpDriveV2** interface has these properties.</span></span>



| <span data-ttu-id="1b2ae-115">屬性</span><span class="sxs-lookup"><span data-stu-id="1b2ae-115">Property</span></span>                                                              | <span data-ttu-id="1b2ae-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="1b2ae-116">Access type</span></span>          | <span data-ttu-id="1b2ae-117">Description</span><span class="sxs-lookup"><span data-stu-id="1b2ae-117">Description</span></span>                                                |
|:----------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="1b2ae-118">**DriveLetterIndex**</span><span class="sxs-lookup"><span data-stu-id="1b2ae-118">**DriveLetterIndex**</span></span>](imsrdpdrivev2-driveletterindex.md)<br/> | <span data-ttu-id="1b2ae-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="1b2ae-119">Read-only</span></span><br/> | <span data-ttu-id="1b2ae-120">包含磁片磁碟機的字母索引。</span><span class="sxs-lookup"><span data-stu-id="1b2ae-120">Contains the index of the letter for the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1b2ae-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b2ae-121">Requirements</span></span>



| <span data-ttu-id="1b2ae-122">需求</span><span class="sxs-lookup"><span data-stu-id="1b2ae-122">Requirement</span></span> | <span data-ttu-id="1b2ae-123">值</span><span class="sxs-lookup"><span data-stu-id="1b2ae-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b2ae-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b2ae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1b2ae-125">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="1b2ae-125">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="1b2ae-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b2ae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1b2ae-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b2ae-127">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="1b2ae-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1b2ae-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="1b2ae-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b2ae-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1b2ae-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1b2ae-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b2ae-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b2ae-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1b2ae-132">IID</span><span class="sxs-lookup"><span data-stu-id="1b2ae-132">IID</span></span><br/>                      | <span data-ttu-id="1b2ae-133">IID \_ IMsRdpDriveV2 定義為3e05417c-2721-4008-9d80-4edf1539c817</span><span class="sxs-lookup"><span data-stu-id="1b2ae-133">IID\_IMsRdpDriveV2 is defined as 3e05417c-2721-4008-9d80-4edf1539c817</span></span><br/>       |



 

 





