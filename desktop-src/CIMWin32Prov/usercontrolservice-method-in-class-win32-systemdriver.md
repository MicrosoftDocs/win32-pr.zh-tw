---
description: 嘗試傳送使用者定義的控制項程式碼至系統驅動程式所管理的服務。
ms.assetid: 62e66c35-f264-43d0-9e94-fb5e85f936e0
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別的 UserControlService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99974206f6487d90e1660f5a64c1d00904912c66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936457"
---
# <a name="usercontrolservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="95d13-103">Win32 >systemdriver 類別的 UserControlService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="95d13-103">UserControlService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="95d13-104">**UserControlService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將使用者定義的控制項程式碼傳送至系統驅動程式所管理的服務。</span><span class="sxs-lookup"><span data-stu-id="95d13-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service managed by a system driver.</span></span>

<span data-ttu-id="95d13-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="95d13-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="95d13-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="95d13-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="95d13-107">語法</span><span class="sxs-lookup"><span data-stu-id="95d13-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="95d13-108">參數</span><span class="sxs-lookup"><span data-stu-id="95d13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d13-109">*ControlCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95d13-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d13-110">指定從128到 255) 的定義值，這些 (值會提供使用者特定的控制項命令。</span><span class="sxs-lookup"><span data-stu-id="95d13-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d13-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95d13-111">Return value</span></span>

<span data-ttu-id="95d13-112">如果已接受 **UserControlService** 要求，則傳回 0 (零) 的值，如果要求不受支援則為 1 (一個) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="95d13-112">Returns a value of 0 (zero) if the **UserControlService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d13-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="95d13-113">Requirements</span></span>



| <span data-ttu-id="95d13-114">需求</span><span class="sxs-lookup"><span data-stu-id="95d13-114">Requirement</span></span> | <span data-ttu-id="95d13-115">值</span><span class="sxs-lookup"><span data-stu-id="95d13-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95d13-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95d13-116">Minimum supported client</span></span><br/> | <span data-ttu-id="95d13-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95d13-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95d13-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95d13-118">Minimum supported server</span></span><br/> | <span data-ttu-id="95d13-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95d13-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95d13-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="95d13-120">Namespace</span></span><br/>                | <span data-ttu-id="95d13-121">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="95d13-121">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95d13-122">MOF</span><span class="sxs-lookup"><span data-stu-id="95d13-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95d13-123"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="95d13-123"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95d13-124">DLL</span><span class="sxs-lookup"><span data-stu-id="95d13-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d13-125"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d13-125"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d13-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95d13-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="95d13-127">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95d13-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="95d13-128">**Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="95d13-128">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

