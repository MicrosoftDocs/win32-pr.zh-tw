---
title: Win32_TSGatewayServerSettings 類別的 SetEnforceChannelBinding 方法
description: 設定 EnforceChannelBinding 屬性。
ms.assetid: 8bd64fe7-bad5-44e6-a309-10802d9a8bd4
ms.tgt_platform: multiple
keywords:
- SetEnforceChannelBinding 方法遠端桌面服務
- SetEnforceChannelBinding 方法遠端桌面服務，Win32_TSGatewayServerSettings 類別
- Win32_TSGatewayServerSettings 類別遠端桌面服務，SetEnforceChannelBinding 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetEnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b236341f0fdac31f80f7e7d77aa12a4b22eb9731
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508740"
---
# <a name="setenforcechannelbinding-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="65df1-106">Win32 TSGatewayServerSettings 類別的 SetEnforceChannelBinding 方法 \_</span><span class="sxs-lookup"><span data-stu-id="65df1-106">SetEnforceChannelBinding method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="65df1-107">設定 **EnforceChannelBinding** 屬性。</span><span class="sxs-lookup"><span data-stu-id="65df1-107">Sets the **EnforceChannelBinding** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="65df1-108">語法</span><span class="sxs-lookup"><span data-stu-id="65df1-108">Syntax</span></span>


```mof
uint32 SetEnforceChannelBinding(
  [in] boolean EnforceChannelBinding
);
```



## <a name="parameters"></a><span data-ttu-id="65df1-109">參數</span><span class="sxs-lookup"><span data-stu-id="65df1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65df1-110">*EnforceChannelBinding* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65df1-110">*EnforceChannelBinding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65df1-111">指定新的 **EnforceChannelBinding** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="65df1-111">Specifies the new **EnforceChannelBinding** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65df1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="65df1-112">Return value</span></span>

<span data-ttu-id="65df1-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="65df1-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="65df1-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="65df1-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="65df1-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="65df1-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65df1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="65df1-116">Requirements</span></span>



| <span data-ttu-id="65df1-117">需求</span><span class="sxs-lookup"><span data-stu-id="65df1-117">Requirement</span></span> | <span data-ttu-id="65df1-118">值</span><span class="sxs-lookup"><span data-stu-id="65df1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65df1-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65df1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65df1-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="65df1-120">None supported</span></span><br/>                                                                |
| <span data-ttu-id="65df1-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65df1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65df1-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65df1-122">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="65df1-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="65df1-123">Namespace</span></span><br/>                | <span data-ttu-id="65df1-124">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="65df1-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="65df1-125">MOF</span><span class="sxs-lookup"><span data-stu-id="65df1-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65df1-126"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="65df1-126"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="65df1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="65df1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65df1-128"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65df1-128"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="65df1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65df1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65df1-130">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="65df1-130">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





