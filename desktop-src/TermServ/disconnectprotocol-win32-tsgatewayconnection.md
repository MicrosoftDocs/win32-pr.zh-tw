---
title: Win32_TSGatewayConnection 類別的 DisconnectProtocol 方法
description: 將指定之通訊協定的所有連接從遠端桌面閘道的 (RD 閘道) 伺服器中斷連線。
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- DisconnectProtocol 方法遠端桌面服務
- DisconnectProtocol 方法遠端桌面服務，Win32_TSGatewayConnection 類別
- Win32_TSGatewayConnection 類別遠端桌面服務，DisconnectProtocol 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectProtocol
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a37050cbd622c6fea14b8b4e5dc6a414eaad85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317307"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="d14c1-106">Win32 TSGatewayConnection 類別的 DisconnectProtocol 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d14c1-106">DisconnectProtocol method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="d14c1-107">將指定之通訊協定的所有連接從遠端桌面閘道的 (RD 閘道) 伺服器中斷連線。</span><span class="sxs-lookup"><span data-stu-id="d14c1-107">Disconnects all connections of the specified protocol from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d14c1-108">語法</span><span class="sxs-lookup"><span data-stu-id="d14c1-108">Syntax</span></span>


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="d14c1-109">參數</span><span class="sxs-lookup"><span data-stu-id="d14c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d14c1-110">*ProtocolName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d14c1-110">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d14c1-111">特定連接的通訊協定名稱。</span><span class="sxs-lookup"><span data-stu-id="d14c1-111">The protocol name for a specific connection.</span></span> <span data-ttu-id="d14c1-112">這可以從 **Win32 \_ TSGatewayConnection** 類別的 **ProtocolName** 屬性抓取。</span><span class="sxs-lookup"><span data-stu-id="d14c1-112">This can be retrieved from the **ProtocolName** property of the **Win32\_TSGatewayConnection** class.</span></span>

<dt>

<span data-ttu-id="d14c1-113">有毒</span><span class="sxs-lookup"><span data-stu-id="d14c1-113">"TS"</span></span>
</dt> <dd>

<span data-ttu-id="d14c1-114">RD 閘道伺服器的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d14c1-114">The protocol for the RD Gateway server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d14c1-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d14c1-115">Return value</span></span>

<span data-ttu-id="d14c1-116">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d14c1-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d14c1-117">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="d14c1-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d14c1-118">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="d14c1-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d14c1-119">備註</span><span class="sxs-lookup"><span data-stu-id="d14c1-119">Remarks</span></span>

<span data-ttu-id="d14c1-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="d14c1-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d14c1-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="d14c1-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d14c1-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d14c1-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d14c1-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="d14c1-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d14c1-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="d14c1-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d14c1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d14c1-125">Requirements</span></span>



| <span data-ttu-id="d14c1-126">需求</span><span class="sxs-lookup"><span data-stu-id="d14c1-126">Requirement</span></span> | <span data-ttu-id="d14c1-127">值</span><span class="sxs-lookup"><span data-stu-id="d14c1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d14c1-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d14c1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d14c1-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="d14c1-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d14c1-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d14c1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d14c1-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d14c1-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d14c1-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="d14c1-132">Namespace</span></span><br/>                | <span data-ttu-id="d14c1-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="d14c1-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d14c1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d14c1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d14c1-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="d14c1-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d14c1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d14c1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d14c1-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d14c1-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d14c1-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d14c1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d14c1-139">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="d14c1-139">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

