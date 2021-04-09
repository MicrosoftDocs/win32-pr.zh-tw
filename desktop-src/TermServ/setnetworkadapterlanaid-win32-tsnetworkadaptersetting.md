---
title: Win32_TSNetworkAdapterSetting 類別的 SetNetworkAdapterLanaID 方法
description: 指定要設定之網路介面卡的局域網路介面卡 (LANA) 號碼。
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- SetNetworkAdapterLanaID 方法遠端桌面服務
- SetNetworkAdapterLanaID 方法遠端桌面服務，Win32_TSNetworkAdapterSetting 類別
- Win32_TSNetworkAdapterSetting 類別遠端桌面服務，SetNetworkAdapterLanaID 方法
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686424"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="a658a-106">Win32 TSNetworkAdapterSetting 類別的 SetNetworkAdapterLanaID 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a658a-106">SetNetworkAdapterLanaID method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="a658a-107">**SetNetworkAdapterLanaID** 方法會指定要設定之網路介面卡的局域網路介面卡 (LANA) 號碼。</span><span class="sxs-lookup"><span data-stu-id="a658a-107">The **SetNetworkAdapterLanaID** method specifies the Local Area Network Adapter (LANA) number of the network adapter to set.</span></span> <span data-ttu-id="a658a-108">如果指定的 LANA 識別碼無效或不存在，就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a658a-108">If the LANA ID specified is not valid or does not exist, an error is returned.</span></span> <span data-ttu-id="a658a-109">可透過列舉 [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)類別中的屬性 **DeviceIDList** 來取得 LANA 識別碼的可用清單。</span><span class="sxs-lookup"><span data-stu-id="a658a-109">The available list of LANA IDs is obtained by enumerating the property **DeviceIDList** in the [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="a658a-110">語法</span><span class="sxs-lookup"><span data-stu-id="a658a-110">Syntax</span></span>


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a><span data-ttu-id="a658a-111">參數</span><span class="sxs-lookup"><span data-stu-id="a658a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a658a-112">*NetworkAdapterLanaID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a658a-112">*NetworkAdapterLanaID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a658a-113">要設定的網路介面卡的 LANA 號碼。</span><span class="sxs-lookup"><span data-stu-id="a658a-113">LANA number of the network adapter to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a658a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a658a-114">Return value</span></span>

<span data-ttu-id="a658a-115">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a658a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a658a-116">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="a658a-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a658a-117">備註</span><span class="sxs-lookup"><span data-stu-id="a658a-117">Remarks</span></span>

<span data-ttu-id="a658a-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="a658a-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a658a-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a658a-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a658a-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="a658a-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a658a-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="a658a-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a658a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a658a-122">Requirements</span></span>



| <span data-ttu-id="a658a-123">需求</span><span class="sxs-lookup"><span data-stu-id="a658a-123">Requirement</span></span> | <span data-ttu-id="a658a-124">值</span><span class="sxs-lookup"><span data-stu-id="a658a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a658a-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a658a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a658a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a658a-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a658a-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a658a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a658a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a658a-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a658a-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="a658a-129">Namespace</span></span><br/>                | <span data-ttu-id="a658a-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="a658a-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a658a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a658a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a658a-132"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="a658a-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a658a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a658a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a658a-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a658a-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a658a-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a658a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a658a-136">**Win32 \_ TSNetworkAdapterSetting**</span><span class="sxs-lookup"><span data-stu-id="a658a-136">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

