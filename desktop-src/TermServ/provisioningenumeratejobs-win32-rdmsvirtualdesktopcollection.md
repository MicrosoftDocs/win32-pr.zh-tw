---
title: Win32_RDMSVirtualDesktopCollection 類別的 ProvisioningEnumerateJobs 方法
description: 列舉此服務的虛擬桌面布建作業。
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- ProvisioningEnumerateJobs 方法遠端桌面服務
- ProvisioningEnumerateJobs 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，ProvisioningEnumerateJobs 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509388"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="af94c-106">Win32 RDMSVirtualDesktopCollection 類別的 ProvisioningEnumerateJobs 方法 \_</span><span class="sxs-lookup"><span data-stu-id="af94c-106">ProvisioningEnumerateJobs method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="af94c-107">列舉此服務的虛擬桌面布建作業。</span><span class="sxs-lookup"><span data-stu-id="af94c-107">Enumerates virtual desktop provisioning jobs for this service.</span></span>

## <a name="syntax"></a><span data-ttu-id="af94c-108">語法</span><span class="sxs-lookup"><span data-stu-id="af94c-108">Syntax</span></span>


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a><span data-ttu-id="af94c-109">參數</span><span class="sxs-lookup"><span data-stu-id="af94c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af94c-110">*JobType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af94c-110">*JobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af94c-111">整數，指定要列舉的作業類型。</span><span class="sxs-lookup"><span data-stu-id="af94c-111">An integer that specifies the type of job to enumerate.</span></span>

<span data-ttu-id="af94c-112">這個參數可以設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="af94c-112">This parameter can be set to one of the following values:</span></span>

<dt>

<span data-ttu-id="af94c-113">0</span><span class="sxs-lookup"><span data-stu-id="af94c-113">0</span></span>
</dt> <dd>

<span data-ttu-id="af94c-114">正在執行工作</span><span class="sxs-lookup"><span data-stu-id="af94c-114">Running jobs</span></span>

</dd> <dt>

<span data-ttu-id="af94c-115">1</span><span class="sxs-lookup"><span data-stu-id="af94c-115">1</span></span>
</dt> <dd>

<span data-ttu-id="af94c-116">已完成的工作</span><span class="sxs-lookup"><span data-stu-id="af94c-116">Completed jobs</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="af94c-117">*CollectionAlias* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af94c-117">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af94c-118">要列舉之虛擬桌面集合的別名。</span><span class="sxs-lookup"><span data-stu-id="af94c-118">The alias of the virtual desktop collection to enumerate.</span></span> <span data-ttu-id="af94c-119">此參數的預設值為 FALSE，這會指定要列舉所有正在執行的作業。</span><span class="sxs-lookup"><span data-stu-id="af94c-119">The default value for this parameter is FALSE, which specifies that all running jobs are to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="af94c-120">*JobGuids* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="af94c-120">*JobGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af94c-121">陣列，其中包含要列舉之布建作業的 **guid** 。</span><span class="sxs-lookup"><span data-stu-id="af94c-121">An array that contains the **GUIDs** of provisioning jobs to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af94c-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="af94c-122">Return value</span></span>

<span data-ttu-id="af94c-123">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="af94c-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="af94c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="af94c-124">Requirements</span></span>



| <span data-ttu-id="af94c-125">需求</span><span class="sxs-lookup"><span data-stu-id="af94c-125">Requirement</span></span> | <span data-ttu-id="af94c-126">值</span><span class="sxs-lookup"><span data-stu-id="af94c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="af94c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af94c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="af94c-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="af94c-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="af94c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af94c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="af94c-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af94c-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="af94c-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="af94c-131">Namespace</span></span><br/>                | <span data-ttu-id="af94c-132">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="af94c-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="af94c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="af94c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af94c-134"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="af94c-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="af94c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="af94c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af94c-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af94c-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="af94c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af94c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af94c-138">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="af94c-138">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





