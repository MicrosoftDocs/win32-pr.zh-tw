---
title: Win32_RDMSDeploymentSettings 類別的 GetBaseVHDPath 方法
description: 抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。 |Win32_RDMSDeploymentSettings 類別的 GetBaseVHDPath 方法
ms.assetid: d3629a08-ef16-4aab-b74b-f837a8ba00d0
ms.tgt_platform: multiple
keywords:
- GetBaseVHDPath 方法遠端桌面服務
- GetBaseVHDPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetBaseVHDPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595c6459148a0270bed2328c70e15ef74a69acf3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945897"
---
# <a name="getbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="16070-107">Win32 RDMSDeploymentSettings 類別的 GetBaseVHDPath 方法 \_</span><span class="sxs-lookup"><span data-stu-id="16070-107">GetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="16070-108">抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。</span><span class="sxs-lookup"><span data-stu-id="16070-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="16070-109">語法</span><span class="sxs-lookup"><span data-stu-id="16070-109">Syntax</span></span>


```mof
uint32 GetBaseVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="16070-110">參數</span><span class="sxs-lookup"><span data-stu-id="16070-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16070-111">*DirectoryPath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="16070-111">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16070-112">接收 VHD 部署路徑。</span><span class="sxs-lookup"><span data-stu-id="16070-112">Receives the VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16070-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="16070-113">Return value</span></span>

<span data-ttu-id="16070-114">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="16070-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="16070-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="16070-115">Requirements</span></span>



| <span data-ttu-id="16070-116">需求</span><span class="sxs-lookup"><span data-stu-id="16070-116">Requirement</span></span> | <span data-ttu-id="16070-117">值</span><span class="sxs-lookup"><span data-stu-id="16070-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="16070-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16070-118">Minimum supported client</span></span><br/> | <span data-ttu-id="16070-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="16070-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="16070-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16070-120">Minimum supported server</span></span><br/> | <span data-ttu-id="16070-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16070-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="16070-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="16070-122">Namespace</span></span><br/>                | <span data-ttu-id="16070-123">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="16070-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="16070-124">MOF</span><span class="sxs-lookup"><span data-stu-id="16070-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16070-125"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="16070-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="16070-126">DLL</span><span class="sxs-lookup"><span data-stu-id="16070-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16070-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16070-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="16070-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16070-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16070-129">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="16070-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





