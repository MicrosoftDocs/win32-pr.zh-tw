---
title: Win32_RDMSDesktopAssignment 類別的 RemoveDesktopAssignment 方法
description: 移除桌面指派。
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- RemoveDesktopAssignment 方法遠端桌面服務
- RemoveDesktopAssignment 方法遠端桌面服務，Win32_RDMSDesktopAssignment 類別
- Win32_RDMSDesktopAssignment 類別遠端桌面服務，RemoveDesktopAssignment 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965118"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="fff0b-106">Win32 RDMSDesktopAssignment 類別的 RemoveDesktopAssignment 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fff0b-106">RemoveDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="fff0b-107">移除桌面指派</span><span class="sxs-lookup"><span data-stu-id="fff0b-107">Removes a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="fff0b-108">語法</span><span class="sxs-lookup"><span data-stu-id="fff0b-108">Syntax</span></span>


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="fff0b-109">參數</span><span class="sxs-lookup"><span data-stu-id="fff0b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fff0b-110">*CollectionAlias* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff0b-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff0b-111">集合別名。</span><span class="sxs-lookup"><span data-stu-id="fff0b-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="fff0b-112">*DesktopName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff0b-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff0b-113">桌面的名稱。</span><span class="sxs-lookup"><span data-stu-id="fff0b-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="fff0b-114">*UserDomain* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff0b-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff0b-115">使用者帳戶功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="fff0b-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="fff0b-116">使用者 *名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fff0b-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fff0b-117">使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fff0b-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fff0b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fff0b-118">Requirements</span></span>



| <span data-ttu-id="fff0b-119">需求</span><span class="sxs-lookup"><span data-stu-id="fff0b-119">Requirement</span></span> | <span data-ttu-id="fff0b-120">值</span><span class="sxs-lookup"><span data-stu-id="fff0b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fff0b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fff0b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fff0b-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="fff0b-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fff0b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fff0b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fff0b-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fff0b-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="fff0b-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="fff0b-125">Namespace</span></span><br/>                | <span data-ttu-id="fff0b-126">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="fff0b-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fff0b-127">MOF</span><span class="sxs-lookup"><span data-stu-id="fff0b-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fff0b-128"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="fff0b-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fff0b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fff0b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fff0b-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fff0b-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fff0b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fff0b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff0b-132">**Win32 \_ RDMSDesktopAssignment**</span><span class="sxs-lookup"><span data-stu-id="fff0b-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





