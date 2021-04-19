---
title: Win32_RDMSDeploymentSettings 類別的 SetInt32Property 方法
description: 針對虛擬桌面集合的部署設定，更新整數屬性。
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- SetInt32Property 方法遠端桌面服務
- SetInt32Property 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，SetInt32Property 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fecdc42031514d5219fc03172b951602ad021ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966535"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="c9300-106">Win32 RDMSDeploymentSettings 類別的 SetInt32Property 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c9300-106">SetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="c9300-107">針對虛擬桌面集合的部署設定，更新整數屬性。</span><span class="sxs-lookup"><span data-stu-id="c9300-107">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9300-108">語法</span><span class="sxs-lookup"><span data-stu-id="c9300-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="c9300-109">參數</span><span class="sxs-lookup"><span data-stu-id="c9300-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9300-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9300-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9300-111">虛擬桌面集合的別名。</span><span class="sxs-lookup"><span data-stu-id="c9300-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="c9300-112">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9300-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9300-113">新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="c9300-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9300-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9300-114">Requirements</span></span>



| <span data-ttu-id="c9300-115">需求</span><span class="sxs-lookup"><span data-stu-id="c9300-115">Requirement</span></span> | <span data-ttu-id="c9300-116">值</span><span class="sxs-lookup"><span data-stu-id="c9300-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9300-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9300-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c9300-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="c9300-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c9300-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9300-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c9300-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9300-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c9300-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9300-121">Namespace</span></span><br/>                | <span data-ttu-id="c9300-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="c9300-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c9300-123">MOF</span><span class="sxs-lookup"><span data-stu-id="c9300-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9300-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9300-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9300-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c9300-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9300-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9300-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c9300-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9300-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9300-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="c9300-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





