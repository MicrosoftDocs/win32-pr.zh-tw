---
title: Win32_TSNetworkAdapterSetting 類別的 SelectAllNetworkAdapters 方法
description: SelectAllNetworkAdapters 方法會選取所有網路介面卡。
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- SelectAllNetworkAdapters 方法遠端桌面服務
- SelectAllNetworkAdapters 方法遠端桌面服務，Win32_TSNetworkAdapterSetting 類別
- Win32_TSNetworkAdapterSetting 類別遠端桌面服務，SelectAllNetworkAdapters 方法
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectAllNetworkAdapters
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f68245c30fbdbf0721d138d1fc0386c779efe111
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317323"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="9f00f-106">Win32 TSNetworkAdapterSetting 類別的 SelectAllNetworkAdapters 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9f00f-106">SelectAllNetworkAdapters method of the Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="9f00f-107">**SelectAllNetworkAdapters** 方法會選取所有網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="9f00f-107">The **SelectAllNetworkAdapters** method selects all network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f00f-108">語法</span><span class="sxs-lookup"><span data-stu-id="9f00f-108">Syntax</span></span>


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a><span data-ttu-id="9f00f-109">參數</span><span class="sxs-lookup"><span data-stu-id="9f00f-109">Parameters</span></span>

<span data-ttu-id="9f00f-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9f00f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f00f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f00f-111">Return value</span></span>

<span data-ttu-id="9f00f-112">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9f00f-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9f00f-113">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="9f00f-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f00f-114">備註</span><span class="sxs-lookup"><span data-stu-id="9f00f-114">Remarks</span></span>

<span data-ttu-id="9f00f-115">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="9f00f-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9f00f-116">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9f00f-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9f00f-117">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="9f00f-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9f00f-118">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="9f00f-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f00f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f00f-119">Requirements</span></span>



| <span data-ttu-id="9f00f-120">需求</span><span class="sxs-lookup"><span data-stu-id="9f00f-120">Requirement</span></span> | <span data-ttu-id="9f00f-121">值</span><span class="sxs-lookup"><span data-stu-id="9f00f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f00f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f00f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9f00f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f00f-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f00f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f00f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9f00f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f00f-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f00f-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="9f00f-126">Namespace</span></span><br/>                | <span data-ttu-id="9f00f-127">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="9f00f-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9f00f-128">MOF</span><span class="sxs-lookup"><span data-stu-id="9f00f-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f00f-129"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f00f-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f00f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9f00f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f00f-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f00f-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f00f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f00f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f00f-133">**Win32 \_ TSNetworkAdapterSetting**</span><span class="sxs-lookup"><span data-stu-id="9f00f-133">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

