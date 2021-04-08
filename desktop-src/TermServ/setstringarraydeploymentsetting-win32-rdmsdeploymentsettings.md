---
title: Win32_RDMSDeploymentSettings 類別的 SetStringArrayDeploymentSetting 方法
description: 更新虛擬桌面集合的部署設定。
ms.assetid: 386594bd-a793-4e5d-ad2c-217951bee9f6
ms.tgt_platform: multiple
keywords:
- SetStringArrayDeploymentSetting 方法遠端桌面服務
- SetStringArrayDeploymentSetting 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，SetStringArrayDeploymentSetting 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb5ecc6d1238b739f8fe19d02e96ba427ed09b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686423"
---
# <a name="setstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="5ad60-106">Win32 RDMSDeploymentSettings 類別的 SetStringArrayDeploymentSetting 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5ad60-106">SetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="5ad60-107">更新虛擬桌面集合的部署設定。</span><span class="sxs-lookup"><span data-stu-id="5ad60-107">Updates the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad60-108">語法</span><span class="sxs-lookup"><span data-stu-id="5ad60-108">Syntax</span></span>


```mof
uint32 SetStringArrayDeploymentSetting(
  [in] string Key,
  [in] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="5ad60-109">參數</span><span class="sxs-lookup"><span data-stu-id="5ad60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ad60-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ad60-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad60-111">虛擬桌面集合的別名。</span><span class="sxs-lookup"><span data-stu-id="5ad60-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="5ad60-112">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ad60-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad60-113">字串的陣列，其中包含新的部署設定。</span><span class="sxs-lookup"><span data-stu-id="5ad60-113">An array of strings that contains the new deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ad60-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ad60-114">Requirements</span></span>



| <span data-ttu-id="5ad60-115">需求</span><span class="sxs-lookup"><span data-stu-id="5ad60-115">Requirement</span></span> | <span data-ttu-id="5ad60-116">值</span><span class="sxs-lookup"><span data-stu-id="5ad60-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad60-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ad60-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ad60-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="5ad60-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5ad60-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ad60-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ad60-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ad60-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5ad60-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="5ad60-121">Namespace</span></span><br/>                | <span data-ttu-id="5ad60-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="5ad60-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5ad60-123">MOF</span><span class="sxs-lookup"><span data-stu-id="5ad60-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ad60-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ad60-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ad60-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5ad60-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ad60-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ad60-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5ad60-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ad60-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad60-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="5ad60-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





