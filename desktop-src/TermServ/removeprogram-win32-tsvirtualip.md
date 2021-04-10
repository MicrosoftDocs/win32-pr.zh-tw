---
title: 'Win32_TSVirtualIP 類別的 RemoveProgram 方法 (Bdaiface) '
description: 從使用 IP 虛擬化的程式清單中移除程式。
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- RemoveProgram 方法遠端桌面服務
- RemoveProgram 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，RemoveProgram 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6241664b6e56c3d387673b6a1cc50e43b413336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686491"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="d88ae-106">Win32 TSVirtualIP 類別的 RemoveProgram 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d88ae-106">RemoveProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="d88ae-107">從使用 IP 虛擬化的程式清單中移除程式。</span><span class="sxs-lookup"><span data-stu-id="d88ae-107">Removes a program from the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88ae-108">語法</span><span class="sxs-lookup"><span data-stu-id="d88ae-108">Syntax</span></span>


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="d88ae-109">參數</span><span class="sxs-lookup"><span data-stu-id="d88ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d88ae-110">*ProgramPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d88ae-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d88ae-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d88ae-111">Type: **string**</span></span>

<span data-ttu-id="d88ae-112">要從清單中移除之程式的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="d88ae-112">The path and file name of the program to remove from the list.</span></span> <span data-ttu-id="d88ae-113">如果找不到程式，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d88ae-113">If the program is not found, an error is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d88ae-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d88ae-114">Return value</span></span>

<span data-ttu-id="d88ae-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d88ae-115">Type: **uint32**</span></span>

<span data-ttu-id="d88ae-116">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d88ae-116">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d88ae-117">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="d88ae-117">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="d88ae-118">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d88ae-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d88ae-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d88ae-119">Requirements</span></span>



| <span data-ttu-id="d88ae-120">需求</span><span class="sxs-lookup"><span data-stu-id="d88ae-120">Requirement</span></span> | <span data-ttu-id="d88ae-121">值</span><span class="sxs-lookup"><span data-stu-id="d88ae-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d88ae-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d88ae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d88ae-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="d88ae-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d88ae-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d88ae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d88ae-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d88ae-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="d88ae-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="d88ae-126">Namespace</span></span><br/>                | <span data-ttu-id="d88ae-127">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="d88ae-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d88ae-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d88ae-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d88ae-129"><dt>Bdaiface。h</dt></span><span class="sxs-lookup"><span data-stu-id="d88ae-129"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="d88ae-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d88ae-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d88ae-131"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="d88ae-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d88ae-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d88ae-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d88ae-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d88ae-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d88ae-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d88ae-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88ae-135">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="d88ae-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





