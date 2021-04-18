---
title: Win32_RDMSJoinedNode 類別的退出方法
description: 從遠端桌面管理服務 (RDMS) 移除節點。
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- 退出方法遠端桌面服務
- 退出方法遠端桌面服務，Win32_RDMSJoinedNode 類別
- Win32_RDMSJoinedNode 類別遠端桌面服務、退出方法
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Unjoin
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234f7cc3ad8a797fff51661528f4545ed9fea3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965726"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="a2a30-106">Win32 RDMSJoinedNode 類別的退出方法 \_</span><span class="sxs-lookup"><span data-stu-id="a2a30-106">Unjoin method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="a2a30-107">從遠端桌面管理服務 (RDMS) 移除節點。</span><span class="sxs-lookup"><span data-stu-id="a2a30-107">Removes a node from Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a30-108">語法</span><span class="sxs-lookup"><span data-stu-id="a2a30-108">Syntax</span></span>


```mof
uint32 Unjoin();
```



## <a name="parameters"></a><span data-ttu-id="a2a30-109">參數</span><span class="sxs-lookup"><span data-stu-id="a2a30-109">Parameters</span></span>

<span data-ttu-id="a2a30-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a2a30-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2a30-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2a30-111">Return value</span></span>

<span data-ttu-id="a2a30-112">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a2a30-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a30-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2a30-113">Requirements</span></span>



| <span data-ttu-id="a2a30-114">需求</span><span class="sxs-lookup"><span data-stu-id="a2a30-114">Requirement</span></span> | <span data-ttu-id="a2a30-115">值</span><span class="sxs-lookup"><span data-stu-id="a2a30-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a30-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2a30-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a2a30-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="a2a30-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a2a30-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2a30-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a2a30-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a2a30-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a2a30-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="a2a30-120">Namespace</span></span><br/>                | <span data-ttu-id="a2a30-121">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="a2a30-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a2a30-122">MOF</span><span class="sxs-lookup"><span data-stu-id="a2a30-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2a30-123"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2a30-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2a30-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a2a30-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2a30-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2a30-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a2a30-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2a30-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a30-127">**Win32 \_ RDMSJoinedNode**</span><span class="sxs-lookup"><span data-stu-id="a2a30-127">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





