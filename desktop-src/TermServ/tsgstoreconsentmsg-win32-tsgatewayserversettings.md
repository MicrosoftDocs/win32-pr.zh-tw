---
title: Win32_TSGatewayServerSettings 類別的 TSGStoreConsentMsg 方法
description: 更新閘道伺服器的同意訊息。
ms.assetid: b3146d87-95af-4b6b-8c02-5ac4748fbe98
ms.tgt_platform: multiple
keywords:
- TSGStoreConsentMsg 方法遠端桌面服務
- TSGStoreConsentMsg 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，TSGStoreConsentMsg 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907097739d21e1523aca3b719cdb5f18b6f3fa30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465557"
---
# <a name="tsgstoreconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="eb9bb-106">Win32 TSGatewayServerSettings 類別的 TSGStoreConsentMsg 方法 \_</span><span class="sxs-lookup"><span data-stu-id="eb9bb-106">TSGStoreConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="eb9bb-107">更新閘道伺服器的同意訊息。</span><span class="sxs-lookup"><span data-stu-id="eb9bb-107">Updates the consent message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9bb-108">語法</span><span class="sxs-lookup"><span data-stu-id="eb9bb-108">Syntax</span></span>


```mof
uint32 TSGStoreConsentMsg(
  [in] string TSGConMsgText
);
```



## <a name="parameters"></a><span data-ttu-id="eb9bb-109">參數</span><span class="sxs-lookup"><span data-stu-id="eb9bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb9bb-110">*TSGConMsgText* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb9bb-110">*TSGConMsgText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9bb-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb9bb-111">Type: **string**</span></span>

<span data-ttu-id="eb9bb-112">同意郵件內文。</span><span class="sxs-lookup"><span data-stu-id="eb9bb-112">The consent message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb9bb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb9bb-113">Return value</span></span>

<span data-ttu-id="eb9bb-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="eb9bb-114">Type: **uint32**</span></span>

<span data-ttu-id="eb9bb-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="eb9bb-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="eb9bb-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="eb9bb-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="eb9bb-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="eb9bb-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eb9bb-118">備註</span><span class="sxs-lookup"><span data-stu-id="eb9bb-118">Remarks</span></span>

<span data-ttu-id="eb9bb-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="eb9bb-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="eb9bb-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="eb9bb-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eb9bb-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="eb9bb-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eb9bb-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="eb9bb-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eb9bb-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="eb9bb-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9bb-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb9bb-124">Requirements</span></span>



| <span data-ttu-id="eb9bb-125">需求</span><span class="sxs-lookup"><span data-stu-id="eb9bb-125">Requirement</span></span> | <span data-ttu-id="eb9bb-126">值</span><span class="sxs-lookup"><span data-stu-id="eb9bb-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9bb-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb9bb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eb9bb-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="eb9bb-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="eb9bb-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb9bb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eb9bb-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eb9bb-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="eb9bb-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="eb9bb-131">Namespace</span></span><br/>                | <span data-ttu-id="eb9bb-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="eb9bb-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="eb9bb-133">MOF</span><span class="sxs-lookup"><span data-stu-id="eb9bb-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb9bb-134"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb9bb-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb9bb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="eb9bb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb9bb-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb9bb-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="eb9bb-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb9bb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9bb-138">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="eb9bb-138">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

