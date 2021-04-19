---
title: Win32_TSLicenseServer 類別的 IsLSPreventUpgradeGPEnabled 方法
description: 抓取 \ 0034; 是否防止授權升級 \ 0034;遠端桌面授權伺服器上已啟用群組原則設定。
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- IsLSPreventUpgradeGPEnabled 方法遠端桌面服務
- IsLSPreventUpgradeGPEnabled 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsLSPreventUpgradeGPEnabled 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205dc1ac05f5dca44297f8d80653ad51b7518d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969790"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="a34f2-106">Win32 TSLicenseServer 類別的 IsLSPreventUpgradeGPEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a34f2-106">IsLSPreventUpgradeGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="a34f2-107">抓取是否已在遠端桌面授權伺服器上啟用「防止授權升級」群組原則設定。</span><span class="sxs-lookup"><span data-stu-id="a34f2-107">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a34f2-108">語法</span><span class="sxs-lookup"><span data-stu-id="a34f2-108">Syntax</span></span>


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="a34f2-109">參數</span><span class="sxs-lookup"><span data-stu-id="a34f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a34f2-110">*已啟用* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a34f2-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a34f2-111">指出是否已啟用「防止授權升級」原則設定的布林值。</span><span class="sxs-lookup"><span data-stu-id="a34f2-111">Boolean value that indicates whether the "prevent license upgrade" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a34f2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a34f2-112">Return value</span></span>

<span data-ttu-id="a34f2-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="a34f2-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a34f2-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="a34f2-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a34f2-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="a34f2-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a34f2-116">備註</span><span class="sxs-lookup"><span data-stu-id="a34f2-116">Remarks</span></span>

<span data-ttu-id="a34f2-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a34f2-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a34f2-118">如果啟用「防止授權升級」原則設定，授權伺服器將只會在遠端桌面工作階段主機 (RD 工作階段主機) 伺服器的適當 RDS CAL 無法使用時，發出暫時 RDS CAL 給用戶端。</span><span class="sxs-lookup"><span data-stu-id="a34f2-118">If the "prevent license upgrade" policy setting is enabled, the license server will only issue a temporary RDS CAL to the client if an appropriate RDS CAL for the Remote Desktop Session Host (RD Session Host) server is not available.</span></span>

<span data-ttu-id="a34f2-119">原則設定位於本機群組原則編輯器的下列節點中：</span><span class="sxs-lookup"><span data-stu-id="a34f2-119">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="a34f2-120">電腦設定 \\ 系統管理範本 \\ Windows 元件 \\ 終端機服務 \\ TS 授權</span><span class="sxs-lookup"><span data-stu-id="a34f2-120">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="a34f2-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="a34f2-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a34f2-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a34f2-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a34f2-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="a34f2-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a34f2-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="a34f2-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a34f2-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a34f2-125">Requirements</span></span>



| <span data-ttu-id="a34f2-126">需求</span><span class="sxs-lookup"><span data-stu-id="a34f2-126">Requirement</span></span> | <span data-ttu-id="a34f2-127">值</span><span class="sxs-lookup"><span data-stu-id="a34f2-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a34f2-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a34f2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a34f2-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="a34f2-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a34f2-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a34f2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a34f2-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a34f2-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a34f2-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="a34f2-132">Namespace</span></span><br/>                | <span data-ttu-id="a34f2-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a34f2-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="a34f2-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a34f2-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a34f2-135"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="a34f2-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a34f2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a34f2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a34f2-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a34f2-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a34f2-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a34f2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a34f2-139">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="a34f2-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

