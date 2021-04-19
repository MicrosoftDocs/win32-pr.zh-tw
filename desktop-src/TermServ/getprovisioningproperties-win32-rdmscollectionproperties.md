---
title: Win32_RDMSCollectionProperties 類別的 GetProvisioningProperties 方法
description: 抓取虛擬桌面集合的布建屬性。
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- GetProvisioningProperties 方法遠端桌面服務
- GetProvisioningProperties 方法遠端桌面服務，Win32_RDMSCollectionProperties 類別
- Win32_RDMSCollectionProperties 類別遠端桌面服務，GetProvisioningProperties 方法
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966327"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a><span data-ttu-id="f6812-106">Win32 RDMSCollectionProperties 類別的 GetProvisioningProperties 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f6812-106">GetProvisioningProperties method of the Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="f6812-107">抓取虛擬桌面集合的布建屬性。</span><span class="sxs-lookup"><span data-stu-id="f6812-107">Retrieves the provisioning properties of the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6812-108">語法</span><span class="sxs-lookup"><span data-stu-id="f6812-108">Syntax</span></span>


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a><span data-ttu-id="f6812-109">參數</span><span class="sxs-lookup"><span data-stu-id="f6812-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6812-110">*PoolVhdType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-110">*PoolVhdType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-111">在集合中指定虛擬機器集區 (虛擬硬碟) 格式的 VHD。</span><span class="sxs-lookup"><span data-stu-id="f6812-111">Specifies the VHD (virtual hard disk) format of the virtual machine pool in the collection.</span></span>

<dt>

<span data-ttu-id="f6812-112">複製</span><span class="sxs-lookup"><span data-stu-id="f6812-112">Clone</span></span>
</dt> <dd>

<span data-ttu-id="f6812-113">複製的 VHD。</span><span class="sxs-lookup"><span data-stu-id="f6812-113">A cloned VHD.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-114">DiffDisk</span><span class="sxs-lookup"><span data-stu-id="f6812-114">DiffDisk</span></span>
</dt> <dd>

<span data-ttu-id="f6812-115">差異 VHD。</span><span class="sxs-lookup"><span data-stu-id="f6812-115">A differencing VHD.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f6812-116">*MasterVmLocation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-116">*MasterVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-117">接收主要 VM 映射的路徑。</span><span class="sxs-lookup"><span data-stu-id="f6812-117">Receives the path to the master VM image.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-118">*NamePrefix* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-118">*NamePrefix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-119">接收要附加至虛擬機器名稱開頭的名稱前置詞。</span><span class="sxs-lookup"><span data-stu-id="f6812-119">Receives the name prefix to append to the beginning of virtual machine names.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-120">*NameStartIndex* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-120">*NameStartIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-121">開始索引。</span><span class="sxs-lookup"><span data-stu-id="f6812-121">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-122">*LocalVmLocation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-122">*LocalVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-123">接收 Hyper-v 伺服器上虛擬機器的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="f6812-123">Receives the local path to the virtual machines on the Hyper-V servers.</span></span> <span data-ttu-id="f6812-124">如果此參數設定為 **Null** 或為空白，則會使用預設的虛擬機器目錄。</span><span class="sxs-lookup"><span data-stu-id="f6812-124">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-125">*LocalGoldVmLocation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-125">*LocalGoldVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-126">當 *PoolVhdTpe* 參數設定為 "DiffDisk" 時，接收黃金 VHD 映射的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="f6812-126">Receives the local path to the golden VHD image when the *PoolVhdTpe* parameter is set to "DiffDisk".</span></span> <span data-ttu-id="f6812-127">如果此參數設定為 **Null** 或為空白，則會使用預設的虛擬機器目錄。</span><span class="sxs-lookup"><span data-stu-id="f6812-127">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-128">*RunFromSMB* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-128">*RunFromSMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-129">接收值，指出是否要從伺服器訊息區 (SMB) 共用執行集合。</span><span class="sxs-lookup"><span data-stu-id="f6812-129">Receives a value that indicates whether to run the collection from an Server Message Block (SMB) share.</span></span> <span data-ttu-id="f6812-130">**TRUE** 表示從 SBM 共用執行虛擬機器;相反 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f6812-130">**TRUE** to run the virtual machines from an SBM share; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-131">*SMBLocation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-131">*SMBLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-132">如果已啟用 SMB 共用，則會接收 SMB 共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="f6812-132">Receives the path to the SMB share if SMB sharing is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-133">*SMBStreaming* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-133">*SMBStreaming* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-134">接收值，指出是否已啟用 SMB 串流。</span><span class="sxs-lookup"><span data-stu-id="f6812-134">Receives a value that indicates whether SMB streaming is enabled.</span></span> <span data-ttu-id="f6812-135">如果已啟用 SMB 共用，則 **為 TRUE** ;相反 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f6812-135">**TRUE** if SMB sharing is enabled; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-136">*VmDomain* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-136">*VmDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-137">接收集合中虛擬機器的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="f6812-137">Receives the domain name of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-138">*VmOU* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-138">*VmOU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-139">接收集合中虛擬機器的 Active Directory 組織單位 (OU) 。</span><span class="sxs-lookup"><span data-stu-id="f6812-139">Receives the Active Directory organization unit (OU) of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="f6812-140">*ProductKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6812-140">*ProductKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6812-141">接收集合中虛擬機器的作業系統產品金鑰。</span><span class="sxs-lookup"><span data-stu-id="f6812-141">Receives the OS product keys for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6812-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6812-142">Return value</span></span>

<span data-ttu-id="f6812-143">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f6812-143">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6812-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6812-144">Requirements</span></span>



| <span data-ttu-id="f6812-145">需求</span><span class="sxs-lookup"><span data-stu-id="f6812-145">Requirement</span></span> | <span data-ttu-id="f6812-146">值</span><span class="sxs-lookup"><span data-stu-id="f6812-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6812-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6812-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f6812-148">都不支援</span><span class="sxs-lookup"><span data-stu-id="f6812-148">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f6812-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6812-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f6812-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6812-150">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f6812-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="f6812-151">Namespace</span></span><br/>                | <span data-ttu-id="f6812-152">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="f6812-152">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f6812-153">MOF</span><span class="sxs-lookup"><span data-stu-id="f6812-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6812-154"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6812-154"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6812-155">DLL</span><span class="sxs-lookup"><span data-stu-id="f6812-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6812-156"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6812-156"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f6812-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6812-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6812-158">**Win32 \_ RDMSCollectionProperties**</span><span class="sxs-lookup"><span data-stu-id="f6812-158">**Win32\_RDMSCollectionProperties**</span></span>](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





