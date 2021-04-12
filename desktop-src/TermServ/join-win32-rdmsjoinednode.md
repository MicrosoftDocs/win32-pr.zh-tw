---
title: Win32_RDMSJoinedNode 類別的 Join 方法
description: 將節點新增至遠端桌面管理服務 (RDM) 。
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Join 方法遠端桌面服務
- Join 方法遠端桌面服務，Win32_RDMSJoinedNode 類別
- Win32_RDMSJoinedNode 類別遠端桌面服務，Join 方法
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384154"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="7a249-106">Win32 RDMSJoinedNode 類別的 Join 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7a249-106">Join method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="7a249-107">將節點新增至遠端桌面管理服務 (RDM) 。</span><span class="sxs-lookup"><span data-stu-id="7a249-107">Adds a node to Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a249-108">語法</span><span class="sxs-lookup"><span data-stu-id="7a249-108">Syntax</span></span>


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a><span data-ttu-id="7a249-109">參數</span><span class="sxs-lookup"><span data-stu-id="7a249-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a249-110">*NodeFQDN* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a249-110">*NodeFQDN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a249-111">節點的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="7a249-111">The fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="7a249-112">*NodeSID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a249-112">*NodeSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a249-113">節點 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a249-113">The security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a249-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a249-114">Return value</span></span>

<span data-ttu-id="7a249-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7a249-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a249-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a249-116">Requirements</span></span>



| <span data-ttu-id="7a249-117">需求</span><span class="sxs-lookup"><span data-stu-id="7a249-117">Requirement</span></span> | <span data-ttu-id="7a249-118">值</span><span class="sxs-lookup"><span data-stu-id="7a249-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a249-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a249-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7a249-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="7a249-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7a249-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a249-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7a249-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a249-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7a249-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="7a249-123">Namespace</span></span><br/>                | <span data-ttu-id="7a249-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="7a249-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7a249-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7a249-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a249-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a249-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a249-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7a249-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a249-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a249-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7a249-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a249-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a249-130">**Win32 \_ RDMSJoinedNode**</span><span class="sxs-lookup"><span data-stu-id="7a249-130">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





