---
title: Win32_TSSessionDirectory 類別的 SetTSRedirectorMode 方法
description: 設定值，指出伺服器是否將作為遠端桌面服務的重新導向器。
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- SetTSRedirectorMode 方法遠端桌面服務
- SetTSRedirectorMode 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，SetTSRedirectorMode 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e3195a83a32dca0c8e4a96de211a72a66a8f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844216"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="64549-106">Win32 TSSessionDirectory 類別的 SetTSRedirectorMode 方法 \_</span><span class="sxs-lookup"><span data-stu-id="64549-106">SetTSRedirectorMode method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="64549-107">設定值，指出伺服器是否將作為遠端桌面服務的重新導向器。</span><span class="sxs-lookup"><span data-stu-id="64549-107">Sets the value to indicate whether the server will act as a Remote Desktop Services redirector.</span></span>

## <a name="syntax"></a><span data-ttu-id="64549-108">語法</span><span class="sxs-lookup"><span data-stu-id="64549-108">Syntax</span></span>


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a><span data-ttu-id="64549-109">參數</span><span class="sxs-lookup"><span data-stu-id="64549-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64549-110">*TSRedirValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64549-110">*TSRedirValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64549-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="64549-111">Type: **uint32**</span></span>

<span data-ttu-id="64549-112">指定伺服器是否將作為遠端桌面服務的重新導向器。</span><span class="sxs-lookup"><span data-stu-id="64549-112">Specifies if the server will act as a Remote Desktop Services redirector.</span></span> <span data-ttu-id="64549-113">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="64549-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="64549-114">0</span><span class="sxs-lookup"><span data-stu-id="64549-114">0</span></span>
</dt> <dd>

<span data-ttu-id="64549-115">伺服器將作為遠端桌面服務的重新導向器。</span><span class="sxs-lookup"><span data-stu-id="64549-115">The server will act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="64549-116">1</span><span class="sxs-lookup"><span data-stu-id="64549-116">1</span></span>
</dt> <dd>

<span data-ttu-id="64549-117">伺服器將不會作為遠端桌面服務的重新導向器。</span><span class="sxs-lookup"><span data-stu-id="64549-117">The server will not act as a Remote Desktop Services redirector.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64549-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="64549-118">Return value</span></span>

<span data-ttu-id="64549-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="64549-119">Type: **uint32**</span></span>

<span data-ttu-id="64549-120">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="64549-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="64549-121">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="64549-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="64549-122">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="64549-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="64549-123">備註</span><span class="sxs-lookup"><span data-stu-id="64549-123">Remarks</span></span>

<span data-ttu-id="64549-124">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="64549-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="64549-125">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="64549-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="64549-126">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="64549-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="64549-127">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="64549-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="64549-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="64549-128">Requirements</span></span>



| <span data-ttu-id="64549-129">需求</span><span class="sxs-lookup"><span data-stu-id="64549-129">Requirement</span></span> | <span data-ttu-id="64549-130">值</span><span class="sxs-lookup"><span data-stu-id="64549-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64549-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64549-131">Minimum supported client</span></span><br/> | <span data-ttu-id="64549-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="64549-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="64549-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64549-133">Minimum supported server</span></span><br/> | <span data-ttu-id="64549-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64549-134">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="64549-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="64549-135">End of client support</span></span><br/>    | <span data-ttu-id="64549-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="64549-136">None supported</span></span><br/>                                                               |
| <span data-ttu-id="64549-137">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="64549-137">End of server support</span></span><br/>    | <span data-ttu-id="64549-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64549-138">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="64549-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="64549-139">Namespace</span></span><br/>                | <span data-ttu-id="64549-140">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="64549-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="64549-141">MOF</span><span class="sxs-lookup"><span data-stu-id="64549-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64549-142"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="64549-142"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="64549-143">DLL</span><span class="sxs-lookup"><span data-stu-id="64549-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64549-144"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64549-144"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64549-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64549-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64549-146">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="64549-146">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

