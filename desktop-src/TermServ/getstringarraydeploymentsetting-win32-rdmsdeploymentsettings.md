---
title: Win32_RDMSDeploymentSettings 類別的 GetStringArrayDeploymentSetting 方法
description: 抓取虛擬桌面集合的部署設定。
ms.assetid: ab380618-560e-425b-9bf0-a7de6b30d01a
ms.tgt_platform: multiple
keywords:
- GetStringArrayDeploymentSetting 方法遠端桌面服務
- GetStringArrayDeploymentSetting 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetStringArrayDeploymentSetting 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ac0b82441abef8af1b4f6c8e3bd48b89a8cb6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094119"
---
# <a name="getstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="40d5b-106">Win32 RDMSDeploymentSettings 類別的 GetStringArrayDeploymentSetting 方法 \_</span><span class="sxs-lookup"><span data-stu-id="40d5b-106">GetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="40d5b-107">抓取虛擬桌面集合的部署設定。</span><span class="sxs-lookup"><span data-stu-id="40d5b-107">Retrieves the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d5b-108">語法</span><span class="sxs-lookup"><span data-stu-id="40d5b-108">Syntax</span></span>


```mof
uint32 GetStringArrayDeploymentSetting(
  [in]  string Key,
  [out] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="40d5b-109">參數</span><span class="sxs-lookup"><span data-stu-id="40d5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d5b-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40d5b-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d5b-111">虛擬桌面集合的別名。</span><span class="sxs-lookup"><span data-stu-id="40d5b-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="40d5b-112">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="40d5b-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40d5b-113">接收包含部署設定的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="40d5b-113">Receives an array of strings that contains the deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40d5b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="40d5b-114">Requirements</span></span>



| <span data-ttu-id="40d5b-115">需求</span><span class="sxs-lookup"><span data-stu-id="40d5b-115">Requirement</span></span> | <span data-ttu-id="40d5b-116">值</span><span class="sxs-lookup"><span data-stu-id="40d5b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="40d5b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40d5b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="40d5b-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="40d5b-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="40d5b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40d5b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="40d5b-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="40d5b-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="40d5b-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="40d5b-121">Namespace</span></span><br/>                | <span data-ttu-id="40d5b-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="40d5b-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="40d5b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="40d5b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40d5b-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="40d5b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="40d5b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40d5b-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d5b-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="40d5b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40d5b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d5b-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="40d5b-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





