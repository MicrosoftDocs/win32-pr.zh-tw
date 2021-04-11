---
title: Win32_TSLicenseServer 類別的 PublishLS 方法
description: 在 Active Directory Domain Services 發佈遠端桌面授權伺服器。
ms.assetid: 726d5dec-e438-455e-adb8-56d646d65d13
ms.tgt_platform: multiple
keywords:
- PublishLS 方法遠端桌面服務
- PublishLS 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，PublishLS 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.PublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3d20efe8b61cd00e1986bb190500c93fd9473
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105852"
---
# <a name="publishls-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f0a42-106">Win32 TSLicenseServer 類別的 PublishLS 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f0a42-106">PublishLS method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f0a42-107">在 Active Directory Domain Services 發佈遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="f0a42-107">Publishes the Remote Desktop license server in Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a42-108">語法</span><span class="sxs-lookup"><span data-stu-id="f0a42-108">Syntax</span></span>


```mof
uint32 PublishLS();
```



## <a name="parameters"></a><span data-ttu-id="f0a42-109">參數</span><span class="sxs-lookup"><span data-stu-id="f0a42-109">Parameters</span></span>

<span data-ttu-id="f0a42-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f0a42-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0a42-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0a42-111">Return value</span></span>

<span data-ttu-id="f0a42-112">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f0a42-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f0a42-113">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="f0a42-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f0a42-114">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="f0a42-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f0a42-115">備註</span><span class="sxs-lookup"><span data-stu-id="f0a42-115">Remarks</span></span>

<span data-ttu-id="f0a42-116">若要呼叫這個方法，您必須以企業系統管理員的身分登入授權伺服器為其成員的樹系。</span><span class="sxs-lookup"><span data-stu-id="f0a42-116">To call this method, you must be logged on as an enterprise administrator to the forest in which the license server is a member.</span></span>

<span data-ttu-id="f0a42-117">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="f0a42-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f0a42-118">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f0a42-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f0a42-119">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f0a42-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f0a42-120">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="f0a42-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0a42-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0a42-121">Requirements</span></span>



| <span data-ttu-id="f0a42-122">需求</span><span class="sxs-lookup"><span data-stu-id="f0a42-122">Requirement</span></span> | <span data-ttu-id="f0a42-123">值</span><span class="sxs-lookup"><span data-stu-id="f0a42-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a42-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0a42-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a42-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="f0a42-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f0a42-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0a42-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a42-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0a42-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f0a42-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="f0a42-128">Namespace</span></span><br/>                | <span data-ttu-id="f0a42-129">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f0a42-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f0a42-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f0a42-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0a42-131"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0a42-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0a42-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f0a42-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0a42-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0a42-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0a42-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0a42-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a42-135">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f0a42-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

