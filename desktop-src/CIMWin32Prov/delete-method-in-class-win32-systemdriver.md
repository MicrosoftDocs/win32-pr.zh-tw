---
description: Delete Win32_SystemDriver 類別的方法-刪除&\# 8194;WMI 類別方法會刪除現有的服務。
ms.assetid: 5e437d36-3582-448c-b568-45f7fb13b096
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別的 Delete 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1b7435a1bca561b19e7d85299413f88f1ae76c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097086"
---
# <a name="delete-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="9e2a3-103">Win32 >systemdriver 類別的 Delete 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9e2a3-103">Delete method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="9e2a3-104">**Delete** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會刪除現有的服務。</span><span class="sxs-lookup"><span data-stu-id="9e2a3-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="9e2a3-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="9e2a3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9e2a3-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="9e2a3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e2a3-107">語法</span><span class="sxs-lookup"><span data-stu-id="9e2a3-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="9e2a3-108">參數</span><span class="sxs-lookup"><span data-stu-id="9e2a3-108">Parameters</span></span>

<span data-ttu-id="9e2a3-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9e2a3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e2a3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e2a3-110">Return value</span></span>

<span data-ttu-id="9e2a3-111">如果成功刪除服務，則傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指出錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="9e2a3-111">Returns a value of 0 (zero) if the service was successfully deleted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e2a3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e2a3-112">Requirements</span></span>



| <span data-ttu-id="9e2a3-113">需求</span><span class="sxs-lookup"><span data-stu-id="9e2a3-113">Requirement</span></span> | <span data-ttu-id="9e2a3-114">值</span><span class="sxs-lookup"><span data-stu-id="9e2a3-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2a3-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e2a3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9e2a3-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e2a3-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e2a3-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e2a3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9e2a3-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e2a3-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e2a3-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="9e2a3-119">Namespace</span></span><br/>                | <span data-ttu-id="9e2a3-120">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9e2a3-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e2a3-121">MOF</span><span class="sxs-lookup"><span data-stu-id="9e2a3-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e2a3-122"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e2a3-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e2a3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9e2a3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e2a3-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e2a3-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e2a3-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e2a3-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e2a3-126">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e2a3-126">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9e2a3-127">**Win32 \_ >systemdriver**</span><span class="sxs-lookup"><span data-stu-id="9e2a3-127">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

