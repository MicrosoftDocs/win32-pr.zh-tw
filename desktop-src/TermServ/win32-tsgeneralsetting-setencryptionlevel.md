---
title: Win32_TSGeneralSetting 類別的 SetEncryptionLevel 方法 \(英文\)
description: SetEncryptionLevel 方法會設定加密層級。
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- SetEncryptionLevel 方法遠端桌面服務
- SetEncryptionLevel 方法遠端桌面服務，Win32_TSGeneralSetting 類別
- Win32_TSGeneralSetting 類別遠端桌面服務，SetEncryptionLevel 方法
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104597"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="50d29-106">Win32 TSGeneralSetting 類別的 SetEncryptionLevel 方法 \_</span><span class="sxs-lookup"><span data-stu-id="50d29-106">SetEncryptionLevel method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="50d29-107">**SetEncryptionLevel** 方法會設定加密層級。</span><span class="sxs-lookup"><span data-stu-id="50d29-107">The **SetEncryptionLevel** method sets the encryption level.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d29-108">語法</span><span class="sxs-lookup"><span data-stu-id="50d29-108">Syntax</span></span>


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a><span data-ttu-id="50d29-109">參數</span><span class="sxs-lookup"><span data-stu-id="50d29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d29-110">*MinEncryptionLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50d29-110">*MinEncryptionLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d29-111">要設定的最小加密層級。</span><span class="sxs-lookup"><span data-stu-id="50d29-111">The minimum encryption level to set.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="50d29-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="50d29-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="50d29-113">低層級的加密。</span><span class="sxs-lookup"><span data-stu-id="50d29-113">Low level of encryption.</span></span> <span data-ttu-id="50d29-114">只有從用戶端傳送到伺服器的資料會使用56位加密進行加密。</span><span class="sxs-lookup"><span data-stu-id="50d29-114">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="50d29-115">請注意，從伺服器傳送到用戶端的資料並未加密。</span><span class="sxs-lookup"><span data-stu-id="50d29-115">Note that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="50d29-116"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="50d29-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="50d29-117">用戶端相容的加密層級。</span><span class="sxs-lookup"><span data-stu-id="50d29-117">Client-compatible level of encryption.</span></span> <span data-ttu-id="50d29-118">從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會以用戶端所支援的最大金鑰強度進行加密。</span><span class="sxs-lookup"><span data-stu-id="50d29-118">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="50d29-119"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="50d29-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="50d29-120">高層級的加密。</span><span class="sxs-lookup"><span data-stu-id="50d29-120">High level of encryption.</span></span> <span data-ttu-id="50d29-121">從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會使用強式128位加密進行加密。</span><span class="sxs-lookup"><span data-stu-id="50d29-121">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="50d29-122">無法連接不支援此加密層級的用戶端。</span><span class="sxs-lookup"><span data-stu-id="50d29-122">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="50d29-123"><span id="4"></span>**億**</span><span class="sxs-lookup"><span data-stu-id="50d29-123"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="50d29-124">符合 FIPS 規範的加密。</span><span class="sxs-lookup"><span data-stu-id="50d29-124">FIPS-compliant encryption.</span></span> <span data-ttu-id="50d29-125">從用戶端到伺服器以及從伺服器傳送到用戶端的所有資料，都會使用 Microsoft 密碼編譯模組，以聯邦資訊處理標準 (FIPS) 加密演算法進行加密和解密。</span><span class="sxs-lookup"><span data-stu-id="50d29-125">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="50d29-126">FIPS 是「密碼編譯模組的安全性需求」的標準。</span><span class="sxs-lookup"><span data-stu-id="50d29-126">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="50d29-127">FIPS 140-1 (1994) 和 FIPS 140-2 (2001) 描述美國政府內所使用之硬體和軟體密碼編譯模組的政府需求。</span><span class="sxs-lookup"><span data-stu-id="50d29-127">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d29-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="50d29-128">Return value</span></span>

<span data-ttu-id="50d29-129">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="50d29-129">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="50d29-130">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="50d29-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="50d29-131">備註</span><span class="sxs-lookup"><span data-stu-id="50d29-131">Remarks</span></span>

<span data-ttu-id="50d29-132">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="50d29-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="50d29-133">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="50d29-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="50d29-134">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="50d29-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="50d29-135">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="50d29-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="50d29-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="50d29-136">Requirements</span></span>



| <span data-ttu-id="50d29-137">需求</span><span class="sxs-lookup"><span data-stu-id="50d29-137">Requirement</span></span> | <span data-ttu-id="50d29-138">值</span><span class="sxs-lookup"><span data-stu-id="50d29-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50d29-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50d29-139">Minimum supported client</span></span><br/> | <span data-ttu-id="50d29-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50d29-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50d29-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50d29-141">Minimum supported server</span></span><br/> | <span data-ttu-id="50d29-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50d29-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50d29-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="50d29-143">Namespace</span></span><br/>                | <span data-ttu-id="50d29-144">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="50d29-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="50d29-145">MOF</span><span class="sxs-lookup"><span data-stu-id="50d29-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50d29-146"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="50d29-146"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="50d29-147">DLL</span><span class="sxs-lookup"><span data-stu-id="50d29-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50d29-148"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50d29-148"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50d29-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50d29-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d29-150">**Win32 \_ TSGeneralSetting**</span><span class="sxs-lookup"><span data-stu-id="50d29-150">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

