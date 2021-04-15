---
title: Win32_RDMSVirtualDesktopCollection 類別的 ProvisioningJobExecute 方法
description: 執行虛擬桌面布建作業。
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- ProvisioningJobExecute 方法遠端桌面服務
- ProvisioningJobExecute 方法遠端桌面服務，Win32_RDMSVirtualDesktopCollection 類別
- Win32_RDMSVirtualDesktopCollection 類別遠端桌面服務，ProvisioningJobExecute 方法
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466744"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="5c504-106">Win32 RDMSVirtualDesktopCollection 類別的 ProvisioningJobExecute 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5c504-106">ProvisioningJobExecute method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="5c504-107">執行虛擬桌面布建作業。</span><span class="sxs-lookup"><span data-stu-id="5c504-107">Runs a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c504-108">語法</span><span class="sxs-lookup"><span data-stu-id="5c504-108">Syntax</span></span>


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="5c504-109">參數</span><span class="sxs-lookup"><span data-stu-id="5c504-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c504-110">*JobInputXml* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c504-110">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c504-111">包含 XML 格式之布建資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="5c504-111">A string that contains the provisioning information in XML format.</span></span>

</dd> <dt>

<span data-ttu-id="5c504-112">*JobGuid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5c504-112">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c504-113">可唯一識別要執行之布建作業的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="5c504-113">The **GUID** that uniquely identifies the provisioning job to run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c504-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c504-114">Return value</span></span>

<span data-ttu-id="5c504-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5c504-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c504-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c504-116">Requirements</span></span>



| <span data-ttu-id="5c504-117">需求</span><span class="sxs-lookup"><span data-stu-id="5c504-117">Requirement</span></span> | <span data-ttu-id="5c504-118">值</span><span class="sxs-lookup"><span data-stu-id="5c504-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c504-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c504-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c504-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="5c504-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5c504-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c504-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c504-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c504-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5c504-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="5c504-123">Namespace</span></span><br/>                | <span data-ttu-id="5c504-124">根 \\ CIMv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="5c504-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5c504-125">MOF</span><span class="sxs-lookup"><span data-stu-id="5c504-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c504-126"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c504-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c504-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5c504-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c504-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c504-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5c504-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c504-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c504-130">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="5c504-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





