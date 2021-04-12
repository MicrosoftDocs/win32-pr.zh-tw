---
title: Win32_TerminalServiceSetting 類別的 SetProfilePath 方法
description: SetProfilePath 方法會設定類別的 ProfilePath 屬性。
ms.assetid: a0dfe6a4-929c-45ec-bd31-7e0ffb6ce5de
ms.tgt_platform: multiple
keywords:
- SetProfilePath 方法遠端桌面服務
- SetProfilePath 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetProfilePath 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetProfilePath
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 434909471accc191e79c92287ab6e4ac427bf949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384542"
---
# <a name="setprofilepath-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="23f6e-106">Win32 TerminalServiceSetting 類別的 SetProfilePath 方法 \_</span><span class="sxs-lookup"><span data-stu-id="23f6e-106">SetProfilePath method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="23f6e-107">**SetProfilePath** 方法會設定類別的 **ProfilePath** 屬性。</span><span class="sxs-lookup"><span data-stu-id="23f6e-107">The **SetProfilePath** method sets the **ProfilePath** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f6e-108">語法</span><span class="sxs-lookup"><span data-stu-id="23f6e-108">Syntax</span></span>


```mof
uint32 SetProfilePath(
  [in] string ProfilePath
);
```



## <a name="parameters"></a><span data-ttu-id="23f6e-109">參數</span><span class="sxs-lookup"><span data-stu-id="23f6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f6e-110">*ProfilePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23f6e-110">*ProfilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f6e-111">**ProfilePath** 屬性的新值，這個值會指定電腦的設定檔路徑。</span><span class="sxs-lookup"><span data-stu-id="23f6e-111">The new value for the **ProfilePath** property, which specifies the profile path for the computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f6e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="23f6e-112">Return value</span></span>

<span data-ttu-id="23f6e-113">成功時傳回成功，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="23f6e-113">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="23f6e-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="23f6e-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="23f6e-115">備註</span><span class="sxs-lookup"><span data-stu-id="23f6e-115">Remarks</span></span>

<span data-ttu-id="23f6e-116">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="23f6e-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="23f6e-117">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="23f6e-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="23f6e-118">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="23f6e-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="23f6e-119">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="23f6e-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="23f6e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="23f6e-120">Requirements</span></span>



| <span data-ttu-id="23f6e-121">需求</span><span class="sxs-lookup"><span data-stu-id="23f6e-121">Requirement</span></span> | <span data-ttu-id="23f6e-122">值</span><span class="sxs-lookup"><span data-stu-id="23f6e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23f6e-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23f6e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="23f6e-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23f6e-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23f6e-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23f6e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="23f6e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23f6e-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23f6e-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="23f6e-127">Namespace</span></span><br/>                | <span data-ttu-id="23f6e-128">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="23f6e-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="23f6e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="23f6e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23f6e-130"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="23f6e-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="23f6e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="23f6e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23f6e-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23f6e-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23f6e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23f6e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f6e-134">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="23f6e-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

