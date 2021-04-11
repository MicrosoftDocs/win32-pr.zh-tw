---
title: Win32_TSLicenseKeyPack 類別的 ReinstallLicenseKeyPackOffline 方法
description: 重新安裝使用透過網際網路或電話接收之授權識別碼的遠端桌面服務授權金鑰套件。
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- ReinstallLicenseKeyPackOffline 方法遠端桌面服務
- ReinstallLicenseKeyPackOffline 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ReinstallLicenseKeyPackOffline 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e805521ea750c018ab2e7965e7fbfba05a92d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843180"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="79c33-106">Win32 TSLicenseKeyPack 類別的 ReinstallLicenseKeyPackOffline 方法 \_</span><span class="sxs-lookup"><span data-stu-id="79c33-106">ReinstallLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="79c33-107">重新安裝使用透過網際網路或電話接收之授權識別碼的遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="79c33-107">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c33-108">語法</span><span class="sxs-lookup"><span data-stu-id="79c33-108">Syntax</span></span>


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="79c33-109">參數</span><span class="sxs-lookup"><span data-stu-id="79c33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79c33-110">*sLicenseKeyPackId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79c33-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79c33-111">包含35字元的授權碼。</span><span class="sxs-lookup"><span data-stu-id="79c33-111">Contains the 35-character license code.</span></span> <span data-ttu-id="79c33-112">只應將35個字元的英數位元字串指定為輸入。</span><span class="sxs-lookup"><span data-stu-id="79c33-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="79c33-113">不應新增連字號。</span><span class="sxs-lookup"><span data-stu-id="79c33-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="79c33-114">*KeyPackId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="79c33-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79c33-115">接收金鑰組識別碼。</span><span class="sxs-lookup"><span data-stu-id="79c33-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79c33-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="79c33-116">Return value</span></span>

<span data-ttu-id="79c33-117">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="79c33-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="79c33-118">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="79c33-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="79c33-119">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="79c33-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79c33-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="79c33-120">Requirements</span></span>



| <span data-ttu-id="79c33-121">需求</span><span class="sxs-lookup"><span data-stu-id="79c33-121">Requirement</span></span> | <span data-ttu-id="79c33-122">值</span><span class="sxs-lookup"><span data-stu-id="79c33-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c33-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79c33-123">Minimum supported client</span></span><br/> | <span data-ttu-id="79c33-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="79c33-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="79c33-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79c33-125">Minimum supported server</span></span><br/> | <span data-ttu-id="79c33-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79c33-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="79c33-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="79c33-127">Namespace</span></span><br/>                | <span data-ttu-id="79c33-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="79c33-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="79c33-129">MOF</span><span class="sxs-lookup"><span data-stu-id="79c33-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79c33-130"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="79c33-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="79c33-131">DLL</span><span class="sxs-lookup"><span data-stu-id="79c33-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79c33-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79c33-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79c33-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79c33-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c33-134">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="79c33-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





