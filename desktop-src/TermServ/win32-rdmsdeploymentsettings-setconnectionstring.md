---
title: Win32_RDMSDeploymentSettings 類別的 SetConnectionString 方法
description: 設定部署層級的資料庫連接字串。
ms.assetid: c8902ab9-72a6-4d69-ab22-f6074205deb4
ms.tgt_platform: multiple
keywords:
- SetConnectionString 方法遠端桌面服務
- SetConnectionString 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，SetConnectionString 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ccb3f618f6a08dcb95bb7dc04c1494be6a7b5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384446"
---
# <a name="setconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="cec9f-106">Win32 RDMSDeploymentSettings 類別的 SetConnectionString 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cec9f-106">SetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="cec9f-107">設定部署層級的資料庫連接字串。</span><span class="sxs-lookup"><span data-stu-id="cec9f-107">Sets the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec9f-108">語法</span><span class="sxs-lookup"><span data-stu-id="cec9f-108">Syntax</span></span>


```mof
uint32 SetConnectionString(
  [in] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="cec9f-109">參數</span><span class="sxs-lookup"><span data-stu-id="cec9f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cec9f-110">*ConnectionString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cec9f-110">*ConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cec9f-111">要設定的連接字串</span><span class="sxs-lookup"><span data-stu-id="cec9f-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cec9f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cec9f-112">Return value</span></span>

<span data-ttu-id="cec9f-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cec9f-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec9f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cec9f-114">Requirements</span></span>



| <span data-ttu-id="cec9f-115">需求</span><span class="sxs-lookup"><span data-stu-id="cec9f-115">Requirement</span></span> | <span data-ttu-id="cec9f-116">值</span><span class="sxs-lookup"><span data-stu-id="cec9f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec9f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cec9f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cec9f-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="cec9f-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cec9f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cec9f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cec9f-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cec9f-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="cec9f-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="cec9f-121">Namespace</span></span><br/>                | <span data-ttu-id="cec9f-122">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="cec9f-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cec9f-123">MOF</span><span class="sxs-lookup"><span data-stu-id="cec9f-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cec9f-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="cec9f-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cec9f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cec9f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cec9f-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cec9f-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cec9f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cec9f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec9f-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="cec9f-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





