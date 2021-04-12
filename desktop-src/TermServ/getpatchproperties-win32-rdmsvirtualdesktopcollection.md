---
title: Win32_RDMSVirtualDesktopCollection 類別的 GetPatchProperties 方法
description: 抓取虛擬桌面集合中虛擬機器的軟體更新布建作業屬性。
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- GetPatchProperties 方法遠端桌面服務
- GetPatchProperties 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，GetPatchProperties 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508847"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="fbf58-106">Win32 RDMSVirtualDesktopCollection 類別的 GetPatchProperties 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fbf58-106">GetPatchProperties method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="fbf58-107">抓取虛擬桌面集合中虛擬機器的軟體更新布建作業屬性。</span><span class="sxs-lookup"><span data-stu-id="fbf58-107">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf58-108">語法</span><span class="sxs-lookup"><span data-stu-id="fbf58-108">Syntax</span></span>


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a><span data-ttu-id="fbf58-109">參數</span><span class="sxs-lookup"><span data-stu-id="fbf58-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf58-110">*StartTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fbf58-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf58-111">安裝更新的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fbf58-111">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="fbf58-112">*ForceLogOffTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fbf58-112">*ForceLogOffTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf58-113">系統將登出虛擬機器使用者的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fbf58-113">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="fbf58-114">*JobGuid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fbf58-114">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf58-115">可唯一識別布建作業的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="fbf58-115">A **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="fbf58-116">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fbf58-116">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf58-117">布建作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="fbf58-117">The state of the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf58-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbf58-118">Return value</span></span>

<span data-ttu-id="fbf58-119">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fbf58-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf58-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbf58-120">Requirements</span></span>



| <span data-ttu-id="fbf58-121">需求</span><span class="sxs-lookup"><span data-stu-id="fbf58-121">Requirement</span></span> | <span data-ttu-id="fbf58-122">值</span><span class="sxs-lookup"><span data-stu-id="fbf58-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf58-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbf58-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf58-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="fbf58-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fbf58-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbf58-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf58-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fbf58-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fbf58-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="fbf58-127">Namespace</span></span><br/>                | <span data-ttu-id="fbf58-128">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="fbf58-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fbf58-129">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf58-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf58-130"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbf58-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbf58-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf58-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf58-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf58-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fbf58-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbf58-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf58-134">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="fbf58-134">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





