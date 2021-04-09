---
title: IMsRdpDrive 介面
description: 包含磁片磁碟機物件的相關資訊。
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- IMsRdpDrive 介面遠端桌面服務
- IMsRdpDrive 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685530"
---
# <a name="imsrdpdrive-interface"></a><span data-ttu-id="5aed2-105">IMsRdpDrive 介面</span><span class="sxs-lookup"><span data-stu-id="5aed2-105">IMsRdpDrive interface</span></span>

<span data-ttu-id="5aed2-106">包含磁片磁碟機物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5aed2-106">Contains information about a drive object.</span></span>

## <a name="members"></a><span data-ttu-id="5aed2-107">成員</span><span class="sxs-lookup"><span data-stu-id="5aed2-107">Members</span></span>

<span data-ttu-id="5aed2-108">**IMsRdpDrive** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="5aed2-108">The **IMsRdpDrive** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5aed2-109">**IMsRdpDrive** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5aed2-109">**IMsRdpDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="5aed2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5aed2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5aed2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5aed2-111">Properties</span></span>

<span data-ttu-id="5aed2-112">**IMsRdpDrive** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5aed2-112">The **IMsRdpDrive** interface has these properties.</span></span>



| <span data-ttu-id="5aed2-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5aed2-113">Property</span></span>                                                            | <span data-ttu-id="5aed2-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="5aed2-114">Access type</span></span>           | <span data-ttu-id="5aed2-115">Description</span><span class="sxs-lookup"><span data-stu-id="5aed2-115">Description</span></span>                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="5aed2-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="5aed2-116">**Name**</span></span>](imsrdpdrive-name.md)<br/>                         | <span data-ttu-id="5aed2-117">唯讀</span><span class="sxs-lookup"><span data-stu-id="5aed2-117">Read-only</span></span><br/>  | <span data-ttu-id="5aed2-118">抓取磁片磁碟機的名稱。</span><span class="sxs-lookup"><span data-stu-id="5aed2-118">Retrieves the name of the drive.</span></span><br/>              |
| [<span data-ttu-id="5aed2-119">**RedirectionState**</span><span class="sxs-lookup"><span data-stu-id="5aed2-119">**RedirectionState**</span></span>](imsrdpdrive-redirectionstate.md)<br/> | <span data-ttu-id="5aed2-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5aed2-120">Read/write</span></span><br/> | <span data-ttu-id="5aed2-121">指出磁片磁碟機的重新導向狀態。</span><span class="sxs-lookup"><span data-stu-id="5aed2-121">Indicates the redirection state of the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5aed2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5aed2-122">Requirements</span></span>



| <span data-ttu-id="5aed2-123">需求</span><span class="sxs-lookup"><span data-stu-id="5aed2-123">Requirement</span></span> | <span data-ttu-id="5aed2-124">值</span><span class="sxs-lookup"><span data-stu-id="5aed2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aed2-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5aed2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5aed2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5aed2-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5aed2-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5aed2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5aed2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5aed2-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5aed2-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5aed2-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="5aed2-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aed2-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5aed2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5aed2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aed2-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aed2-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5aed2-133">IID</span><span class="sxs-lookup"><span data-stu-id="5aed2-133">IID</span></span><br/>                      | <span data-ttu-id="5aed2-134">IID \_ IMsRdpDrive 定義為 d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="5aed2-134">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="5aed2-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5aed2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aed2-136">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="5aed2-136">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="5aed2-137">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="5aed2-137">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

