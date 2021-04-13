---
title: Win32_RDMSDeploymentSettings 類別的 GetConnectionString 方法
description: 抓取部署層級的資料庫連接字串。
ms.assetid: 91a90883-9b87-42e5-af52-90226f0344bf
ms.tgt_platform: multiple
keywords:
- GetConnectionString 方法遠端桌面服務
- GetConnectionString 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetConnectionString 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6476c938f62e0cd0e1f9d034c89fded50994946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465552"
---
# <a name="getconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="78bbb-106">Win32 RDMSDeploymentSettings 類別的 GetConnectionString 方法 \_</span><span class="sxs-lookup"><span data-stu-id="78bbb-106">GetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="78bbb-107">抓取部署層級的資料庫連接字串。</span><span class="sxs-lookup"><span data-stu-id="78bbb-107">Retrieves the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="78bbb-108">語法</span><span class="sxs-lookup"><span data-stu-id="78bbb-108">Syntax</span></span>


```mof
uint32 GetConnectionString(
  [out] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="78bbb-109">參數</span><span class="sxs-lookup"><span data-stu-id="78bbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78bbb-110">*ConnectionString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="78bbb-110">*ConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78bbb-111">連接字串</span><span class="sxs-lookup"><span data-stu-id="78bbb-111">The connection string</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78bbb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="78bbb-112">Return value</span></span>

<span data-ttu-id="78bbb-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="78bbb-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="78bbb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="78bbb-114">Requirements</span></span>



| <span data-ttu-id="78bbb-115">需求</span><span class="sxs-lookup"><span data-stu-id="78bbb-115">Requirement</span></span> | <span data-ttu-id="78bbb-116">值</span><span class="sxs-lookup"><span data-stu-id="78bbb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="78bbb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78bbb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="78bbb-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="78bbb-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="78bbb-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78bbb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="78bbb-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="78bbb-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="78bbb-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="78bbb-121">Namespace</span></span><br/>                | <span data-ttu-id="78bbb-122">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="78bbb-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="78bbb-123">MOF</span><span class="sxs-lookup"><span data-stu-id="78bbb-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78bbb-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="78bbb-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="78bbb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="78bbb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78bbb-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78bbb-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="78bbb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78bbb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78bbb-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="78bbb-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





