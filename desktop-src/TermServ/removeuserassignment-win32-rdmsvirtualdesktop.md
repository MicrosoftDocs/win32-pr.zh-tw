---
title: Win32_RDMSVirtualDesktop 類別的 RemoveUserAssignment 方法
description: 從虛擬桌面移除使用者指派。
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- RemoveUserAssignment 方法遠端桌面服務
- RemoveUserAssignment 方法遠端桌面服務，Win32_RDMSVirtualDesktop 類別
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，RemoveUserAssignment 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984960"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="7b164-106">Win32 RDMSVirtualDesktop 類別的 RemoveUserAssignment 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7b164-106">RemoveUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="7b164-107">從虛擬桌面移除使用者指派。</span><span class="sxs-lookup"><span data-stu-id="7b164-107">Removes the user assignment from the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b164-108">語法</span><span class="sxs-lookup"><span data-stu-id="7b164-108">Syntax</span></span>


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="7b164-109">參數</span><span class="sxs-lookup"><span data-stu-id="7b164-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b164-110">*VMName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b164-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b164-111">虛擬桌面的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="7b164-111">The virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b164-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b164-112">Return value</span></span>

<span data-ttu-id="7b164-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b164-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b164-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b164-114">Requirements</span></span>



| <span data-ttu-id="7b164-115">需求</span><span class="sxs-lookup"><span data-stu-id="7b164-115">Requirement</span></span> | <span data-ttu-id="7b164-116">值</span><span class="sxs-lookup"><span data-stu-id="7b164-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b164-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b164-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7b164-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="7b164-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7b164-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b164-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7b164-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b164-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7b164-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="7b164-121">Namespace</span></span><br/>                | <span data-ttu-id="7b164-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="7b164-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7b164-123">MOF</span><span class="sxs-lookup"><span data-stu-id="7b164-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b164-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b164-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b164-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7b164-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b164-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b164-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7b164-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b164-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b164-128">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="7b164-128">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





