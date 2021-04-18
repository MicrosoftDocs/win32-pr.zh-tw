---
title: Win32_TSVm 類別的 Export 方法
description: 抓取虛擬機器會話監視資訊。
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Export 方法遠端桌面服務
- Export 方法遠端桌面服務，Win32_TSVm 類別
- Win32_TSVm 類別遠端桌面服務，Export 方法
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965070"
---
# <a name="export-method-of-the-win32_tsvm-class"></a><span data-ttu-id="70b23-106">Win32 TSVm 類別的 Export 方法 \_</span><span class="sxs-lookup"><span data-stu-id="70b23-106">Export method of the Win32\_TSVm class</span></span>

<span data-ttu-id="70b23-107">抓取虛擬機器會話監視資訊。</span><span class="sxs-lookup"><span data-stu-id="70b23-107">Retrieves the virtual machine session monitoring information.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b23-108">語法</span><span class="sxs-lookup"><span data-stu-id="70b23-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a><span data-ttu-id="70b23-109">參數</span><span class="sxs-lookup"><span data-stu-id="70b23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70b23-110">*ExportFolderPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70b23-110">*ExportFolderPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70b23-111">將匯出虛擬機器的路徑。</span><span class="sxs-lookup"><span data-stu-id="70b23-111">Path to where the virtual machine will be exported.</span></span>

</dd> <dt>

<span data-ttu-id="70b23-112">*ExportJobObjectPath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="70b23-112">*ExportJobObjectPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70b23-113">成功時，會傳回 HyperV ConcreteJob 物件路徑。</span><span class="sxs-lookup"><span data-stu-id="70b23-113">On a success returns the HyperV ConcreteJob object path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70b23-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="70b23-114">Return value</span></span>

<span data-ttu-id="70b23-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="70b23-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="70b23-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="70b23-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="70b23-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="70b23-117">Requirements</span></span>



| <span data-ttu-id="70b23-118">需求</span><span class="sxs-lookup"><span data-stu-id="70b23-118">Requirement</span></span> | <span data-ttu-id="70b23-119">值</span><span class="sxs-lookup"><span data-stu-id="70b23-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b23-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70b23-120">Minimum supported client</span></span><br/> | <span data-ttu-id="70b23-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="70b23-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="70b23-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70b23-122">Minimum supported server</span></span><br/> | <span data-ttu-id="70b23-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70b23-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="70b23-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="70b23-124">Namespace</span></span><br/>                | <span data-ttu-id="70b23-125">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="70b23-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="70b23-126">MOF</span><span class="sxs-lookup"><span data-stu-id="70b23-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70b23-127"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="70b23-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="70b23-128">DLL</span><span class="sxs-lookup"><span data-stu-id="70b23-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70b23-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70b23-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70b23-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70b23-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b23-131">**Win32 \_ TSVm**</span><span class="sxs-lookup"><span data-stu-id="70b23-131">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





