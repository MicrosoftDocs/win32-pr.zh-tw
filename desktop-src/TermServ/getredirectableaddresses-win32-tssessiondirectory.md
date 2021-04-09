---
title: Win32_TSSessionDirectory 類別的 GetRedirectableAddresses 方法
description: 取得 DNS 合格位址的完整清單。
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- GetRedirectableAddresses 方法遠端桌面服務
- GetRedirectableAddresses 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，GetRedirectableAddresses 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024614"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="5eaa9-106">Win32 TSSessionDirectory 類別的 GetRedirectableAddresses 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5eaa9-106">GetRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="5eaa9-107">取得 DNS 合格位址的完整清單。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-107">Obtains the entire list of DNS eligible addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eaa9-108">語法</span><span class="sxs-lookup"><span data-stu-id="5eaa9-108">Syntax</span></span>


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a><span data-ttu-id="5eaa9-109">參數</span><span class="sxs-lookup"><span data-stu-id="5eaa9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eaa9-110">*fTokenRedirection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5eaa9-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eaa9-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5eaa9-111">Type: **uint32**</span></span>

<span data-ttu-id="5eaa9-112">指出是否應該使用權杖重新導向的旗標。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="5eaa9-113">*IPAddresses* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5eaa9-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eaa9-114">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5eaa9-114">Type: **string\[\]**</span></span>

<span data-ttu-id="5eaa9-115">可用於重新導向的完整 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-115">The entire list of IP addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="5eaa9-116">*AdapterNames* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5eaa9-116">*AdapterNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eaa9-117">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5eaa9-117">Type: **string\[\]**</span></span>

<span data-ttu-id="5eaa9-118">與可用來重新導向的位址相關聯的網路介面卡名稱清單。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-118">The list of network adapter names that are associated with the addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="5eaa9-119">*NetConName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5eaa9-119">*NetConName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eaa9-120">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5eaa9-120">Type: **string\[\]**</span></span>

<span data-ttu-id="5eaa9-121">與可用來重新導向的位址相關聯的網路連接名稱清單。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-121">The list of network connection names that are associated with the addresses that are available for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eaa9-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="5eaa9-122">Return value</span></span>

<span data-ttu-id="5eaa9-123">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5eaa9-123">Type: **uint32**</span></span>

<span data-ttu-id="5eaa9-124">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-124">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5eaa9-125">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-125">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eaa9-126">備註</span><span class="sxs-lookup"><span data-stu-id="5eaa9-126">Remarks</span></span>

<span data-ttu-id="5eaa9-127">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5eaa9-128">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5eaa9-129">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5eaa9-130">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="5eaa9-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5eaa9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="5eaa9-131">Requirements</span></span>



| <span data-ttu-id="5eaa9-132">需求</span><span class="sxs-lookup"><span data-stu-id="5eaa9-132">Requirement</span></span> | <span data-ttu-id="5eaa9-133">值</span><span class="sxs-lookup"><span data-stu-id="5eaa9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5eaa9-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5eaa9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5eaa9-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="5eaa9-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5eaa9-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5eaa9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5eaa9-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5eaa9-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5eaa9-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="5eaa9-138">Namespace</span></span><br/>                | <span data-ttu-id="5eaa9-139">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="5eaa9-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5eaa9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5eaa9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5eaa9-141"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="5eaa9-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5eaa9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5eaa9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5eaa9-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5eaa9-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eaa9-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5eaa9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eaa9-145">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="5eaa9-145">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

