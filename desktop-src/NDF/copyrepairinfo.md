---
title: 'CopyRepairInfo 函式 (Ndattributils) '
description: 建立 RepairInfo 結構的複本。
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- CopyRepairInfo 函式 NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934157"
---
# <a name="copyrepairinfo-function"></a><span data-ttu-id="df692-104">CopyRepairInfo 函式</span><span class="sxs-lookup"><span data-stu-id="df692-104">CopyRepairInfo function</span></span>

<span data-ttu-id="df692-105">**CopyRepairInfo** 函數會建立一份 [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)結構的複本。</span><span class="sxs-lookup"><span data-stu-id="df692-105">The **CopyRepairInfo** function creates a copy of a [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="df692-106">語法</span><span class="sxs-lookup"><span data-stu-id="df692-106">Syntax</span></span>


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="df692-107">參數</span><span class="sxs-lookup"><span data-stu-id="df692-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df692-108">*目的地* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="df692-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df692-109">類型： \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="df692-109">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="df692-110">要更新的結構。</span><span class="sxs-lookup"><span data-stu-id="df692-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="df692-111">_Source \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df692-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df692-112">類型： \**Const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="df692-112">Type: \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="df692-113">要複製的現有結構。</span><span class="sxs-lookup"><span data-stu-id="df692-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df692-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="df692-114">Return value</span></span>

<span data-ttu-id="df692-115">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="df692-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="df692-116">可能的傳回值包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="df692-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="df692-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="df692-117">Return code</span></span>                                                                                   | <span data-ttu-id="df692-118">Description</span><span class="sxs-lookup"><span data-stu-id="df692-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df692-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="df692-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="df692-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="df692-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="df692-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="df692-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="df692-122">未正確提供一或多個參數。</span><span class="sxs-lookup"><span data-stu-id="df692-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="df692-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="df692-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="df692-124">沒有足夠的記憶體可完成此作業。</span><span class="sxs-lookup"><span data-stu-id="df692-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="df692-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="df692-125">Requirements</span></span>



| <span data-ttu-id="df692-126">需求</span><span class="sxs-lookup"><span data-stu-id="df692-126">Requirement</span></span> | <span data-ttu-id="df692-127">值</span><span class="sxs-lookup"><span data-stu-id="df692-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="df692-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df692-128">Minimum supported client</span></span><br/> | <span data-ttu-id="df692-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df692-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="df692-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df692-130">Minimum supported server</span></span><br/> | <span data-ttu-id="df692-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df692-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="df692-132">標頭</span><span class="sxs-lookup"><span data-stu-id="df692-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="df692-133"><dt>Ndattributils。h</dt></span><span class="sxs-lookup"><span data-stu-id="df692-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df692-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df692-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df692-135">**RepairInfo**</span><span class="sxs-lookup"><span data-stu-id="df692-135">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





