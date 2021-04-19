---
title: Win32_TSLicenseKeyPack 類別的 InstallRetailPurchaseLicenseKeyPack 方法
description: 安裝透過零售通路購買的遠端桌面服務授權金鑰套件。
ms.assetid: cd33c785-7aa1-4e30-8155-4176b6f4c037
ms.tgt_platform: multiple
keywords:
- InstallRetailPurchaseLicenseKeyPack 方法遠端桌面服務
- InstallRetailPurchaseLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，InstallRetailPurchaseLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7523e2106a68284d6b9b376d47608114f940c194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968747"
---
# <a name="installretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="74ed7-106">Win32 TSLicenseKeyPack 類別的 InstallRetailPurchaseLicenseKeyPack 方法 \_</span><span class="sxs-lookup"><span data-stu-id="74ed7-106">InstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="74ed7-107">安裝透過零售通路購買的遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="74ed7-107">Installs a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="74ed7-108">語法</span><span class="sxs-lookup"><span data-stu-id="74ed7-108">Syntax</span></span>


```mof
uint32 InstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="74ed7-109">參數</span><span class="sxs-lookup"><span data-stu-id="74ed7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74ed7-110">*sLicenseCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74ed7-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74ed7-111">包含25個字元的授權碼。</span><span class="sxs-lookup"><span data-stu-id="74ed7-111">Contains the 25-character license code.</span></span> <span data-ttu-id="74ed7-112">只應提供25個字元的英數位元字串做為輸入。</span><span class="sxs-lookup"><span data-stu-id="74ed7-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="74ed7-113">不應新增連字號。</span><span class="sxs-lookup"><span data-stu-id="74ed7-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="74ed7-114">*KeyPackId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="74ed7-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74ed7-115">接收金鑰組識別碼。</span><span class="sxs-lookup"><span data-stu-id="74ed7-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74ed7-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="74ed7-116">Return value</span></span>

<span data-ttu-id="74ed7-117">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="74ed7-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="74ed7-118">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="74ed7-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="74ed7-119">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="74ed7-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="74ed7-120">備註</span><span class="sxs-lookup"><span data-stu-id="74ed7-120">Remarks</span></span>

<span data-ttu-id="74ed7-121">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="74ed7-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="74ed7-122">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="74ed7-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="74ed7-123">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="74ed7-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="74ed7-124">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="74ed7-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="74ed7-125">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="74ed7-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="74ed7-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="74ed7-126">Requirements</span></span>



| <span data-ttu-id="74ed7-127">需求</span><span class="sxs-lookup"><span data-stu-id="74ed7-127">Requirement</span></span> | <span data-ttu-id="74ed7-128">值</span><span class="sxs-lookup"><span data-stu-id="74ed7-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="74ed7-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74ed7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="74ed7-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="74ed7-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="74ed7-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74ed7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="74ed7-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74ed7-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="74ed7-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="74ed7-133">Namespace</span></span><br/>                | <span data-ttu-id="74ed7-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="74ed7-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="74ed7-135">MOF</span><span class="sxs-lookup"><span data-stu-id="74ed7-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74ed7-136"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="74ed7-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="74ed7-137">DLL</span><span class="sxs-lookup"><span data-stu-id="74ed7-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74ed7-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74ed7-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74ed7-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74ed7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ed7-140">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="74ed7-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

