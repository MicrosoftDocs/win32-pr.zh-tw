---
title: 'Win32_RDMSDeploymentSettings 類別的 GetInt32Property 方法 (appanalysis .h) '
description: 抓取虛擬桌面集合部署設定的整數屬性。
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- GetInt32Property 方法遠端桌面服務
- GetInt32Property 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetInt32Property 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991777"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="7d819-106">Win32 RDMSDeploymentSettings 類別的 GetInt32Property 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7d819-106">GetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="7d819-107">抓取虛擬桌面集合部署設定的整數屬性。</span><span class="sxs-lookup"><span data-stu-id="7d819-107">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d819-108">語法</span><span class="sxs-lookup"><span data-stu-id="7d819-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="7d819-109">參數</span><span class="sxs-lookup"><span data-stu-id="7d819-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d819-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7d819-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d819-111">虛擬桌面集合的別名。</span><span class="sxs-lookup"><span data-stu-id="7d819-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="7d819-112">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7d819-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d819-113">接收已抓取值的整數。</span><span class="sxs-lookup"><span data-stu-id="7d819-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d819-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d819-114">Requirements</span></span>



| <span data-ttu-id="7d819-115">需求</span><span class="sxs-lookup"><span data-stu-id="7d819-115">Requirement</span></span> | <span data-ttu-id="7d819-116">值</span><span class="sxs-lookup"><span data-stu-id="7d819-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d819-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d819-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7d819-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="7d819-118">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="7d819-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d819-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7d819-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d819-120">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="7d819-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="7d819-121">Namespace</span></span><br/>                | <span data-ttu-id="7d819-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="7d819-122">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="7d819-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7d819-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d819-124"><dt>Appanalysis。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d819-124"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="7d819-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7d819-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d819-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d819-126"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="7d819-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7d819-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d819-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d819-128"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="7d819-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d819-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d819-130">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="7d819-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





