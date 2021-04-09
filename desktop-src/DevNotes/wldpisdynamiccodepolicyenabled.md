---
description: 抓取描述 .NET 動態程式碼之 Device Guard 原則強制狀態的值。
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: 'WldpIsDynamicCodePolicyEnabled 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110069"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a><span data-ttu-id="6d6a2-103">WldpIsDynamicCodePolicyEnabled 函式</span><span class="sxs-lookup"><span data-stu-id="6d6a2-103">WldpIsDynamicCodePolicyEnabled function</span></span>

<span data-ttu-id="6d6a2-104">抓取描述 .NET 動態程式碼之 Device Guard 原則強制狀態的值。</span><span class="sxs-lookup"><span data-stu-id="6d6a2-104">Retrieves a value that describes the Device Guard policy enforcement status for .NET dynamic code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d6a2-105">語法</span><span class="sxs-lookup"><span data-stu-id="6d6a2-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="6d6a2-106">參數</span><span class="sxs-lookup"><span data-stu-id="6d6a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d6a2-107">*isEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6d6a2-107">*isEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d6a2-108">成功時，如果 Device Guard 原則強制執行 .NET 動態程式碼原則，則會傳回 **true** ;否則，會傳回 **false**。</span><span class="sxs-lookup"><span data-stu-id="6d6a2-108">On success, returns **true** if the Device Guard policy enforces .NET Dynamic Code policy; otherwise, returns **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d6a2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d6a2-109">Return value</span></span>

<span data-ttu-id="6d6a2-110">**如果成功，則 \_ 此** 方法會傳回，否則會傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="6d6a2-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d6a2-111">備註</span><span class="sxs-lookup"><span data-stu-id="6d6a2-111">Remarks</span></span>

<span data-ttu-id="6d6a2-112">動態程式碼是指 .NET CRL 動態產生的程式碼。</span><span class="sxs-lookup"><span data-stu-id="6d6a2-112">Dynamic code refers to .NET CRL dynamically-generated code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d6a2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d6a2-113">Requirements</span></span>



| <span data-ttu-id="6d6a2-114">需求</span><span class="sxs-lookup"><span data-stu-id="6d6a2-114">Requirement</span></span> | <span data-ttu-id="6d6a2-115">值</span><span class="sxs-lookup"><span data-stu-id="6d6a2-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6d6a2-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d6a2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6d6a2-117">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d6a2-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6d6a2-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d6a2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6d6a2-119">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d6a2-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6d6a2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6d6a2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d6a2-121"><dt>Wldp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d6a2-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d6a2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6d6a2-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d6a2-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d6a2-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




