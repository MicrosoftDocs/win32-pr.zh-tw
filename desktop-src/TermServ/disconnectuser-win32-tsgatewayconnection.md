---
title: 'Win32_TSGatewayConnection 類別的 DisconnectUser 方法 (Tsgauthenticationengine) '
description: 將指定之使用者的所有連接從遠端桌面閘道的 (RD 閘道) 伺服器中斷連線。
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- DisconnectUser 方法遠端桌面服務
- DisconnectUser 方法遠端桌面服務，Win32_TSGatewayConnection 類別
- Win32_TSGatewayConnection 類別遠端桌面服務，DisconnectUser 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e223a2de36ad6c2a6fcabc446fe88cad27dc5da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686070"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="a88e5-106">Win32 TSGatewayConnection 類別的 DisconnectUser 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a88e5-106">DisconnectUser method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="a88e5-107">將指定之使用者的所有連接從遠端桌面閘道的 (RD 閘道) 伺服器中斷連線。</span><span class="sxs-lookup"><span data-stu-id="a88e5-107">Disconnects all connections of the specified user from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88e5-108">語法</span><span class="sxs-lookup"><span data-stu-id="a88e5-108">Syntax</span></span>


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="a88e5-109">參數</span><span class="sxs-lookup"><span data-stu-id="a88e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a88e5-110">使用者 *名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a88e5-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a88e5-111">以 \* Domain \* UserName 格式的使用者名稱， **\\** 其連接會中斷連線。</span><span class="sxs-lookup"><span data-stu-id="a88e5-111">The user name, in \*Domain\***\\**_UserName_ format, whose connections are to be disconnected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a88e5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a88e5-112">Return value</span></span>

<span data-ttu-id="a88e5-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="a88e5-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a88e5-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="a88e5-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a88e5-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="a88e5-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a88e5-116">備註</span><span class="sxs-lookup"><span data-stu-id="a88e5-116">Remarks</span></span>

<span data-ttu-id="a88e5-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a88e5-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a88e5-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="a88e5-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a88e5-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a88e5-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a88e5-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="a88e5-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a88e5-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="a88e5-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a88e5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a88e5-122">Requirements</span></span>



| <span data-ttu-id="a88e5-123">需求</span><span class="sxs-lookup"><span data-stu-id="a88e5-123">Requirement</span></span> | <span data-ttu-id="a88e5-124">值</span><span class="sxs-lookup"><span data-stu-id="a88e5-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a88e5-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a88e5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a88e5-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="a88e5-126">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="a88e5-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a88e5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a88e5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a88e5-128">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="a88e5-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="a88e5-129">Namespace</span></span><br/>                | <span data-ttu-id="a88e5-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="a88e5-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                             |
| <span data-ttu-id="a88e5-131">標頭</span><span class="sxs-lookup"><span data-stu-id="a88e5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a88e5-132"><dt>Tsgauthenticationengine。h</dt></span><span class="sxs-lookup"><span data-stu-id="a88e5-132"><dt>Tsgauthenticationengine.h</dt></span></span> </dl> |
| <span data-ttu-id="a88e5-133">MOF</span><span class="sxs-lookup"><span data-stu-id="a88e5-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a88e5-134"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="a88e5-134"><dt>TSGateway.mof</dt></span></span> </dl>             |
| <span data-ttu-id="a88e5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a88e5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a88e5-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a88e5-136"><dt>AagWmi.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="a88e5-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a88e5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88e5-138">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="a88e5-138">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

