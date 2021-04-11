---
title: Win32_RDMSDeploymentSettings 類別的 GetSecondaryConnectionString 方法
description: 抓取部署層級資料庫的次要連接字串，可用來支援密碼到期。
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- GetSecondaryConnectionString 方法遠端桌面服務
- GetSecondaryConnectionString 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetSecondaryConnectionString 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317232"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="dc1ce-106">Win32 RDMSDeploymentSettings 類別的 GetSecondaryConnectionString 方法 \_</span><span class="sxs-lookup"><span data-stu-id="dc1ce-106">GetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="dc1ce-107">抓取部署層級資料庫的次要連接字串，可用來支援密碼到期。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-107">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1ce-108">語法</span><span class="sxs-lookup"><span data-stu-id="dc1ce-108">Syntax</span></span>


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="dc1ce-109">參數</span><span class="sxs-lookup"><span data-stu-id="dc1ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc1ce-110">*SecondaryConnectionString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dc1ce-110">*SecondaryConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc1ce-111">要取出的連接字串</span><span class="sxs-lookup"><span data-stu-id="dc1ce-111">The connection string to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc1ce-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc1ce-112">Return value</span></span>

<span data-ttu-id="dc1ce-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc1ce-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc1ce-114">Requirements</span></span>



| <span data-ttu-id="dc1ce-115">需求</span><span class="sxs-lookup"><span data-stu-id="dc1ce-115">Requirement</span></span> | <span data-ttu-id="dc1ce-116">值</span><span class="sxs-lookup"><span data-stu-id="dc1ce-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc1ce-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc1ce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dc1ce-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="dc1ce-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="dc1ce-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc1ce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dc1ce-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dc1ce-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="dc1ce-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="dc1ce-121">Namespace</span></span><br/>                | <span data-ttu-id="dc1ce-122">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="dc1ce-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="dc1ce-123">MOF</span><span class="sxs-lookup"><span data-stu-id="dc1ce-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc1ce-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc1ce-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc1ce-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dc1ce-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc1ce-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc1ce-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="dc1ce-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc1ce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc1ce-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="dc1ce-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





