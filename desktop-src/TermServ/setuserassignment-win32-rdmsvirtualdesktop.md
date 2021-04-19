---
title: Win32_RDMSVirtualDesktop 類別的 SetUserAssignment 方法
description: 將虛擬桌面指派給使用者。
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- SetUserAssignment 方法遠端桌面服務
- SetUserAssignment 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，SetUserAssignment 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106972689"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="bfb75-106">Win32 RDMSVirtualDesktop 類別的 SetUserAssignment 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bfb75-106">SetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="bfb75-107">將虛擬桌面指派給使用者。</span><span class="sxs-lookup"><span data-stu-id="bfb75-107">Assigns a virtual desktop to a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfb75-108">語法</span><span class="sxs-lookup"><span data-stu-id="bfb75-108">Syntax</span></span>


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="bfb75-109">參數</span><span class="sxs-lookup"><span data-stu-id="bfb75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfb75-110">使用者 *名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bfb75-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfb75-111">使用者的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="bfb75-111">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="bfb75-112">*UserDomain* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bfb75-112">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfb75-113">使用者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="bfb75-113">The domain name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfb75-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfb75-114">Return value</span></span>

<span data-ttu-id="bfb75-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bfb75-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfb75-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfb75-116">Requirements</span></span>



| <span data-ttu-id="bfb75-117">需求</span><span class="sxs-lookup"><span data-stu-id="bfb75-117">Requirement</span></span> | <span data-ttu-id="bfb75-118">值</span><span class="sxs-lookup"><span data-stu-id="bfb75-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb75-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bfb75-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bfb75-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="bfb75-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="bfb75-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bfb75-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bfb75-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bfb75-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="bfb75-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="bfb75-123">Namespace</span></span><br/>                | <span data-ttu-id="bfb75-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="bfb75-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="bfb75-125">MOF</span><span class="sxs-lookup"><span data-stu-id="bfb75-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfb75-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfb75-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfb75-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bfb75-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfb75-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfb75-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="bfb75-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfb75-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfb75-130">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="bfb75-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





