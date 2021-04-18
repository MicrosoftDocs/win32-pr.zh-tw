---
title: Win32_RDMSDeploymentSettings 類別的 GetExportPath 方法
description: 抓取虛擬機器集合的虛擬機器部署所在的目錄路徑。
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- GetExportPath 方法遠端桌面服務
- GetExportPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，GetExportPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baf96d1d71554f1b8ea310759d36d0918a511cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967317"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="755b0-106">Win32 RDMSDeploymentSettings 類別的 GetExportPath 方法 \_</span><span class="sxs-lookup"><span data-stu-id="755b0-106">GetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="755b0-107">抓取虛擬機器集合的虛擬機器部署所在的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="755b0-107">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="755b0-108">語法</span><span class="sxs-lookup"><span data-stu-id="755b0-108">Syntax</span></span>


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="755b0-109">參數</span><span class="sxs-lookup"><span data-stu-id="755b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="755b0-110">*DirectoryPath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="755b0-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="755b0-111">接收目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="755b0-111">Receives the directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="755b0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="755b0-112">Return value</span></span>

<span data-ttu-id="755b0-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="755b0-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="755b0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="755b0-114">Requirements</span></span>



| <span data-ttu-id="755b0-115">需求</span><span class="sxs-lookup"><span data-stu-id="755b0-115">Requirement</span></span> | <span data-ttu-id="755b0-116">值</span><span class="sxs-lookup"><span data-stu-id="755b0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="755b0-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="755b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="755b0-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="755b0-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="755b0-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="755b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="755b0-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="755b0-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="755b0-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="755b0-121">Namespace</span></span><br/>                | <span data-ttu-id="755b0-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="755b0-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="755b0-123">MOF</span><span class="sxs-lookup"><span data-stu-id="755b0-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="755b0-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="755b0-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="755b0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="755b0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="755b0-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="755b0-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="755b0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="755b0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755b0-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="755b0-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





