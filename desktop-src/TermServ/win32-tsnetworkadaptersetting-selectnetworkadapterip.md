---
title: Win32_TSNetworkAdapterSetting 類別的 SelectNetworkAdapterIP 方法
description: 選取以介面卡的 IP 位址為基礎的網路介面卡。
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- SelectNetworkAdapterIP 方法遠端桌面服務
- SelectNetworkAdapterIP 方法遠端桌面服務，Win32_TSNetworkAdapterSetting 類別
- Win32_TSNetworkAdapterSetting 類別遠端桌面服務，SelectNetworkAdapterIP 方法
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969578"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="c32b1-106">Win32 TSNetworkAdapterSetting 類別的 SelectNetworkAdapterIP 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c32b1-106">SelectNetworkAdapterIP method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="c32b1-107">選取以介面卡的 IP 位址為基礎的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="c32b1-107">Selects a network adapter based on the adapter's IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="c32b1-108">語法</span><span class="sxs-lookup"><span data-stu-id="c32b1-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a><span data-ttu-id="c32b1-109">參數</span><span class="sxs-lookup"><span data-stu-id="c32b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c32b1-110">*NetworkAdapterIP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c32b1-110">*NetworkAdapterIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c32b1-111">要設定之網路介面卡的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c32b1-111">The IP address of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c32b1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c32b1-112">Return value</span></span>

<span data-ttu-id="c32b1-113">如果指定的 IP 位址有效，則傳回零，如果 IP 位址無效或不存在，則傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c32b1-113">Returns zero if the specified IP address is valid, and returns a WMI error code if the IP address is invalid or does not exist.</span></span> <span data-ttu-id="c32b1-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="c32b1-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c32b1-115">備註</span><span class="sxs-lookup"><span data-stu-id="c32b1-115">Remarks</span></span>

<span data-ttu-id="c32b1-116">您可以藉由列舉 [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) 類別的屬性，來取得網路介面卡的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c32b1-116">You can retrieve the IP address of a network adapter by enumerating the properties of the [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) class.</span></span>

<span data-ttu-id="c32b1-117">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c32b1-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c32b1-118">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c32b1-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c32b1-119">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c32b1-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c32b1-120">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="c32b1-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c32b1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c32b1-121">Requirements</span></span>



| <span data-ttu-id="c32b1-122">需求</span><span class="sxs-lookup"><span data-stu-id="c32b1-122">Requirement</span></span> | <span data-ttu-id="c32b1-123">值</span><span class="sxs-lookup"><span data-stu-id="c32b1-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c32b1-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c32b1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c32b1-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c32b1-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c32b1-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c32b1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c32b1-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c32b1-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c32b1-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="c32b1-128">Namespace</span></span><br/>                | <span data-ttu-id="c32b1-129">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="c32b1-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c32b1-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c32b1-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c32b1-131"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="c32b1-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c32b1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c32b1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c32b1-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c32b1-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c32b1-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c32b1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c32b1-135">**Win32 \_ TSNetworkAdapterSetting**</span><span class="sxs-lookup"><span data-stu-id="c32b1-135">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

