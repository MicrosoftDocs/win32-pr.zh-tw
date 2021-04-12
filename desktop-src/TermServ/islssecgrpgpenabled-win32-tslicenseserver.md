---
title: Win32_TSLicenseServer 類別的 IsLSSecGrpGPEnabled 方法
description: 抓取 \ 0034; 授權伺服器安全性群組 \ 0034;遠端桌面授權伺服器上已啟用群組原則設定。
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- IsLSSecGrpGPEnabled 方法遠端桌面服務
- IsLSSecGrpGPEnabled 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsLSSecGrpGPEnabled 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104303"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="64db9-106">Win32 TSLicenseServer 類別的 IsLSSecGrpGPEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="64db9-106">IsLSSecGrpGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="64db9-107">抓取是否已在遠端桌面授權伺服器上啟用 [授權伺服器安全性群組] 群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="64db9-107">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="64db9-108">語法</span><span class="sxs-lookup"><span data-stu-id="64db9-108">Syntax</span></span>


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="64db9-109">參數</span><span class="sxs-lookup"><span data-stu-id="64db9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64db9-110">*已啟用* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="64db9-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64db9-111">指出是否已啟用 [授權伺服器安全性群組] 原則設定的布林值。</span><span class="sxs-lookup"><span data-stu-id="64db9-111">Boolean value that indicates whether the "license server security group" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64db9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="64db9-112">Return value</span></span>

<span data-ttu-id="64db9-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="64db9-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="64db9-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="64db9-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="64db9-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="64db9-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="64db9-116">備註</span><span class="sxs-lookup"><span data-stu-id="64db9-116">Remarks</span></span>

<span data-ttu-id="64db9-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="64db9-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="64db9-118">[授權伺服器安全性群組] 原則設定可讓您指定遠端桌面工作階段主機 (RD 工作階段主機) 伺服器，以允許連線到授權伺服器，遠端桌面服務 RDS Cal (取得) 用戶端存取授權。</span><span class="sxs-lookup"><span data-stu-id="64db9-118">The "license server security group" policy setting allows you to specify the Remote Desktop Session Host (RD Session Host) servers that are permitted to contact the license server to obtain Remote Desktop Services client access licenses (RDS CALs).</span></span> <span data-ttu-id="64db9-119">如果授權伺服器上已啟用此原則設定，則伺服器只會回應電腦帳戶是授權伺服器上終端機伺服器電腦本機群組成員之 RD 工作階段主機伺服器的 RDS CAL 要求。</span><span class="sxs-lookup"><span data-stu-id="64db9-119">If the policy setting is enabled on the license server, the server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="64db9-120">原則設定位於本機群組原則編輯器的下列節點中：</span><span class="sxs-lookup"><span data-stu-id="64db9-120">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="64db9-121">電腦設定 \\ 系統管理範本 \\ Windows 元件 \\ 終端機服務 \\ TS 授權</span><span class="sxs-lookup"><span data-stu-id="64db9-121">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="64db9-122">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="64db9-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="64db9-123">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="64db9-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="64db9-124">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="64db9-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="64db9-125">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="64db9-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="64db9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="64db9-126">Requirements</span></span>



| <span data-ttu-id="64db9-127">需求</span><span class="sxs-lookup"><span data-stu-id="64db9-127">Requirement</span></span> | <span data-ttu-id="64db9-128">值</span><span class="sxs-lookup"><span data-stu-id="64db9-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="64db9-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64db9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="64db9-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="64db9-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="64db9-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64db9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="64db9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64db9-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="64db9-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="64db9-133">Namespace</span></span><br/>                | <span data-ttu-id="64db9-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="64db9-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="64db9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="64db9-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64db9-136"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="64db9-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="64db9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="64db9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64db9-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64db9-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64db9-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64db9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64db9-140">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="64db9-140">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

