---
title: Win32_RDMSVirtualDesktop 類別的 GetVirtualDesktopAssignedToUser 方法
description: 抓取指派給指定使用者的虛擬桌面。
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- GetVirtualDesktopAssignedToUser 方法遠端桌面服務
- GetVirtualDesktopAssignedToUser 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，GetVirtualDesktopAssignedToUser 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcbbbed20b6b571e8867689ac901344af8e23b93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967951"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="755ee-106">Win32 RDMSVirtualDesktop 類別的 GetVirtualDesktopAssignedToUser 方法 \_</span><span class="sxs-lookup"><span data-stu-id="755ee-106">GetVirtualDesktopAssignedToUser method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="755ee-107">抓取指派給指定使用者的虛擬桌面。</span><span class="sxs-lookup"><span data-stu-id="755ee-107">Retrieves the virtual desktop that is assigned to the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="755ee-108">語法</span><span class="sxs-lookup"><span data-stu-id="755ee-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="755ee-109">參數</span><span class="sxs-lookup"><span data-stu-id="755ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="755ee-110">*CollectionAlias* \[在\]</span><span class="sxs-lookup"><span data-stu-id="755ee-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="755ee-111">包含虛擬桌面的虛擬桌面集合別名。</span><span class="sxs-lookup"><span data-stu-id="755ee-111">The alias of the virtual desktop collection that contain the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="755ee-112">使用者 *名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="755ee-112">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="755ee-113">使用者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="755ee-113">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="755ee-114">*UserDomain* \[在\]</span><span class="sxs-lookup"><span data-stu-id="755ee-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="755ee-115">使用者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="755ee-115">The domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="755ee-116">*VMName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="755ee-116">*VMName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="755ee-117">接收虛擬桌面的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="755ee-117">Receives the virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="755ee-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="755ee-118">Return value</span></span>

<span data-ttu-id="755ee-119">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="755ee-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="755ee-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="755ee-120">Requirements</span></span>



| <span data-ttu-id="755ee-121">需求</span><span class="sxs-lookup"><span data-stu-id="755ee-121">Requirement</span></span> | <span data-ttu-id="755ee-122">值</span><span class="sxs-lookup"><span data-stu-id="755ee-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="755ee-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="755ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="755ee-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="755ee-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="755ee-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="755ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="755ee-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="755ee-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="755ee-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="755ee-127">Namespace</span></span><br/>                | <span data-ttu-id="755ee-128">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="755ee-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="755ee-129">MOF</span><span class="sxs-lookup"><span data-stu-id="755ee-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="755ee-130"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="755ee-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="755ee-131">DLL</span><span class="sxs-lookup"><span data-stu-id="755ee-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="755ee-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="755ee-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="755ee-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="755ee-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755ee-134">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="755ee-134">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





