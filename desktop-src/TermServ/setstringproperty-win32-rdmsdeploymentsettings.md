---
title: 'Win32_RDMSDeploymentSettings 類別的 SetStringProperty 方法 (Certenroll) '
description: 更新虛擬桌面集合之部署設定的字串屬性。
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- SetStringProperty 方法遠端桌面服務
- SetStringProperty 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，SetStringProperty 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138f6d91ed428caabf8da69e3d958675f879dd15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104604"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="1fbf2-106">Win32 RDMSDeploymentSettings 類別的 SetStringProperty 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1fbf2-106">SetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="1fbf2-107">更新虛擬桌面集合之部署設定的字串屬性。</span><span class="sxs-lookup"><span data-stu-id="1fbf2-107">Updates a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fbf2-108">語法</span><span class="sxs-lookup"><span data-stu-id="1fbf2-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="1fbf2-109">參數</span><span class="sxs-lookup"><span data-stu-id="1fbf2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fbf2-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1fbf2-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fbf2-111">虛擬桌面集合的別名。</span><span class="sxs-lookup"><span data-stu-id="1fbf2-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="1fbf2-112">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1fbf2-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fbf2-113">新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="1fbf2-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fbf2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fbf2-114">Requirements</span></span>



| <span data-ttu-id="1fbf2-115">需求</span><span class="sxs-lookup"><span data-stu-id="1fbf2-115">Requirement</span></span> | <span data-ttu-id="1fbf2-116">值</span><span class="sxs-lookup"><span data-stu-id="1fbf2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fbf2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fbf2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1fbf2-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="1fbf2-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1fbf2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fbf2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1fbf2-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fbf2-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1fbf2-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="1fbf2-121">Namespace</span></span><br/>                | <span data-ttu-id="1fbf2-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="1fbf2-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1fbf2-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1fbf2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fbf2-124"><dt>Certenroll。h</dt></span><span class="sxs-lookup"><span data-stu-id="1fbf2-124"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="1fbf2-125">MOF</span><span class="sxs-lookup"><span data-stu-id="1fbf2-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fbf2-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fbf2-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fbf2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1fbf2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fbf2-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fbf2-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1fbf2-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fbf2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fbf2-130">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="1fbf2-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





