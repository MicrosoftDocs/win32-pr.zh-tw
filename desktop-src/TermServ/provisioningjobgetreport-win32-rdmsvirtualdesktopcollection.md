---
title: Win32_RDMSVirtualDesktopCollection 類別的 ProvisioningJobGetReport 方法
description: 取得虛擬桌面布建作業狀態的相關報告。
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- ProvisioningJobGetReport 方法遠端桌面服務
- ProvisioningJobGetReport 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，ProvisioningJobGetReport 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999608"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="e770d-106">Win32 RDMSVirtualDesktopCollection 類別的 ProvisioningJobGetReport 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e770d-106">ProvisioningJobGetReport method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="e770d-107">取得虛擬桌面布建作業狀態的相關報告。</span><span class="sxs-lookup"><span data-stu-id="e770d-107">Gets a report about the status of a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="e770d-108">語法</span><span class="sxs-lookup"><span data-stu-id="e770d-108">Syntax</span></span>


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a><span data-ttu-id="e770d-109">參數</span><span class="sxs-lookup"><span data-stu-id="e770d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e770d-110">*JobGuid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e770d-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e770d-111">可唯一識別布建作業的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="e770d-111">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="e770d-112">*JobReportXml* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e770d-112">*JobReportXml* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e770d-113">字串，包含 XML 格式的報表。</span><span class="sxs-lookup"><span data-stu-id="e770d-113">A string that contains the report in XML format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e770d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e770d-114">Return value</span></span>

<span data-ttu-id="e770d-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e770d-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e770d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e770d-116">Requirements</span></span>



| <span data-ttu-id="e770d-117">需求</span><span class="sxs-lookup"><span data-stu-id="e770d-117">Requirement</span></span> | <span data-ttu-id="e770d-118">值</span><span class="sxs-lookup"><span data-stu-id="e770d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e770d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e770d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e770d-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="e770d-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e770d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e770d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e770d-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e770d-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e770d-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="e770d-123">Namespace</span></span><br/>                | <span data-ttu-id="e770d-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="e770d-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e770d-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e770d-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e770d-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="e770d-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e770d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e770d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e770d-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e770d-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e770d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e770d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e770d-130">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="e770d-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





