---
title: Win32_TerminalServiceSetting 類別的 CreateWinstation 方法
description: 根據接聽程式名稱和 NIC 的唯一組合，建立新的接聽程式堆疊。
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- CreateWinstation 方法遠端桌面服務
- CreateWinstation 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，CreateWinstation 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 112237a00e9e92a2074ee0b95f9964d73f083e43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999601"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="24f81-106">Win32 TerminalServiceSetting 類別的 CreateWinstation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="24f81-106">CreateWinstation method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="24f81-107">**CreateWinstation** 方法會根據接聽程式名稱和 NIC 的唯一組合來建立新的接聽程式堆疊。</span><span class="sxs-lookup"><span data-stu-id="24f81-107">The **CreateWinstation** method creates a new listener stack based on the unique combination of listener name and NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f81-108">語法</span><span class="sxs-lookup"><span data-stu-id="24f81-108">Syntax</span></span>


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a><span data-ttu-id="24f81-109">參數</span><span class="sxs-lookup"><span data-stu-id="24f81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f81-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24f81-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f81-111">接聽程式名稱。</span><span class="sxs-lookup"><span data-stu-id="24f81-111">Listener name.</span></span>

</dd> <dt>

<span data-ttu-id="24f81-112">*WinstaDriverName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24f81-112">*WinstaDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f81-113">Winstation 驅動程式名稱。</span><span class="sxs-lookup"><span data-stu-id="24f81-113">The winstation driver name.</span></span>

</dd> <dt>

<span data-ttu-id="24f81-114">*LanaId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24f81-114">*LanaId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f81-115">NIC 的 NetBIOS 局域網路介面卡 (LANA) 號碼。</span><span class="sxs-lookup"><span data-stu-id="24f81-115">NetBIOS Local Area Network Adapter (LANA) number for the NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f81-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="24f81-116">Return value</span></span>

<span data-ttu-id="24f81-117">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="24f81-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="24f81-118">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="24f81-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="24f81-119">備註</span><span class="sxs-lookup"><span data-stu-id="24f81-119">Remarks</span></span>

<span data-ttu-id="24f81-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="24f81-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="24f81-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="24f81-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="24f81-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="24f81-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="24f81-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="24f81-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="24f81-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="24f81-124">Requirements</span></span>



| <span data-ttu-id="24f81-125">需求</span><span class="sxs-lookup"><span data-stu-id="24f81-125">Requirement</span></span> | <span data-ttu-id="24f81-126">值</span><span class="sxs-lookup"><span data-stu-id="24f81-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24f81-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24f81-127">Minimum supported client</span></span><br/> | <span data-ttu-id="24f81-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24f81-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24f81-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24f81-129">Minimum supported server</span></span><br/> | <span data-ttu-id="24f81-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24f81-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24f81-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="24f81-131">Namespace</span></span><br/>                | <span data-ttu-id="24f81-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="24f81-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="24f81-133">MOF</span><span class="sxs-lookup"><span data-stu-id="24f81-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24f81-134"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="24f81-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="24f81-135">DLL</span><span class="sxs-lookup"><span data-stu-id="24f81-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24f81-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24f81-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24f81-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24f81-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f81-138">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="24f81-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

