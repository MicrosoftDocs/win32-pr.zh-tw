---
title: Win32_Terminal 類別的 Delete 方法
description: 刪除指定的終端機。
ms.assetid: 59d8cc73-aef1-49d2-a7a2-dd3cbe5a8c52
ms.tgt_platform: multiple
keywords:
- Delete 方法遠端桌面服務
- Delete 方法遠端桌面服務，Win32_Terminal 類別
- Win32_Terminal 類別遠端桌面服務，Delete 方法
topic_type:
- apiref
api_name:
- Win32_Terminal.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b7120c78eada2b047f836219d3382e5ce1e2f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001099"
---
# <a name="delete-method-of-the-win32_terminal-class"></a><span data-ttu-id="2e97b-106">Win32 終端機類別的 Delete 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2e97b-106">Delete method of the Win32\_Terminal class</span></span>

<span data-ttu-id="2e97b-107">**Delete** 方法會刪除指定的終端機。</span><span class="sxs-lookup"><span data-stu-id="2e97b-107">The **Delete** method deletes the specified terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e97b-108">語法</span><span class="sxs-lookup"><span data-stu-id="2e97b-108">Syntax</span></span>


```mof
uint32 Delete(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a><span data-ttu-id="2e97b-109">參數</span><span class="sxs-lookup"><span data-stu-id="2e97b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e97b-110">*NewTerminalName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e97b-110">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e97b-111">要刪除的終端機名稱。</span><span class="sxs-lookup"><span data-stu-id="2e97b-111">Name of the terminal to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e97b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e97b-112">Return value</span></span>

<span data-ttu-id="2e97b-113">成功時傳回0，否則會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2e97b-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2e97b-114">如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="2e97b-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e97b-115">備註</span><span class="sxs-lookup"><span data-stu-id="2e97b-115">Remarks</span></span>

<span data-ttu-id="2e97b-116">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="2e97b-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2e97b-117">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2e97b-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2e97b-118">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="2e97b-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2e97b-119">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="2e97b-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e97b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e97b-120">Requirements</span></span>



| <span data-ttu-id="2e97b-121">需求</span><span class="sxs-lookup"><span data-stu-id="2e97b-121">Requirement</span></span> | <span data-ttu-id="2e97b-122">值</span><span class="sxs-lookup"><span data-stu-id="2e97b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e97b-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e97b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2e97b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e97b-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e97b-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e97b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2e97b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e97b-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e97b-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="2e97b-127">Namespace</span></span><br/>                | <span data-ttu-id="2e97b-128">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="2e97b-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2e97b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="2e97b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e97b-130"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e97b-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e97b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2e97b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e97b-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e97b-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e97b-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e97b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e97b-134">**Win32 \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="2e97b-134">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

