---
title: Win32_RDMSDeploymentSettings 類別的 GetDiffVHDPath 方法
description: 抓取為虛擬桌面集合部署差異磁片的目錄路徑。
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- GetDiffVHDPath 方法遠端桌面服務
- GetDiffVHDPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetDiffVHDPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7391315013cf8487d93b32f645933d14f06db2d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384054"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="7b591-106">Win32 RDMSDeploymentSettings 類別的 GetDiffVHDPath 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7b591-106">GetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="7b591-107">抓取為虛擬桌面集合部署差異磁片的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="7b591-107">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b591-108">語法</span><span class="sxs-lookup"><span data-stu-id="7b591-108">Syntax</span></span>


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="7b591-109">參數</span><span class="sxs-lookup"><span data-stu-id="7b591-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b591-110">*DirectoryPath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7b591-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b591-111">接收新的差異磁片路徑。</span><span class="sxs-lookup"><span data-stu-id="7b591-111">Receives the new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b591-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b591-112">Return value</span></span>

<span data-ttu-id="7b591-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b591-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b591-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b591-114">Requirements</span></span>



| <span data-ttu-id="7b591-115">需求</span><span class="sxs-lookup"><span data-stu-id="7b591-115">Requirement</span></span> | <span data-ttu-id="7b591-116">值</span><span class="sxs-lookup"><span data-stu-id="7b591-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b591-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b591-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7b591-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="7b591-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7b591-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b591-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7b591-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b591-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7b591-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="7b591-121">Namespace</span></span><br/>                | <span data-ttu-id="7b591-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="7b591-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7b591-123">MOF</span><span class="sxs-lookup"><span data-stu-id="7b591-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b591-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b591-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b591-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7b591-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b591-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b591-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7b591-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b591-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b591-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="7b591-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





