---
title: Win32_TSClientSetting 類別的 SetMaxYResolution 方法
description: 設定 MaxYResolution 屬性。
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- SetMaxYResolution 方法遠端桌面服務
- SetMaxYResolution 方法遠端桌面服務，Win32_TSClientSetting 類別
- Win32_TSClientSetting 類別遠端桌面服務，SetMaxYResolution 方法
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c85564e075865d993552e831869979fc6227af29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106988035"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="dc386-106">Win32 TSClientSetting 類別的 SetMaxYResolution 方法 \_</span><span class="sxs-lookup"><span data-stu-id="dc386-106">SetMaxYResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="dc386-107">設定 **MaxYResolution** 屬性。</span><span class="sxs-lookup"><span data-stu-id="dc386-107">Sets the **MaxYResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc386-108">語法</span><span class="sxs-lookup"><span data-stu-id="dc386-108">Syntax</span></span>


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a><span data-ttu-id="dc386-109">參數</span><span class="sxs-lookup"><span data-stu-id="dc386-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc386-110">*MaxYResolution* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc386-110">*MaxYResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc386-111">伺服器支援的新最大 Y 解析度。</span><span class="sxs-lookup"><span data-stu-id="dc386-111">The new maximum Y resolution supported by the server.</span></span> <span data-ttu-id="dc386-112">最小值是200，而最大值是2048。</span><span class="sxs-lookup"><span data-stu-id="dc386-112">The minimum value is 200 and the maximum value is 2048.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc386-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc386-113">Return value</span></span>

<span data-ttu-id="dc386-114">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc386-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="dc386-115">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="dc386-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="dc386-116">如果伺服器已覆寫使用者的連接設定，此方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="dc386-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc386-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc386-117">Requirements</span></span>



| <span data-ttu-id="dc386-118">需求</span><span class="sxs-lookup"><span data-stu-id="dc386-118">Requirement</span></span> | <span data-ttu-id="dc386-119">值</span><span class="sxs-lookup"><span data-stu-id="dc386-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc386-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc386-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dc386-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="dc386-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="dc386-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc386-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dc386-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dc386-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="dc386-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="dc386-124">Namespace</span></span><br/>                | <span data-ttu-id="dc386-125">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="dc386-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="dc386-126">MOF</span><span class="sxs-lookup"><span data-stu-id="dc386-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc386-127"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc386-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc386-128">DLL</span><span class="sxs-lookup"><span data-stu-id="dc386-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc386-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc386-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc386-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc386-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc386-131">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="dc386-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





