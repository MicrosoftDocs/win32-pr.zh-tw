---
title: Win32_RDMSDeploymentSettings 類別的 RemoveDeploymentSetting 方法
description: 刪除虛擬桌面集合的部署設定。
ms.assetid: 68e102a3-8f3f-4997-bdf0-c2ae3640ed42
ms.tgt_platform: multiple
keywords:
- RemoveDeploymentSetting 方法遠端桌面服務
- RemoveDeploymentSetting 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，RemoveDeploymentSetting 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.RemoveDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336b93f86d6b96074341dde4851813b26eb66fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844307"
---
# <a name="removedeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="17a8e-106">Win32 RDMSDeploymentSettings 類別的 RemoveDeploymentSetting 方法 \_</span><span class="sxs-lookup"><span data-stu-id="17a8e-106">RemoveDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="17a8e-107">刪除虛擬桌面集合的部署設定。</span><span class="sxs-lookup"><span data-stu-id="17a8e-107">Deletes the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a8e-108">語法</span><span class="sxs-lookup"><span data-stu-id="17a8e-108">Syntax</span></span>


```mof
uint32 RemoveDeploymentSetting(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="17a8e-109">參數</span><span class="sxs-lookup"><span data-stu-id="17a8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17a8e-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17a8e-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a8e-111">虛擬桌面集合的別名。</span><span class="sxs-lookup"><span data-stu-id="17a8e-111">The alias of the virtual desktop collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17a8e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="17a8e-112">Requirements</span></span>



| <span data-ttu-id="17a8e-113">需求</span><span class="sxs-lookup"><span data-stu-id="17a8e-113">Requirement</span></span> | <span data-ttu-id="17a8e-114">值</span><span class="sxs-lookup"><span data-stu-id="17a8e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="17a8e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17a8e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="17a8e-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="17a8e-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="17a8e-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17a8e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="17a8e-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17a8e-118">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="17a8e-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="17a8e-119">Namespace</span></span><br/>                | <span data-ttu-id="17a8e-120">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="17a8e-120">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="17a8e-121">MOF</span><span class="sxs-lookup"><span data-stu-id="17a8e-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17a8e-122"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="17a8e-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="17a8e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="17a8e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17a8e-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17a8e-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="17a8e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17a8e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a8e-126">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="17a8e-126">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





