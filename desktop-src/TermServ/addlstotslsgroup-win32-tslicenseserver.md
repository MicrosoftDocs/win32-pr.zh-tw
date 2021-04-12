---
title: Win32_TSLicenseServer 類別的 AddLStoTSLSGroup 方法
description: 將遠端桌面授權伺服器新增至與遠端桌面授權伺服器相同網域中的網域控制站上的遠端桌面連線代理人 (RD 連線代理人) 授權伺服器群組。
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- AddLStoTSLSGroup 方法遠端桌面服務
- AddLStoTSLSGroup 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，AddLStoTSLSGroup 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53934f6682d1a23f99916588aa4eac3b18526c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384338"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="c783b-106">Win32 TSLicenseServer 類別的 AddLStoTSLSGroup 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c783b-106">AddLStoTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="c783b-107">將遠端桌面授權伺服器新增至與遠端桌面授權伺服器相同網域中的網域控制站上的遠端桌面連線代理人 (RD 連線代理人) 授權伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="c783b-107">Adds the Remote Desktop license server to the Remote Desktop Connection Broker (RD Connection Broker) License Servers group on a domain controller in the same domain as the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c783b-108">語法</span><span class="sxs-lookup"><span data-stu-id="c783b-108">Syntax</span></span>


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="c783b-109">參數</span><span class="sxs-lookup"><span data-stu-id="c783b-109">Parameters</span></span>

<span data-ttu-id="c783b-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c783b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c783b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c783b-111">Return value</span></span>

<span data-ttu-id="c783b-112">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="c783b-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c783b-113">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="c783b-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c783b-114">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="c783b-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c783b-115">備註</span><span class="sxs-lookup"><span data-stu-id="c783b-115">Remarks</span></span>

<span data-ttu-id="c783b-116">您必須是 Domain Admins 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c783b-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="c783b-117">如果伺服器設定為使用網域或樹系探索領域，則授權伺服器應該是 [遠端桌面授權伺服器] 群組的成員。</span><span class="sxs-lookup"><span data-stu-id="c783b-117">The license server should be a member of the Remote Desktop license servers group if the server is configured to use the domain or forest discovery scope.</span></span>

<span data-ttu-id="c783b-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c783b-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c783b-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c783b-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c783b-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c783b-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c783b-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="c783b-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c783b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c783b-122">Requirements</span></span>



| <span data-ttu-id="c783b-123">需求</span><span class="sxs-lookup"><span data-stu-id="c783b-123">Requirement</span></span> | <span data-ttu-id="c783b-124">值</span><span class="sxs-lookup"><span data-stu-id="c783b-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c783b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c783b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c783b-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="c783b-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c783b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c783b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c783b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c783b-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c783b-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="c783b-129">Namespace</span></span><br/>                | <span data-ttu-id="c783b-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c783b-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c783b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c783b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c783b-132"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="c783b-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c783b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c783b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c783b-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c783b-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c783b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c783b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c783b-136">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="c783b-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="c783b-137">**IsLSinTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="c783b-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

