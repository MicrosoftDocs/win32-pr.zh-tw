---
title: Win32_RDMSDeploymentSettings 類別的 GetSMBPath 方法
description: 抓取虛擬桌面集合的虛擬機器部署所在 SMB 共用的 UNC 路徑。
ms.assetid: 0a5d3c11-6a77-48f7-a3ea-6f82725ff01f
ms.tgt_platform: multiple
keywords:
- GetSMBPath 方法遠端桌面服務
- GetSMBPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetSMBPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1738faf82a6405018495dd762ba9585daa3e1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385290"
---
# <a name="getsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="e911b-106">Win32 RDMSDeploymentSettings 類別的 GetSMBPath 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e911b-106">GetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="e911b-107">抓取虛擬桌面集合的虛擬機器部署所在 SMB 共用的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="e911b-107">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e911b-108">語法</span><span class="sxs-lookup"><span data-stu-id="e911b-108">Syntax</span></span>


```mof
uint32 GetSMBPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="e911b-109">參數</span><span class="sxs-lookup"><span data-stu-id="e911b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e911b-110">*DirectoryPath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e911b-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e911b-111">接收 SMB 共用的 UNC 格式化路徑。</span><span class="sxs-lookup"><span data-stu-id="e911b-111">Receives a UNC formatted path to the SMB share.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e911b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e911b-112">Return value</span></span>

<span data-ttu-id="e911b-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e911b-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e911b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e911b-114">Requirements</span></span>



| <span data-ttu-id="e911b-115">需求</span><span class="sxs-lookup"><span data-stu-id="e911b-115">Requirement</span></span> | <span data-ttu-id="e911b-116">值</span><span class="sxs-lookup"><span data-stu-id="e911b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e911b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e911b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e911b-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="e911b-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e911b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e911b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e911b-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e911b-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e911b-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="e911b-121">Namespace</span></span><br/>                | <span data-ttu-id="e911b-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="e911b-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e911b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e911b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e911b-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="e911b-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e911b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e911b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e911b-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e911b-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e911b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e911b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e911b-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="e911b-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





