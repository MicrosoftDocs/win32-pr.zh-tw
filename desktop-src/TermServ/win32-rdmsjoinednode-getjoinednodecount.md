---
title: Win32_RDMSJoinedNode 類別的 GetJoinedNodeCount 方法
description: 取得已安裝指定角色的伺服器數目。
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- GetJoinedNodeCount 方法遠端桌面服務
- GetJoinedNodeCount 方法遠端桌面服務，Win32_RDMSJoinedNode 類別
- Win32_RDMSJoinedNode 類別遠端桌面服務，GetJoinedNodeCount 方法
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966305"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="f0c41-106">Win32 RDMSJoinedNode 類別的 GetJoinedNodeCount 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f0c41-106">GetJoinedNodeCount method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="f0c41-107">取得已安裝指定角色的伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="f0c41-107">Get number of servers that have the specified roles installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c41-108">語法</span><span class="sxs-lookup"><span data-stu-id="f0c41-108">Syntax</span></span>


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a><span data-ttu-id="f0c41-109">參數</span><span class="sxs-lookup"><span data-stu-id="f0c41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c41-110">*roleType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0c41-110">*roleType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c41-111">指定角色類型的位位。</span><span class="sxs-lookup"><span data-stu-id="f0c41-111">A bitfield that specifies the role types.</span></span>

<dt>

<span data-ttu-id="f0c41-112">0</span><span class="sxs-lookup"><span data-stu-id="f0c41-112">0</span></span>
</dt> <dd>

<span data-ttu-id="f0c41-113">全部</span><span class="sxs-lookup"><span data-stu-id="f0c41-113">All</span></span>

</dd> <dt>

<span data-ttu-id="f0c41-114">1</span><span class="sxs-lookup"><span data-stu-id="f0c41-114">1</span></span>
</dt> <dd>

<span data-ttu-id="f0c41-115">遠端桌面連線代理人 (RDCB) </span><span class="sxs-lookup"><span data-stu-id="f0c41-115">Remote Desktop Connection Broker (RDCB)</span></span>

</dd> <dt>

<span data-ttu-id="f0c41-116">2</span><span class="sxs-lookup"><span data-stu-id="f0c41-116">2</span></span>
</dt> <dd>

<span data-ttu-id="f0c41-117">遠端桌面工作階段主機 (RDSH) </span><span class="sxs-lookup"><span data-stu-id="f0c41-117">Remote Desktop Session Host (RDSH)</span></span>

</dd> <dt>

<span data-ttu-id="f0c41-118">4</span><span class="sxs-lookup"><span data-stu-id="f0c41-118">4</span></span>
</dt> <dd>

<span data-ttu-id="f0c41-119">遠端桌面虛擬化主機 (RDVH) </span><span class="sxs-lookup"><span data-stu-id="f0c41-119">Remote Desktop Virtualization Host (RDVH)</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f0c41-120">*計數* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f0c41-120">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c41-121">成功時，會傳回已安裝指定角色的伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="f0c41-121">On success, returns the number of servers with the specified roles installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c41-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0c41-122">Return value</span></span>

<span data-ttu-id="f0c41-123">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f0c41-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c41-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0c41-124">Requirements</span></span>



| <span data-ttu-id="f0c41-125">需求</span><span class="sxs-lookup"><span data-stu-id="f0c41-125">Requirement</span></span> | <span data-ttu-id="f0c41-126">值</span><span class="sxs-lookup"><span data-stu-id="f0c41-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c41-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0c41-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c41-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="f0c41-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f0c41-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0c41-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c41-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f0c41-130">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="f0c41-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="f0c41-131">Namespace</span></span><br/>                | <span data-ttu-id="f0c41-132">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="f0c41-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f0c41-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f0c41-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0c41-134"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0c41-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0c41-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f0c41-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0c41-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0c41-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f0c41-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0c41-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c41-138">**Win32 \_ RDMSJoinedNode**</span><span class="sxs-lookup"><span data-stu-id="f0c41-138">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





