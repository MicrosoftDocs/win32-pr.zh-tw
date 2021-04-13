---
title: Win32_RDMSJoinedNode 類別
description: 代表由遠端桌面管理服務 (RDMS) 管理的伺服器節點。
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Win32_RDMSJoinedNode 類別遠端桌面服務
- Win32_RDMSJoinedNode 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383962"
---
# <a name="win32_rdmsjoinednode-class"></a><span data-ttu-id="76672-105">Win32 \_ RDMSJoinedNode 類別</span><span class="sxs-lookup"><span data-stu-id="76672-105">Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="76672-106">代表由遠端桌面管理服務 (RDMS) 管理的伺服器節點。</span><span class="sxs-lookup"><span data-stu-id="76672-106">Represents a server node that is managed by Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="76672-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="76672-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="76672-108">語法</span><span class="sxs-lookup"><span data-stu-id="76672-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a><span data-ttu-id="76672-109">成員</span><span class="sxs-lookup"><span data-stu-id="76672-109">Members</span></span>

<span data-ttu-id="76672-110">**Win32 \_ RDMSJoinedNode** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="76672-110">The **Win32\_RDMSJoinedNode** class has these types of members:</span></span>

-   [<span data-ttu-id="76672-111">方法</span><span class="sxs-lookup"><span data-stu-id="76672-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="76672-112">屬性</span><span class="sxs-lookup"><span data-stu-id="76672-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="76672-113">方法</span><span class="sxs-lookup"><span data-stu-id="76672-113">Methods</span></span>

<span data-ttu-id="76672-114">**Win32 \_ RDMSJoinedNode** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="76672-114">The **Win32\_RDMSJoinedNode** class has these methods.</span></span>



| <span data-ttu-id="76672-115">方法</span><span class="sxs-lookup"><span data-stu-id="76672-115">Method</span></span>                                                                | <span data-ttu-id="76672-116">描述</span><span class="sxs-lookup"><span data-stu-id="76672-116">Description</span></span>                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76672-117">**GetJoinedNodeCount**</span><span class="sxs-lookup"><span data-stu-id="76672-117">**GetJoinedNodeCount**</span></span>](win32-rdmsjoinednode-getjoinednodecount.md) | <span data-ttu-id="76672-118">**Windows server 2012 R2 和 Windows server 2012：** 此方法在 Windows Server 2016 之前無法使用。</span><span class="sxs-lookup"><span data-stu-id="76672-118">**Windows Server 2012 R2 and Windows Server 2012:** This method is unavailable prior to Windows Server 2016.</span></span><br/> <span data-ttu-id="76672-119">取得已安裝指定角色的伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="76672-119">Gets the number of servers that have the specified role installed.</span></span><br/> |
| [<span data-ttu-id="76672-120">**加入**</span><span class="sxs-lookup"><span data-stu-id="76672-120">**Join**</span></span>](join-win32-rdmsjoinednode.md)                             | <span data-ttu-id="76672-121">將節點新增至 RDM。</span><span class="sxs-lookup"><span data-stu-id="76672-121">Adds a node to RDMS.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="76672-122">**退出**</span><span class="sxs-lookup"><span data-stu-id="76672-122">**Unjoin**</span></span>](unjoin-win32-rdmsjoinednode.md)                         | <span data-ttu-id="76672-123">從 RDM 移除節點。</span><span class="sxs-lookup"><span data-stu-id="76672-123">Removes a node from RDMS.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="76672-124">屬性</span><span class="sxs-lookup"><span data-stu-id="76672-124">Properties</span></span>

