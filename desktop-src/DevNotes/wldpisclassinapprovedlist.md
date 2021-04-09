---
description: 呼叫程式庫，以驗證是否可以安全地呼叫特定 CLSID。
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: 'WldpIsClassInApprovedList 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110072"
---
# <a name="wldpisclassinapprovedlist-function"></a><span data-ttu-id="f8954-103">WldpIsClassInApprovedList 函式</span><span class="sxs-lookup"><span data-stu-id="f8954-103">WldpIsClassInApprovedList function</span></span>

<span data-ttu-id="f8954-104">呼叫程式庫，以驗證是否可以安全地呼叫特定 **CLSID** 。</span><span class="sxs-lookup"><span data-stu-id="f8954-104">Calls the library to validate if a particular **CLSID** is safe to be called.</span></span> <span data-ttu-id="f8954-105">函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="f8954-105">The function has no associated import library.</span></span> <span data-ttu-id="f8954-106">您必須使用 LoadLibrary 和 GetProcAddress 函數，以動態方式連結至 wldp.dll。</span><span class="sxs-lookup"><span data-stu-id="f8954-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8954-107">語法</span><span class="sxs-lookup"><span data-stu-id="f8954-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f8954-108">參數</span><span class="sxs-lookup"><span data-stu-id="f8954-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8954-109">*classID*</span><span class="sxs-lookup"><span data-stu-id="f8954-109">*classID*</span></span> 
</dt> <dd>

<span data-ttu-id="f8954-110">要檢查是否有核准的 COM 類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8954-110">The COM class ID to check for approval.</span></span>

</dd> <dt>

<span data-ttu-id="f8954-111">*hostInformation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8954-111">*hostInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8954-112">識別要評估之主機的 [**WLDP \_ 主機 \_ 資訊**](wldp-host-information.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="f8954-112">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="f8954-113">*isApproved* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f8954-113">*isApproved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8954-114">成功完成時，如果類別識別碼已核准，則會包含 **TRUE** 。否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f8954-114">On successful completion, contains **TRUE** if the class ID is approved; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f8954-115">*optionalFlags*</span><span class="sxs-lookup"><span data-stu-id="f8954-115">*optionalFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="f8954-116">此參數是保留的，而且必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="f8954-116">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8954-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8954-117">Return value</span></span>

<span data-ttu-id="f8954-118">**如果成功，則 \_ 此** 方法會傳回，否則會傳回失敗碼。</span><span class="sxs-lookup"><span data-stu-id="f8954-118">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8954-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8954-119">Requirements</span></span>



| <span data-ttu-id="f8954-120">需求</span><span class="sxs-lookup"><span data-stu-id="f8954-120">Requirement</span></span> | <span data-ttu-id="f8954-121">值</span><span class="sxs-lookup"><span data-stu-id="f8954-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f8954-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8954-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f8954-123">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8954-123">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f8954-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8954-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f8954-125">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8954-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f8954-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f8954-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8954-127"><dt>Wldp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8954-127"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8954-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f8954-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8954-129"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8954-129"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




