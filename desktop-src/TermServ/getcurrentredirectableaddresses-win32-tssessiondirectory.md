---
title: Win32_TSSessionDirectory 類別的 GetCurrentRedirectableAddresses 方法
description: 取得目前設定的 DNS 合格地址清單，可用於重新導向。
ms.assetid: 79f35d8f-b5f9-4b0f-bb7d-0d1ee3f02346
ms.tgt_platform: multiple
keywords:
- GetCurrentRedirectableAddresses 方法遠端桌面服務
- GetCurrentRedirectableAddresses 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，GetCurrentRedirectableAddresses 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6b4a859c77f449fb5a8f436be6e18c058ca59f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466760"
---
# <a name="getcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="ce090-106">Win32 TSSessionDirectory 類別的 GetCurrentRedirectableAddresses 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ce090-106">GetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="ce090-107">取得目前設定的 DNS 合格地址清單，可用於重新導向。</span><span class="sxs-lookup"><span data-stu-id="ce090-107">Obtains the currently configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce090-108">語法</span><span class="sxs-lookup"><span data-stu-id="ce090-108">Syntax</span></span>


```mof
uint32 GetCurrentRedirectableAddresses(
  [out] uint32 fTokenRedirection,
  [out] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="ce090-109">參數</span><span class="sxs-lookup"><span data-stu-id="ce090-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce090-110">*fTokenRedirection* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce090-110">*fTokenRedirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce090-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ce090-111">Type: **uint32**</span></span>

<span data-ttu-id="ce090-112">指出是否應該使用權杖重新導向的旗標。</span><span class="sxs-lookup"><span data-stu-id="ce090-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="ce090-113">*IPAddresses* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce090-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce090-114">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="ce090-114">Type: **string\[\]**</span></span>

<span data-ttu-id="ce090-115">目前已設定 DNS 合格 IP 位址的陣列，可用於重新導向。</span><span class="sxs-lookup"><span data-stu-id="ce090-115">An array of the currently configured DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce090-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce090-116">Return value</span></span>

<span data-ttu-id="ce090-117">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ce090-117">Type: **uint32**</span></span>

<span data-ttu-id="ce090-118">成功時傳回 0;否則，會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ce090-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="ce090-119">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="ce090-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce090-120">備註</span><span class="sxs-lookup"><span data-stu-id="ce090-120">Remarks</span></span>

<span data-ttu-id="ce090-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="ce090-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ce090-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ce090-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ce090-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="ce090-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ce090-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="ce090-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce090-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce090-125">Requirements</span></span>



| <span data-ttu-id="ce090-126">需求</span><span class="sxs-lookup"><span data-stu-id="ce090-126">Requirement</span></span> | <span data-ttu-id="ce090-127">值</span><span class="sxs-lookup"><span data-stu-id="ce090-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce090-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce090-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ce090-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="ce090-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ce090-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce090-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ce090-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce090-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce090-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="ce090-132">Namespace</span></span><br/>                | <span data-ttu-id="ce090-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="ce090-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ce090-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ce090-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce090-135"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce090-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce090-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ce090-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce090-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce090-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce090-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce090-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce090-139">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="ce090-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

