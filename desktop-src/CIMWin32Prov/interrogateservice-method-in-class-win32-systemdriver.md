---
description: 要求系統驅動程式服務將其狀態更新至 service manager。
ms.assetid: 350d9044-39fd-436f-ab15-b30324b2b2e9
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別的 InterrogateService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 666a261dfe3fac7dd62e6253c5eb4804b3a55677
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110488"
---
# <a name="interrogateservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="26e1a-103">Win32 >systemdriver 類別的 InterrogateService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="26e1a-103">InterrogateService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="26e1a-104">**InterrogateService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會要求系統驅動程式服務將其狀態更新為 service manager。</span><span class="sxs-lookup"><span data-stu-id="26e1a-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the system driver service update its state to the service manager.</span></span>

<span data-ttu-id="26e1a-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="26e1a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="26e1a-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="26e1a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="26e1a-107">語法</span><span class="sxs-lookup"><span data-stu-id="26e1a-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="26e1a-108">參數</span><span class="sxs-lookup"><span data-stu-id="26e1a-108">Parameters</span></span>

<span data-ttu-id="26e1a-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="26e1a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26e1a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="26e1a-110">Return value</span></span>

<span data-ttu-id="26e1a-111">如果已接受 **InterrogateService** 要求，則傳回 0 (零) 的值，如果要求不受支援則為 1 (一個) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="26e1a-111">Returns a value of 0 (zero) if the **InterrogateService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e1a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="26e1a-112">Requirements</span></span>



| <span data-ttu-id="26e1a-113">需求</span><span class="sxs-lookup"><span data-stu-id="26e1a-113">Requirement</span></span> | <span data-ttu-id="26e1a-114">值</span><span class="sxs-lookup"><span data-stu-id="26e1a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26e1a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26e1a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="26e1a-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26e1a-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26e1a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26e1a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="26e1a-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26e1a-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26e1a-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="26e1a-119">Namespace</span></span><br/>                | <span data-ttu-id="26e1a-120">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="26e1a-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26e1a-121">MOF</span><span class="sxs-lookup"><span data-stu-id="26e1a-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26e1a-122"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="26e1a-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26e1a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="26e1a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26e1a-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26e1a-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e1a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26e1a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e1a-126">**Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="26e1a-126">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> <dt>

<span data-ttu-id="26e1a-127">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="26e1a-127">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="26e1a-128">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="26e1a-128">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

