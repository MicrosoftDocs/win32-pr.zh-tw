---
title: ITsSbTargetEx 介面
description: 公開屬性，這些屬性會儲存目標的設定和狀態資訊。
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- ITsSbTargetEx 介面遠端桌面服務
- ITsSbTargetEx 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d53d126d9419f87d91b027b0d69847f67de84be6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935037"
---
# <a name="itssbtargetex-interface"></a><span data-ttu-id="57f44-105">ITsSbTargetEx 介面</span><span class="sxs-lookup"><span data-stu-id="57f44-105">ITsSbTargetEx interface</span></span>

<span data-ttu-id="57f44-106">公開屬性，這些屬性會儲存目標的設定和狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="57f44-106">Exposes properties that store configuration and state information about a target.</span></span>

<span data-ttu-id="57f44-107">這個介面僅適用于已安裝 [KB3091411](https://support.microsoft.com/kb/3091411) 的 Windows Server 2012 R2。</span><span class="sxs-lookup"><span data-stu-id="57f44-107">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="57f44-108">從 Windows Server 2016 開始，可以使用 [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)介面的 [**TargetLoad**](itssbtarget-targetload.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="57f44-108">The [**TargetLoad**](itssbtarget-targetload.md) property of the [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) interface is available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="57f44-109">成員</span><span class="sxs-lookup"><span data-stu-id="57f44-109">Members</span></span>

<span data-ttu-id="57f44-110">**ITsSbTargetEx** 介面繼承自 [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)。</span><span class="sxs-lookup"><span data-stu-id="57f44-110">The **ITsSbTargetEx** interface inherits from [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span></span> <span data-ttu-id="57f44-111">**ITsSbTargetEx** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="57f44-111">**ITsSbTargetEx** also has these types of members:</span></span>

-   [<span data-ttu-id="57f44-112">屬性</span><span class="sxs-lookup"><span data-stu-id="57f44-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57f44-113">屬性</span><span class="sxs-lookup"><span data-stu-id="57f44-113">Properties</span></span>

<span data-ttu-id="57f44-114">**ITsSbTargetEx** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="57f44-114">The **ITsSbTargetEx** interface has these properties.</span></span>



| <span data-ttu-id="57f44-115">屬性</span><span class="sxs-lookup"><span data-stu-id="57f44-115">Property</span></span>                                                                      | <span data-ttu-id="57f44-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="57f44-116">Access type</span></span>           | <span data-ttu-id="57f44-117">Description</span><span class="sxs-lookup"><span data-stu-id="57f44-117">Description</span></span>                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57f44-118">**EnvironmentName**</span><span class="sxs-lookup"><span data-stu-id="57f44-118">**EnvironmentName**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | <span data-ttu-id="57f44-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="57f44-119">Read/write</span></span><br/> | <span data-ttu-id="57f44-120">抓取或指定與目標相關聯之環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="57f44-120">Retrieves or specifies the name of the environment associated with the target.</span></span><br/> |
| [<span data-ttu-id="57f44-121">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="57f44-121">**FarmName**</span></span>](itssbtarget-farmname.md)<br/>                           | <span data-ttu-id="57f44-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="57f44-122">Read/write</span></span><br/> | <span data-ttu-id="57f44-123">指定或抓取這個目標所聯結的伺服器陣列名稱。</span><span class="sxs-lookup"><span data-stu-id="57f44-123">Specifies or retrieves the name of the farm to which this target is joined.</span></span><br/>    |
| [<span data-ttu-id="57f44-124">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="57f44-124">**IpAddresses**</span></span>](itssbtarget-ipaddresses.md)<br/>                     | <span data-ttu-id="57f44-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="57f44-125">Read/write</span></span><br/> | <span data-ttu-id="57f44-126">捕獲或指定目標的外部 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="57f44-126">Retrieves or specifies the external IP addresses of the target.</span></span><br/>                |
| [<span data-ttu-id="57f44-127">**NumPendingConnections**</span><span class="sxs-lookup"><span data-stu-id="57f44-127">**NumPendingConnections**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | <span data-ttu-id="57f44-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="57f44-128">Read-only</span></span><br/>  | <span data-ttu-id="57f44-129">抓取目標的暫止使用者連接數目。</span><span class="sxs-lookup"><span data-stu-id="57f44-129">Retrieves the number of pending user connections for the target.</span></span><br/>               |
| [<span data-ttu-id="57f44-130">**NumSessions**</span><span class="sxs-lookup"><span data-stu-id="57f44-130">**NumSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | <span data-ttu-id="57f44-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="57f44-131">Read-only</span></span><br/>  | <span data-ttu-id="57f44-132">抓取 broker 針對目標所維護的會話數目。</span><span class="sxs-lookup"><span data-stu-id="57f44-132">Retrieves the number of sessions maintained by broker for the target.</span></span><br/>          |
| [<span data-ttu-id="57f44-133">**TargetFQDN**</span><span class="sxs-lookup"><span data-stu-id="57f44-133">**TargetFQDN**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | <span data-ttu-id="57f44-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="57f44-134">Read/write</span></span><br/> | <span data-ttu-id="57f44-135">指定或抓取目標的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="57f44-135">Specifies or retrieves the fully qualified domain name of the target.</span></span><br/>          |
| <span data-ttu-id="57f44-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="57f44-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span></span><br/>                     | <span data-ttu-id="57f44-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="57f44-137">Read-only</span></span><br/>  | <span data-ttu-id="57f44-138">抓取目標的相對負載。</span><span class="sxs-lookup"><span data-stu-id="57f44-138">Retrieves the relative load on a target.</span></span><br/>                                       |
| [<span data-ttu-id="57f44-139">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="57f44-139">**TargetName**</span></span>](itssbtarget-targetname.md)<br/>                       | <span data-ttu-id="57f44-140">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="57f44-140">Read/write</span></span><br/> | <span data-ttu-id="57f44-141">指定或抓取目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="57f44-141">Specifies or retrieves the name of the target.</span></span><br/>                                 |
| [<span data-ttu-id="57f44-142">**TargetNetbios**</span><span class="sxs-lookup"><span data-stu-id="57f44-142">**TargetNetbios**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | <span data-ttu-id="57f44-143">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="57f44-143">Read/write</span></span><br/> | <span data-ttu-id="57f44-144">指定或抓取目標的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="57f44-144">Specifies or retrieves the NetBIOS name of the target.</span></span><br/>                         |
| [<span data-ttu-id="57f44-145">**TargetPropertySet**</span><span class="sxs-lookup"><span data-stu-id="57f44-145">**TargetPropertySet**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | <span data-ttu-id="57f44-146">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="57f44-146">Read/write</span></span><br/> | <span data-ttu-id="57f44-147">指定或抓取目標的屬性集。</span><span class="sxs-lookup"><span data-stu-id="57f44-147">Specifies or retrieves the property set for the target.</span></span><br/>                        |
| [<span data-ttu-id="57f44-148">**TargetState**</span><span class="sxs-lookup"><span data-stu-id="57f44-148">**TargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | <span data-ttu-id="57f44-149">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="57f44-149">Read/write</span></span><br/> | <span data-ttu-id="57f44-150">指定或抓取目標狀態。</span><span class="sxs-lookup"><span data-stu-id="57f44-150">Specifies or retrieves the target state.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="57f44-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="57f44-151">Requirements</span></span>



| <span data-ttu-id="57f44-152">需求</span><span class="sxs-lookup"><span data-stu-id="57f44-152">Requirement</span></span> | <span data-ttu-id="57f44-153">值</span><span class="sxs-lookup"><span data-stu-id="57f44-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57f44-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57f44-154">Minimum supported client</span></span><br/> | <span data-ttu-id="57f44-155">都不支援</span><span class="sxs-lookup"><span data-stu-id="57f44-155">None supported</span></span><br/>                                                        |
| <span data-ttu-id="57f44-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57f44-156">Minimum supported server</span></span><br/> | <span data-ttu-id="57f44-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="57f44-157">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="57f44-158">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="57f44-158">End of server support</span></span><br/>    | <span data-ttu-id="57f44-159">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="57f44-159">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="57f44-160">IID</span><span class="sxs-lookup"><span data-stu-id="57f44-160">IID</span></span><br/>                      | <span data-ttu-id="57f44-161">IID \_ ITsSbTargetEx 定義為74f99987-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="57f44-161">IID\_ITsSbTargetEx is defined as 74f99987-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57f44-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57f44-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f44-163">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="57f44-163">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="57f44-164">遠端桌面虛擬化介面</span><span class="sxs-lookup"><span data-stu-id="57f44-164">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

