---
title: Win32_RDMSDeploymentSettings 類別的 SetBaseVHDPath 方法
description: 抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。 |Win32_RDMSDeploymentSettings 類別的 SetBaseVHDPath 方法
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- SetBaseVHDPath 方法遠端桌面服務
- SetBaseVHDPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，SetBaseVHDPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7907640a9641cff3c94475318bf499415b25184
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981954"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="ba808-107">Win32 RDMSDeploymentSettings 類別的 SetBaseVHDPath 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ba808-107">SetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="ba808-108">抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。</span><span class="sxs-lookup"><span data-stu-id="ba808-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba808-109">語法</span><span class="sxs-lookup"><span data-stu-id="ba808-109">Syntax</span></span>


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="ba808-110">參數</span><span class="sxs-lookup"><span data-stu-id="ba808-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba808-111">*DirectoryPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ba808-111">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba808-112">新的 VHD 部署路徑。</span><span class="sxs-lookup"><span data-stu-id="ba808-112">The new VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba808-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba808-113">Return value</span></span>

<span data-ttu-id="ba808-114">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ba808-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba808-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba808-115">Requirements</span></span>



| <span data-ttu-id="ba808-116">需求</span><span class="sxs-lookup"><span data-stu-id="ba808-116">Requirement</span></span> | <span data-ttu-id="ba808-117">值</span><span class="sxs-lookup"><span data-stu-id="ba808-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba808-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba808-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ba808-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="ba808-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ba808-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba808-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ba808-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ba808-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ba808-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="ba808-122">Namespace</span></span><br/>                | <span data-ttu-id="ba808-123">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="ba808-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ba808-124">MOF</span><span class="sxs-lookup"><span data-stu-id="ba808-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba808-125"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba808-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba808-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ba808-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba808-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba808-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ba808-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba808-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba808-129">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="ba808-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





