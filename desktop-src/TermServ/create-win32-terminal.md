---
title: Win32_Terminal 類別的 Create 方法
description: 使用 Win32 TerminalSetting 類別的屬性和方法，建立具有預設設定的終端機，這些設定可以自訂 \_ 。
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- 建立方法遠端桌面服務
- 建立方法遠端桌面服務、Win32_Terminal 類別
- Win32_Terminal 類別遠端桌面服務，Create 方法
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464592"
---
# <a name="create-method-of-the-win32_terminal-class"></a><span data-ttu-id="13848-106">Win32 終端機類別的 Create 方法 \_</span><span class="sxs-lookup"><span data-stu-id="13848-106">Create method of the Win32\_Terminal class</span></span>

<span data-ttu-id="13848-107">**Create** 方法會建立具有預設設定的終端機，您可以使用 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)類別的屬性和方法來自訂這些設定。</span><span class="sxs-lookup"><span data-stu-id="13848-107">The **Create** method creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span> <span data-ttu-id="13848-108">函數會在成功時傳回零，並在失敗時傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="13848-108">The function returns zero on success and an error on failure.</span></span>

## <a name="syntax"></a><span data-ttu-id="13848-109">語法</span><span class="sxs-lookup"><span data-stu-id="13848-109">Syntax</span></span>


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="13848-110">參數</span><span class="sxs-lookup"><span data-stu-id="13848-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13848-111">*NewTerminalName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13848-111">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13848-112">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="13848-112">Name of the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="13848-113">*傳輸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13848-113">*Transport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13848-114">終端機的傳輸。</span><span class="sxs-lookup"><span data-stu-id="13848-114">Transport for the terminal.</span></span> <span data-ttu-id="13848-115">這是 [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) 類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="13848-115">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="13848-116">*TerminalProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13848-116">*TerminalProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13848-117">終端機的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="13848-117">Protocol for the terminal.</span></span> <span data-ttu-id="13848-118">這是 [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) 類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="13848-118">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13848-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="13848-119">Return value</span></span>

<span data-ttu-id="13848-120">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="13848-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="13848-121">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="13848-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="13848-122">備註</span><span class="sxs-lookup"><span data-stu-id="13848-122">Remarks</span></span>

<span data-ttu-id="13848-123">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="13848-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="13848-124">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="13848-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="13848-125">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="13848-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="13848-126">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="13848-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="13848-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="13848-127">Requirements</span></span>



| <span data-ttu-id="13848-128">需求</span><span class="sxs-lookup"><span data-stu-id="13848-128">Requirement</span></span> | <span data-ttu-id="13848-129">值</span><span class="sxs-lookup"><span data-stu-id="13848-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13848-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13848-130">Minimum supported client</span></span><br/> | <span data-ttu-id="13848-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13848-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13848-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13848-132">Minimum supported server</span></span><br/> | <span data-ttu-id="13848-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13848-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13848-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="13848-134">Namespace</span></span><br/>                | <span data-ttu-id="13848-135">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="13848-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="13848-136">MOF</span><span class="sxs-lookup"><span data-stu-id="13848-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13848-137"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="13848-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="13848-138">DLL</span><span class="sxs-lookup"><span data-stu-id="13848-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13848-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13848-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13848-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13848-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13848-141">**Win32 \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="13848-141">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

