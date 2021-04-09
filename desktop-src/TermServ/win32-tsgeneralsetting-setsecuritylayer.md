---
title: Win32_TSGeneralSetting 類別的 SetSecurityLayer 方法
description: SetSecurityLayer 方法會設定安全性層級。
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- SetSecurityLayer 方法遠端桌面服務
- SetSecurityLayer 方法遠端桌面服務，Win32_TSGeneralSetting 類別
- Win32_TSGeneralSetting 類別遠端桌面服務，SetSecurityLayer 方法
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934475"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="6e46f-106">Win32 TSGeneralSetting 類別的 SetSecurityLayer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6e46f-106">SetSecurityLayer method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="6e46f-107">**SetSecurityLayer** 方法會設定安全性層級。</span><span class="sxs-lookup"><span data-stu-id="6e46f-107">The **SetSecurityLayer** method sets the security layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e46f-108">語法</span><span class="sxs-lookup"><span data-stu-id="6e46f-108">Syntax</span></span>


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a><span data-ttu-id="6e46f-109">參數</span><span class="sxs-lookup"><span data-stu-id="6e46f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e46f-110">*SecurityLayer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e46f-110">*SecurityLayer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e46f-111">要設定的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="6e46f-111">The security layer to set.</span></span> <span data-ttu-id="6e46f-112">如果目前的加密層級為1，則 *SecurityLayer* 的值為2，表示無效。</span><span class="sxs-lookup"><span data-stu-id="6e46f-112">If the current Encryption Level is 1, then a value of 2 for *SecurityLayer* is not valid.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="6e46f-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP 安全性層** (0) </span><span class="sxs-lookup"><span data-stu-id="6e46f-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6e46f-114">伺服器和用戶端之間的通訊，會使用原生 RDP 加密。</span><span class="sxs-lookup"><span data-stu-id="6e46f-114">Communication between the server and the client will use native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="6e46f-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**協商** (1) </span><span class="sxs-lookup"><span data-stu-id="6e46f-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6e46f-116">會使用用戶端可支援之最安全的安全性階層。</span><span class="sxs-lookup"><span data-stu-id="6e46f-116">The most secure layer that is supported by the client will be used.</span></span> <span data-ttu-id="6e46f-117">若支援 SSL (TLS 1.0)，就會使用 SSL (TLS 1.0)。</span><span class="sxs-lookup"><span data-stu-id="6e46f-117">If supported, SSL (TLS 1.0) will be used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="6e46f-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2) </span><span class="sxs-lookup"><span data-stu-id="6e46f-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6e46f-119">SSL (TLS 1.0) 將用於伺服器驗證，以及用來加密伺服器與用戶端之間傳送的所有資料。</span><span class="sxs-lookup"><span data-stu-id="6e46f-119">SSL (TLS 1.0) will be used for server authentication as well as for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="6e46f-120">此設定需要伺服器具有 SSL 相容的憑證。</span><span class="sxs-lookup"><span data-stu-id="6e46f-120">This setting requires the server to have an SSL compatible certificate.</span></span> <span data-ttu-id="6e46f-121">這項設定與 **MinEncryptionLevel** 值1不相容。</span><span class="sxs-lookup"><span data-stu-id="6e46f-121">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e46f-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e46f-122">Return value</span></span>

<span data-ttu-id="6e46f-123">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6e46f-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6e46f-124">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="6e46f-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e46f-125">備註</span><span class="sxs-lookup"><span data-stu-id="6e46f-125">Remarks</span></span>

<span data-ttu-id="6e46f-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6e46f-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6e46f-127">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6e46f-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6e46f-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6e46f-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6e46f-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="6e46f-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e46f-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e46f-130">Requirements</span></span>



| <span data-ttu-id="6e46f-131">需求</span><span class="sxs-lookup"><span data-stu-id="6e46f-131">Requirement</span></span> | <span data-ttu-id="6e46f-132">值</span><span class="sxs-lookup"><span data-stu-id="6e46f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e46f-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e46f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6e46f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e46f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e46f-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e46f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6e46f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e46f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e46f-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="6e46f-137">Namespace</span></span><br/>                | <span data-ttu-id="6e46f-138">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="6e46f-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6e46f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6e46f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e46f-140"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e46f-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e46f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6e46f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e46f-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e46f-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e46f-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e46f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e46f-144">**Win32 \_ TSGeneralSetting**</span><span class="sxs-lookup"><span data-stu-id="6e46f-144">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dt>

[<span data-ttu-id="6e46f-145">**SetEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="6e46f-145">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

