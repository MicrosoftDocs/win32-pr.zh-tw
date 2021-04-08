---
title: Win32_RDMSDeploymentSettings 類別的 SetSecondaryConnectionString 方法
description: 設定部署層級資料庫次要連接字串。
ms.assetid: 154c495e-564e-4d90-a4ff-de683d41aa73
ms.tgt_platform: multiple
keywords:
- SetSecondaryConnectionString 方法遠端桌面服務
- SetSecondaryConnectionString 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，SetSecondaryConnectionString 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8060a6f2676b5599bf44672e79ebf48e64e354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685808"
---
# <a name="setsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="4e14a-106">Win32 RDMSDeploymentSettings 類別的 SetSecondaryConnectionString 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4e14a-106">SetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="4e14a-107">設定部署層級資料庫次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="4e14a-107">Sets the deployment level database secondary connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e14a-108">語法</span><span class="sxs-lookup"><span data-stu-id="4e14a-108">Syntax</span></span>


```mof
uint32 SetSecondaryConnectionString(
  [in] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="4e14a-109">參數</span><span class="sxs-lookup"><span data-stu-id="4e14a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e14a-110">*SecondaryConnectionString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e14a-110">*SecondaryConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e14a-111">要設定的連接字串</span><span class="sxs-lookup"><span data-stu-id="4e14a-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e14a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e14a-112">Return value</span></span>

<span data-ttu-id="4e14a-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4e14a-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e14a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e14a-114">Requirements</span></span>



| <span data-ttu-id="4e14a-115">需求</span><span class="sxs-lookup"><span data-stu-id="4e14a-115">Requirement</span></span> | <span data-ttu-id="4e14a-116">值</span><span class="sxs-lookup"><span data-stu-id="4e14a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e14a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e14a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4e14a-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="4e14a-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="4e14a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e14a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4e14a-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4e14a-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="4e14a-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="4e14a-121">Namespace</span></span><br/>                | <span data-ttu-id="4e14a-122">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="4e14a-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="4e14a-123">MOF</span><span class="sxs-lookup"><span data-stu-id="4e14a-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e14a-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e14a-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e14a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4e14a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e14a-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e14a-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="4e14a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e14a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e14a-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="4e14a-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





