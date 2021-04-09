---
title: Win32_TSVirtualIP 類別的 SelectNetworkAdapter 方法
description: 設定要用於 IP 虛擬化之網路介面卡的 MAC 位址。
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- SelectNetworkAdapter 方法遠端桌面服務
- SelectNetworkAdapter 方法遠端桌面服務，Win32_TSVirtualIP 類別
- Win32_TSVirtualIP 類別遠端桌面服務，SelectNetworkAdapter 方法
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934294"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="e1f12-106">Win32 TSVirtualIP 類別的 SelectNetworkAdapter 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e1f12-106">SelectNetworkAdapter method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="e1f12-107">設定要用於 IP 虛擬化之網路介面卡的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="e1f12-107">Sets the MAC address of the network adapter to use for IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f12-108">語法</span><span class="sxs-lookup"><span data-stu-id="e1f12-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="e1f12-109">參數</span><span class="sxs-lookup"><span data-stu-id="e1f12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1f12-110">*NetworkAdapterMacAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e1f12-110">*NetworkAdapterMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1f12-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e1f12-111">Type: **string**</span></span>

<span data-ttu-id="e1f12-112">指定網路介面卡的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="e1f12-112">Specifies the MAC address of the network adapter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1f12-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1f12-113">Return value</span></span>

<span data-ttu-id="e1f12-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e1f12-114">Type: **uint32**</span></span>

<span data-ttu-id="e1f12-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e1f12-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e1f12-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="e1f12-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

<span data-ttu-id="e1f12-117">如果 MAC 位址無效或不存在，或 IP 虛擬化模式為每個會話，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e1f12-117">If the MAC address is invalid or does not exist, or if the IP virtualization mode is per-session, an error is returned.</span></span>

<span data-ttu-id="e1f12-118">如果設定位於群組原則控制之下，則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e1f12-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f12-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1f12-119">Requirements</span></span>



| <span data-ttu-id="e1f12-120">需求</span><span class="sxs-lookup"><span data-stu-id="e1f12-120">Requirement</span></span> | <span data-ttu-id="e1f12-121">值</span><span class="sxs-lookup"><span data-stu-id="e1f12-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f12-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1f12-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e1f12-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="e1f12-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e1f12-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1f12-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e1f12-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e1f12-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e1f12-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="e1f12-126">Namespace</span></span><br/>                | <span data-ttu-id="e1f12-127">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e1f12-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e1f12-128">MOF</span><span class="sxs-lookup"><span data-stu-id="e1f12-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1f12-129"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1f12-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1f12-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e1f12-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1f12-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1f12-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f12-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1f12-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f12-133">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="e1f12-133">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





