---
title: 'Win32_TSVirtualIP 類別的 AddProgram 方法 (Bdaiface) '
description: 將程式新增至使用 IP 虛擬化的程式清單。
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- AddProgram 方法遠端桌面服務
- AddProgram 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，AddProgram 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de573e8d04500917ed44d5a0453005b3aa691bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685724"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="35113-106">Win32 TSVirtualIP 類別的 AddProgram 方法 \_</span><span class="sxs-lookup"><span data-stu-id="35113-106">AddProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="35113-107">將程式新增至使用 IP 虛擬化的程式清單。</span><span class="sxs-lookup"><span data-stu-id="35113-107">Adds a program to the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="35113-108">語法</span><span class="sxs-lookup"><span data-stu-id="35113-108">Syntax</span></span>


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="35113-109">參數</span><span class="sxs-lookup"><span data-stu-id="35113-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35113-110">*ProgramPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35113-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35113-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35113-111">Type: **string**</span></span>

<span data-ttu-id="35113-112">要加入至清單之程式的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="35113-112">The path and file name of the program to add to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35113-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="35113-113">Return value</span></span>

<span data-ttu-id="35113-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="35113-114">Type: **uint32**</span></span>

<span data-ttu-id="35113-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="35113-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="35113-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="35113-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="35113-117">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="35113-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="35113-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="35113-118">Requirements</span></span>



| <span data-ttu-id="35113-119">需求</span><span class="sxs-lookup"><span data-stu-id="35113-119">Requirement</span></span> | <span data-ttu-id="35113-120">值</span><span class="sxs-lookup"><span data-stu-id="35113-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35113-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35113-121">Minimum supported client</span></span><br/> | <span data-ttu-id="35113-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="35113-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="35113-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35113-123">Minimum supported server</span></span><br/> | <span data-ttu-id="35113-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35113-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="35113-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="35113-125">Namespace</span></span><br/>                | <span data-ttu-id="35113-126">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="35113-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="35113-127">標頭</span><span class="sxs-lookup"><span data-stu-id="35113-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="35113-128"><dt>Bdaiface。h</dt></span><span class="sxs-lookup"><span data-stu-id="35113-128"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="35113-129">MOF</span><span class="sxs-lookup"><span data-stu-id="35113-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35113-130"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="35113-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="35113-131">DLL</span><span class="sxs-lookup"><span data-stu-id="35113-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35113-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35113-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35113-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35113-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35113-134">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="35113-134">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





