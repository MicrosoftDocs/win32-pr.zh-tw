---
title: Win32_TSSessionDirectory 類別的 SetCurrentRedirectableAddresses 方法
description: 設定可用於重新導向之 DNS 合格位址的已設定清單。
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- SetCurrentRedirectableAddresses 方法遠端桌面服務
- SetCurrentRedirectableAddresses 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，SetCurrentRedirectableAddresses 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e70f8d108e908155b5db3e6800f4be26811c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384969"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="c0a3d-106">Win32 TSSessionDirectory 類別的 SetCurrentRedirectableAddresses 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c0a3d-106">SetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="c0a3d-107">**SetCurrentRedirectableAddresses** 方法會設定可用於重新導向之 DNS 合格位址的已設定清單。</span><span class="sxs-lookup"><span data-stu-id="c0a3d-107">The **SetCurrentRedirectableAddresses** method sets the configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0a3d-108">語法</span><span class="sxs-lookup"><span data-stu-id="c0a3d-108">Syntax</span></span>


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="c0a3d-109">參數</span><span class="sxs-lookup"><span data-stu-id="c0a3d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0a3d-110">*fTokenRedirection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0a3d-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0a3d-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0a3d-111">Type: **uint32**</span></span>

<span data-ttu-id="c0a3d-112">指出是否應該使用權杖重新導向的旗標。</span><span class="sxs-lookup"><span data-stu-id="c0a3d-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="c0a3d-113">*IPAddresses* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0a3d-113">*IPAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0a3d-114">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="c0a3d-114">Type: **string\[\]**</span></span>

<span data-ttu-id="c0a3d-115">字串的陣列，表示可用於重新導向的 DNS 合格 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="c0a3d-115">An array of strings that represents the list of DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0a3d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0a3d-116">Return value</span></span>

<span data-ttu-id="c0a3d-117">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0a3d-117">Type: **uint32**</span></span>

<span data-ttu-id="c0a3d-118">成功時傳回 0;否則，會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c0a3d-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="c0a3d-119">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="c0a3d-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0a3d-120">備註</span><span class="sxs-lookup"><span data-stu-id="c0a3d-120">Remarks</span></span>

<span data-ttu-id="c0a3d-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c0a3d-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c0a3d-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c0a3d-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c0a3d-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c0a3d-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c0a3d-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="c0a3d-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a3d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0a3d-125">Requirements</span></span>



| <span data-ttu-id="c0a3d-126">需求</span><span class="sxs-lookup"><span data-stu-id="c0a3d-126">Requirement</span></span> | <span data-ttu-id="c0a3d-127">值</span><span class="sxs-lookup"><span data-stu-id="c0a3d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a3d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0a3d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a3d-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="c0a3d-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c0a3d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0a3d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a3d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0a3d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0a3d-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="c0a3d-132">Namespace</span></span><br/>                | <span data-ttu-id="c0a3d-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="c0a3d-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c0a3d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c0a3d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0a3d-135"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0a3d-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0a3d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c0a3d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0a3d-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0a3d-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0a3d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0a3d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a3d-139">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="c0a3d-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

