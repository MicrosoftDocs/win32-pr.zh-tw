---
title: Win32_TSGatewayServerSettings 類別的 GetProtocolName 方法
description: 傳回指定之通訊協定索引的通訊協定名稱。
ms.assetid: 6778cede-cc61-4e5d-9a29-ba88197fa8c6
ms.tgt_platform: multiple
keywords:
- GetProtocolName 方法遠端桌面服務
- GetProtocolName 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，GetProtocolName 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetProtocolName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81064581b209f047ac492faee6d442b082d038cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104333"
---
# <a name="getprotocolname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="99c7c-106">Win32 TSGatewayServerSettings 類別的 GetProtocolName 方法 \_</span><span class="sxs-lookup"><span data-stu-id="99c7c-106">GetProtocolName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="99c7c-107">傳回指定之通訊協定索引的通訊協定名稱。</span><span class="sxs-lookup"><span data-stu-id="99c7c-107">Returns the protocol name for the specified protocol index.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c7c-108">語法</span><span class="sxs-lookup"><span data-stu-id="99c7c-108">Syntax</span></span>


```mof
uint32 GetProtocolName(
  [in]  uint32 ProtocolId,
  [out] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="99c7c-109">參數</span><span class="sxs-lookup"><span data-stu-id="99c7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c7c-110">*ProtocolId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99c7c-110">*ProtocolId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c7c-111">通訊協定識別碼的索引。</span><span class="sxs-lookup"><span data-stu-id="99c7c-111">Index of the protocol identifier.</span></span> <span data-ttu-id="99c7c-112">值必須介於零到 **MaxProtocols** 屬性的值之間。</span><span class="sxs-lookup"><span data-stu-id="99c7c-112">The value must be between zero and the value of the **MaxProtocols** property.</span></span>

</dd> <dt>

<span data-ttu-id="99c7c-113">*ProtocolName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="99c7c-113">*ProtocolName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99c7c-114">傳回指定之通訊協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="99c7c-114">Returns the name of the specified protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c7c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="99c7c-115">Return value</span></span>

<span data-ttu-id="99c7c-116">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="99c7c-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="99c7c-117">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="99c7c-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="99c7c-118">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="99c7c-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="99c7c-119">備註</span><span class="sxs-lookup"><span data-stu-id="99c7c-119">Remarks</span></span>

<span data-ttu-id="99c7c-120">支援一個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="99c7c-120">One protocol is supported.</span></span>

<span data-ttu-id="99c7c-121">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="99c7c-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="99c7c-122">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="99c7c-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="99c7c-123">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="99c7c-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="99c7c-124">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="99c7c-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="99c7c-125">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="99c7c-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="99c7c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="99c7c-126">Requirements</span></span>



| <span data-ttu-id="99c7c-127">需求</span><span class="sxs-lookup"><span data-stu-id="99c7c-127">Requirement</span></span> | <span data-ttu-id="99c7c-128">值</span><span class="sxs-lookup"><span data-stu-id="99c7c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c7c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99c7c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="99c7c-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="99c7c-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="99c7c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99c7c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="99c7c-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99c7c-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="99c7c-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="99c7c-133">Namespace</span></span><br/>                | <span data-ttu-id="99c7c-134">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="99c7c-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="99c7c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="99c7c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99c7c-136"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="99c7c-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="99c7c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="99c7c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99c7c-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99c7c-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="99c7c-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99c7c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c7c-140">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="99c7c-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

