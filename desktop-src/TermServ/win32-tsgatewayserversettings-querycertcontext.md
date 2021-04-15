---
title: Win32_TSGatewayServerSettings 類別的 QueryCertCoNtext 方法
description: 指出是否已安裝指定的憑證。
ms.assetid: 25d56f72-befd-46b4-84ff-dca748eeaca4
ms.tgt_platform: multiple
keywords:
- QueryCertCoNtext 方法遠端桌面服務
- QueryCertCoNtext 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，QueryCertCoNtext 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.QueryCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e158b348debc610682380d793b66949c5a7648
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466708"
---
# <a name="querycertcontext-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="70962-106">Win32 TSGatewayServerSettings 類別的 QueryCertCoNtext 方法 \_</span><span class="sxs-lookup"><span data-stu-id="70962-106">QueryCertContext method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="70962-107">指出是否已安裝指定的憑證。</span><span class="sxs-lookup"><span data-stu-id="70962-107">Indicates whether the specified certificate is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="70962-108">語法</span><span class="sxs-lookup"><span data-stu-id="70962-108">Syntax</span></span>


```mof
uint32 QueryCertContext(
  [out] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="70962-109">參數</span><span class="sxs-lookup"><span data-stu-id="70962-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70962-110">*CertHash* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="70962-110">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70962-111">RD 閘道伺服器所使用之憑證的雜湊。</span><span class="sxs-lookup"><span data-stu-id="70962-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70962-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="70962-112">Return value</span></span>

<span data-ttu-id="70962-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="70962-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="70962-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="70962-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="70962-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="70962-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70962-116">備註</span><span class="sxs-lookup"><span data-stu-id="70962-116">Remarks</span></span>

<span data-ttu-id="70962-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="70962-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="70962-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="70962-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="70962-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="70962-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="70962-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="70962-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="70962-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="70962-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="70962-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="70962-122">Requirements</span></span>



| <span data-ttu-id="70962-123">需求</span><span class="sxs-lookup"><span data-stu-id="70962-123">Requirement</span></span> | <span data-ttu-id="70962-124">值</span><span class="sxs-lookup"><span data-stu-id="70962-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="70962-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70962-125">Minimum supported client</span></span><br/> | <span data-ttu-id="70962-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="70962-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="70962-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70962-127">Minimum supported server</span></span><br/> | <span data-ttu-id="70962-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70962-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="70962-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="70962-129">Namespace</span></span><br/>                | <span data-ttu-id="70962-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="70962-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="70962-131">MOF</span><span class="sxs-lookup"><span data-stu-id="70962-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70962-132"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="70962-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="70962-133">DLL</span><span class="sxs-lookup"><span data-stu-id="70962-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70962-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70962-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="70962-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70962-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70962-136">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="70962-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

