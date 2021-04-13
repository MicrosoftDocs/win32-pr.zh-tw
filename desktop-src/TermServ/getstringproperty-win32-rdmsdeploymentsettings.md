---
title: Win32_RDMSDeploymentSettings 類別的 GetStringProperty 方法
description: 抓取虛擬桌面集合之部署設定的字串屬性。
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- GetStringProperty 方法遠端桌面服務
- GetStringProperty 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetStringProperty 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f26a570becbbae6b0d768c399acd3dd2954ecdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384326"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="f06f1-106">Win32 RDMSDeploymentSettings 類別的 GetStringProperty 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f06f1-106">GetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="f06f1-107">抓取虛擬桌面集合之部署設定的字串屬性。</span><span class="sxs-lookup"><span data-stu-id="f06f1-107">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f06f1-108">語法</span><span class="sxs-lookup"><span data-stu-id="f06f1-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="f06f1-109">參數</span><span class="sxs-lookup"><span data-stu-id="f06f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f06f1-110">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f06f1-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f06f1-111">虛擬桌面集合的別名。</span><span class="sxs-lookup"><span data-stu-id="f06f1-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="f06f1-112">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f06f1-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f06f1-113">接收已抓取值的字串。</span><span class="sxs-lookup"><span data-stu-id="f06f1-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f06f1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f06f1-114">Requirements</span></span>



| <span data-ttu-id="f06f1-115">需求</span><span class="sxs-lookup"><span data-stu-id="f06f1-115">Requirement</span></span> | <span data-ttu-id="f06f1-116">值</span><span class="sxs-lookup"><span data-stu-id="f06f1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f06f1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f06f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f06f1-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="f06f1-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f06f1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f06f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f06f1-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f06f1-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f06f1-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="f06f1-121">Namespace</span></span><br/>                | <span data-ttu-id="f06f1-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="f06f1-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f06f1-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f06f1-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f06f1-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="f06f1-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f06f1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f06f1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f06f1-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f06f1-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f06f1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f06f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f06f1-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="f06f1-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