<span data-ttu-id="76672-125">**Win32 \_ RDMSJoinedNode** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="76672-125">The **Win32\_RDMSJoinedNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76672-126">**FQDN**</span><span class="sxs-lookup"><span data-stu-id="76672-126">**FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76672-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76672-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="76672-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76672-129">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="76672-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="76672-130">取得節點的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="76672-130">Gets the fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="76672-131">**IsGatewayCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="76672-131">**IsGatewayCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-132">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="76672-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76672-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76672-134">取得和設定值，這個值會指出伺服器是否具有憑證，可執行遠端桌面閘道連線的驗證。</span><span class="sxs-lookup"><span data-stu-id="76672-134">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop gateway connections.</span></span> <span data-ttu-id="76672-135">如果已安裝憑證，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76672-135">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="76672-136">**IsPublishingCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="76672-136">**IsPublishingCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-137">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="76672-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76672-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76672-139">取得和設定值，這個值會指出伺服器是否具有憑證來簽署遠端桌面通訊協定發行檔案。</span><span class="sxs-lookup"><span data-stu-id="76672-139">Gets and sets a value that indicates whether the server has a certificate to sign Remote Desktop Protocol publishing files.</span></span> <span data-ttu-id="76672-140">如果已安裝憑證，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76672-140">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="76672-141">**IsRdcb**</span><span class="sxs-lookup"><span data-stu-id="76672-141">**IsRdcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="76672-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76672-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76672-144">取得和設定值，這個值會指出伺服器是否為遠端桌面連線代理人。</span><span class="sxs-lookup"><span data-stu-id="76672-144">Gets and sets a value that indicates whether the server is Remote Desktop Connection Broker.</span></span> <span data-ttu-id="76672-145">如果伺服器是遠端桌面連線代理人，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76672-145">**TRUE** if the server is a Remote Desktop Connection Broker; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="76672-146">**IsRdg**</span><span class="sxs-lookup"><span data-stu-id="76672-146">**IsRdg**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-147">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="76672-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76672-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76672-149">取得和設定值，這個值會指出伺服器是否為遠端桌面閘道伺服器。</span><span class="sxs-lookup"><span data-stu-id="76672-149">Gets and sets a value that indicates whether the server is Remote Desktop gateway server.</span></span> <span data-ttu-id="76672-150">如果伺服器是遠端桌面閘道伺服器，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76672-150">**TRUE** if the server is a Remote Desktop gateway server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="76672-151">**IsRdls**</span><span class="sxs-lookup"><span data-stu-id="76672-151">**IsRdls**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-152">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="76672-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76672-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76672-154">取得和設定值，這個值會指出伺服器是否為遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="76672-154">Gets and sets a value that indicates whether the server is Remote Desktop license server.</span></span> <span data-ttu-id="76672-155">如果伺服器是遠端桌面授權伺服器，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76672-155">**TRUE** if the server is a Remote Desktop license server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="76672-156">**IsRdsh**</span><span class="sxs-lookup"><span data-stu-id="76672-156">**IsRdsh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-157">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="76672-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76672-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76672-159">取得和設定值，這個值會指出伺服器是否為遠端桌面工作階段主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="76672-159">Gets and sets a value that indicates whether the server is Remote Desktop session host server.</span></span> <span data-ttu-id="76672-160">如果伺服器是遠端桌面工作階段主機伺服器，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76672-160">**TRUE** if the server is a Remote Desktop session host server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="76672-161">**IsRdvh**</span><span class="sxs-lookup"><span data-stu-id="76672-161">**IsRdvh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-162">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="76672-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76672-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76672-164">取得和設定值，這個值會指出伺服器是否為遠端桌面虛擬化主機。</span><span class="sxs-lookup"><span data-stu-id="76672-164">Gets and sets a value that indicates whether the server is Remote Desktop virtualization host.</span></span> <span data-ttu-id="76672-165">如果伺服器是遠端桌面虛擬化主機，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76672-165">**TRUE** if the server is a Remote Desktop virtualization host; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="76672-166">**IsRdwa**</span><span class="sxs-lookup"><span data-stu-id="76672-166">**IsRdwa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-167">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="76672-167">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76672-168">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-168">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76672-169">取得和設定值，這個值會指出伺服器是否為遠端桌面 web 存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="76672-169">Gets and sets a value that indicates whether the server is Remote Desktop web access server.</span></span> <span data-ttu-id="76672-170">如果伺服器是遠端桌面 Web 存取伺服器，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76672-170">**TRUE** if the server is a Remote Desktop Web Access server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="76672-171">**IsRedirectorCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="76672-171">**IsRedirectorCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-172">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="76672-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76672-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76672-174">取得和設定值，這個值會指出伺服器是否具有憑證來執行遠端桌面服務部署的驗證。</span><span class="sxs-lookup"><span data-stu-id="76672-174">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Services deployment.</span></span> <span data-ttu-id="76672-175">如果已安裝憑證，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76672-175">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="76672-176">**IsWebAccessCertificateInstalled**</span><span class="sxs-lookup"><span data-stu-id="76672-176">**IsWebAccessCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-177">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="76672-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76672-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="76672-179">取得和設定值，這個值會指出伺服器是否具有憑證，可執行遠端桌面 Web 存取的驗證。</span><span class="sxs-lookup"><span data-stu-id="76672-179">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Web Access.</span></span> <span data-ttu-id="76672-180">如果已安裝憑證，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="76672-180">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="76672-181">**OSVersion**</span><span class="sxs-lookup"><span data-stu-id="76672-181">**OSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76672-182">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="76672-183">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="76672-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="76672-184">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="76672-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="76672-185">取得和設定節點上的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="76672-185">Gets and sets the version of the operating systems on the node.</span></span>

</dd> <dt>

<span data-ttu-id="76672-186">**SID**</span><span class="sxs-lookup"><span data-stu-id="76672-186">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76672-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="76672-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76672-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="76672-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76672-189">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="76672-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="76672-190">取得節點 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="76672-190">Gets the security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76672-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="76672-191">Requirements</span></span>



| <span data-ttu-id="76672-192">需求</span><span class="sxs-lookup"><span data-stu-id="76672-192">Requirement</span></span> | <span data-ttu-id="76672-193">值</span><span class="sxs-lookup"><span data-stu-id="76672-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="76672-194">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76672-194">Minimum supported client</span></span><br/> | <span data-ttu-id="76672-195">都不支援</span><span class="sxs-lookup"><span data-stu-id="76672-195">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="76672-196">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76672-196">Minimum supported server</span></span><br/> | <span data-ttu-id="76672-197">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76672-197">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="76672-198">命名空間</span><span class="sxs-lookup"><span data-stu-id="76672-198">Namespace</span></span><br/>                | <span data-ttu-id="76672-199">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="76672-199">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="76672-200">MOF</span><span class="sxs-lookup"><span data-stu-id="76672-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76672-201"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="76672-201"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="76672-202">DLL</span><span class="sxs-lookup"><span data-stu-id="76672-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76672-203"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76672-203"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="76672-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76672-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76672-205">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="76672-205">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

