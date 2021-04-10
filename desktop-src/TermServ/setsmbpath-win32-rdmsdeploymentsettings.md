---
title: Win32_RDMSDeploymentSettings 類別的 SetSMBPath 方法
description: 將 UNC 路徑更新為虛擬桌面集合的虛擬機器部署所在的 SMB 共用。
ms.assetid: 0b0b5b17-7b52-41e5-b9c6-c5f3e51c7853
ms.tgt_platform: multiple
keywords:
- SetSMBPath 方法遠端桌面服務
- SetSMBPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，SetSMBPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40598a3217ff1ca7c6082b3af09097352962309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934656"
---
# <a name="setsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="2525a-106">Win32 RDMSDeploymentSettings 類別的 SetSMBPath 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2525a-106">SetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="2525a-107">將 UNC 路徑更新為虛擬桌面集合的虛擬機器部署所在的 SMB 共用。</span><span class="sxs-lookup"><span data-stu-id="2525a-107">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2525a-108">語法</span><span class="sxs-lookup"><span data-stu-id="2525a-108">Syntax</span></span>


```mof
uint32 SetSMBPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="2525a-109">參數</span><span class="sxs-lookup"><span data-stu-id="2525a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2525a-110">*DirectoryPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2525a-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2525a-111">SMB 共用的新路徑（UNC 格式）。</span><span class="sxs-lookup"><span data-stu-id="2525a-111">The new path to the SMB share, in UNC format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2525a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2525a-112">Return value</span></span>

<span data-ttu-id="2525a-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2525a-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2525a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2525a-114">Requirements</span></span>



| <span data-ttu-id="2525a-115">需求</span><span class="sxs-lookup"><span data-stu-id="2525a-115">Requirement</span></span> | <span data-ttu-id="2525a-116">值</span><span class="sxs-lookup"><span data-stu-id="2525a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2525a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2525a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2525a-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="2525a-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2525a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2525a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2525a-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2525a-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2525a-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="2525a-121">Namespace</span></span><br/>                | <span data-ttu-id="2525a-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="2525a-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2525a-123">MOF</span><span class="sxs-lookup"><span data-stu-id="2525a-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2525a-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="2525a-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2525a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2525a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2525a-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2525a-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2525a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2525a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2525a-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="2525a-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





