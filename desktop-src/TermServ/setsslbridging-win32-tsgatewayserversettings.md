---
title: Win32_TSGatewayServerSettings 類別的 SetSslBridging 方法
description: 設定遠端桌面閘道 (RD 閘道) 伺服器所使用的 SSL 橋接類型。
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- SetSslBridging 方法遠端桌面服務
- SetSslBridging 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，SetSslBridging 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384866"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="b182f-106">Win32 TSGatewayServerSettings 類別的 SetSslBridging 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b182f-106">SetSslBridging method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="b182f-107">設定遠端桌面閘道 (RD 閘道) 伺服器所使用的 SSL 橋接類型。</span><span class="sxs-lookup"><span data-stu-id="b182f-107">Sets the type of SSL bridging to be used by the Remote Desktop Gateway (RD Gateway) server.</span></span> <span data-ttu-id="b182f-108">此值會儲存在 **SslBridging** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="b182f-108">This value is stored in the **SslBridging** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b182f-109">使用這個方法變更 SSL 橋接類型時，必須重新開機 RD 閘道服務，才能讓此變更生效。</span><span class="sxs-lookup"><span data-stu-id="b182f-109">When the SSL bridging type is changed with this method, the RD Gateway service must be restarted to make this change take effect.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b182f-110">語法</span><span class="sxs-lookup"><span data-stu-id="b182f-110">Syntax</span></span>


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a><span data-ttu-id="b182f-111">參數</span><span class="sxs-lookup"><span data-stu-id="b182f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b182f-112">*SslBridging* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b182f-112">*SslBridging* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b182f-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b182f-113">Type: **uint32**</span></span>

<span data-ttu-id="b182f-114">指定新的 SSL 橋接值。</span><span class="sxs-lookup"><span data-stu-id="b182f-114">Specifies the new SSL bridging value.</span></span> <span data-ttu-id="b182f-115">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b182f-115">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="b182f-116">0</span><span class="sxs-lookup"><span data-stu-id="b182f-116">0</span></span>
</dt> <dd>

<span data-ttu-id="b182f-117">無 SSL 橋接。</span><span class="sxs-lookup"><span data-stu-id="b182f-117">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="b182f-118">1</span><span class="sxs-lookup"><span data-stu-id="b182f-118">1</span></span>
</dt> <dd>

<span data-ttu-id="b182f-119">HTTPS 至 HTTP 橋接。</span><span class="sxs-lookup"><span data-stu-id="b182f-119">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="b182f-120">2</span><span class="sxs-lookup"><span data-stu-id="b182f-120">2</span></span>
</dt> <dd>

<span data-ttu-id="b182f-121">HTTPS 至 HTTPS 橋接。</span><span class="sxs-lookup"><span data-stu-id="b182f-121">HTTPS to HTTPS bridging.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b182f-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="b182f-122">Return value</span></span>

<span data-ttu-id="b182f-123">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b182f-123">Type: **uint32**</span></span>

<span data-ttu-id="b182f-124">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="b182f-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b182f-125">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="b182f-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b182f-126">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="b182f-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b182f-127">備註</span><span class="sxs-lookup"><span data-stu-id="b182f-127">Remarks</span></span>

<span data-ttu-id="b182f-128">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b182f-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b182f-129">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="b182f-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b182f-130">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b182f-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b182f-131">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b182f-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b182f-132">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="b182f-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b182f-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b182f-133">Requirements</span></span>



| <span data-ttu-id="b182f-134">需求</span><span class="sxs-lookup"><span data-stu-id="b182f-134">Requirement</span></span> | <span data-ttu-id="b182f-135">值</span><span class="sxs-lookup"><span data-stu-id="b182f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b182f-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b182f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b182f-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="b182f-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b182f-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b182f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b182f-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b182f-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="b182f-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="b182f-140">Namespace</span></span><br/>                | <span data-ttu-id="b182f-141">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="b182f-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b182f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b182f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b182f-143"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="b182f-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b182f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b182f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b182f-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b182f-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b182f-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b182f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b182f-147">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="b182f-147">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

