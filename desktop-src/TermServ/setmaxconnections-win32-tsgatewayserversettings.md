---
title: Win32_TSGatewayServerSettings 類別的 SetMaxConnections 方法
description: 設定 MaxConnections 和 UnlimitedConnections 屬性，控制遠端桌面閘道 (RD 閘道) 伺服器的允許連接數目上限。
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- SetMaxConnections 方法遠端桌面服務
- SetMaxConnections 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，SetMaxConnections 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e8a2fa18491232a058913fd338bb871b0a98aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967742"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="da325-106">Win32 TSGatewayServerSettings 類別的 SetMaxConnections 方法 \_</span><span class="sxs-lookup"><span data-stu-id="da325-106">SetMaxConnections method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="da325-107">設定 **MaxConnections** 和 **UnlimitedConnections** 屬性，控制遠端桌面閘道 (RD 閘道) 伺服器的允許連接數目上限。</span><span class="sxs-lookup"><span data-stu-id="da325-107">Sets the **MaxConnections** and **UnlimitedConnections** properties, which control the maximum number of allowed connections to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="da325-108">語法</span><span class="sxs-lookup"><span data-stu-id="da325-108">Syntax</span></span>


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a><span data-ttu-id="da325-109">參數</span><span class="sxs-lookup"><span data-stu-id="da325-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da325-110">*連接* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da325-110">*Connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da325-111">此伺服器應接受的連接數目。</span><span class="sxs-lookup"><span data-stu-id="da325-111">Number of connections that this server should accept.</span></span> <span data-ttu-id="da325-112">針對不限數目的連接，請將 *IsUnlimited* 參數設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="da325-112">For an unlimited number of connections, set the *IsUnlimited* parameter to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="da325-113">*IsUnlimited* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da325-113">*IsUnlimited* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da325-114">若為 **True**，則服務的連接不限於特定的數目。</span><span class="sxs-lookup"><span data-stu-id="da325-114">If **True**, connections to the service are not limited to a specific number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da325-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="da325-115">Return value</span></span>

<span data-ttu-id="da325-116">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="da325-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="da325-117">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="da325-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="da325-118">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="da325-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="da325-119">備註</span><span class="sxs-lookup"><span data-stu-id="da325-119">Remarks</span></span>

<span data-ttu-id="da325-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="da325-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="da325-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="da325-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="da325-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="da325-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="da325-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="da325-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="da325-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="da325-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="da325-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="da325-125">Requirements</span></span>



| <span data-ttu-id="da325-126">需求</span><span class="sxs-lookup"><span data-stu-id="da325-126">Requirement</span></span> | <span data-ttu-id="da325-127">值</span><span class="sxs-lookup"><span data-stu-id="da325-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="da325-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da325-128">Minimum supported client</span></span><br/> | <span data-ttu-id="da325-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="da325-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="da325-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da325-130">Minimum supported server</span></span><br/> | <span data-ttu-id="da325-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da325-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="da325-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="da325-132">Namespace</span></span><br/>                | <span data-ttu-id="da325-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="da325-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="da325-134">MOF</span><span class="sxs-lookup"><span data-stu-id="da325-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da325-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="da325-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="da325-136">DLL</span><span class="sxs-lookup"><span data-stu-id="da325-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da325-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da325-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="da325-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da325-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da325-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="da325-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

