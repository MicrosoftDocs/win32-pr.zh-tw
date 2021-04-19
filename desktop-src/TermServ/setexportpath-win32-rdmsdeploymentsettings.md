---
title: Win32_RDMSDeploymentSettings 類別的 SetExportPath 方法
description: 更新虛擬機器集合的虛擬機器部署所在的目錄路徑。
ms.assetid: e52b79c8-6724-4264-93d5-4a2a14c89b6b
ms.tgt_platform: multiple
keywords:
- SetExportPath 方法遠端桌面服務
- SetExportPath 方法遠端桌面服務，Win32_RDMSDeploymentSettings 類別
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，SetExportPath 方法
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32dbc844aecf86d4c62fada6c5cd68d514a69272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969971"
---
# <a name="setexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="359c5-106">Win32 RDMSDeploymentSettings 類別的 SetExportPath 方法 \_</span><span class="sxs-lookup"><span data-stu-id="359c5-106">SetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="359c5-107">更新虛擬機器集合的虛擬機器部署所在的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="359c5-107">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="359c5-108">語法</span><span class="sxs-lookup"><span data-stu-id="359c5-108">Syntax</span></span>


```mof
uint32 SetExportPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="359c5-109">參數</span><span class="sxs-lookup"><span data-stu-id="359c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="359c5-110">*DirectoryPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="359c5-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="359c5-111">新的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="359c5-111">The new directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="359c5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="359c5-112">Return value</span></span>

<span data-ttu-id="359c5-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="359c5-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="359c5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="359c5-114">Requirements</span></span>



| <span data-ttu-id="359c5-115">需求</span><span class="sxs-lookup"><span data-stu-id="359c5-115">Requirement</span></span> | <span data-ttu-id="359c5-116">值</span><span class="sxs-lookup"><span data-stu-id="359c5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="359c5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="359c5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="359c5-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="359c5-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="359c5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="359c5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="359c5-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="359c5-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="359c5-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="359c5-121">Namespace</span></span><br/>                | <span data-ttu-id="359c5-122">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="359c5-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="359c5-123">MOF</span><span class="sxs-lookup"><span data-stu-id="359c5-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="359c5-124"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="359c5-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="359c5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="359c5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="359c5-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="359c5-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="359c5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="359c5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="359c5-128">**Win32 \_ RDMSDeploymentSettings**</span><span class="sxs-lookup"><span data-stu-id="359c5-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





