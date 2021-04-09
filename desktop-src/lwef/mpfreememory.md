---
title: 'MpFreeMemory 函式 (MpClient) '
description: 釋出 malware protection manager 的記憶體。
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- MpFreeMemory 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685785"
---
# <a name="mpfreememory-function"></a><span data-ttu-id="9be71-104">MpFreeMemory 函式</span><span class="sxs-lookup"><span data-stu-id="9be71-104">MpFreeMemory function</span></span>

<span data-ttu-id="9be71-105">釋出 malware protection manager 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9be71-105">Frees memory for the malware protection manager.</span></span> <span data-ttu-id="9be71-106">惡意程式碼防護函式所配置和傳回的所有緩衝區都必須由呼叫者使用此函式釋放。</span><span class="sxs-lookup"><span data-stu-id="9be71-106">All buffers allocated and returned by malware protection functions must be freed by the caller using this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be71-107">語法</span><span class="sxs-lookup"><span data-stu-id="9be71-107">Syntax</span></span>


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="9be71-108">參數</span><span class="sxs-lookup"><span data-stu-id="9be71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9be71-109">*pMemory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9be71-109">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be71-110">類型： **PVOID**</span><span class="sxs-lookup"><span data-stu-id="9be71-110">Type: **PVOID**</span></span>

<span data-ttu-id="9be71-111">惡意程式碼防護功能所配置之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="9be71-111">A pointer to memory allocated by a malware protection function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9be71-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9be71-112">Return value</span></span>

<span data-ttu-id="9be71-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9be71-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9be71-114">備註</span><span class="sxs-lookup"><span data-stu-id="9be71-114">Remarks</span></span>

<span data-ttu-id="9be71-115">為了加速用戶端的記憶體管理，malware protection manager 也會定義宏來釋出與惡意程式碼防護功能所傳回之各種結構相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9be71-115">To facilitate memory management for clients, the malware protection manager also defines macros to free memory associated with various structures returned by malware protection functions.</span></span> <span data-ttu-id="9be71-116">下列巨集定義在標頭檔 mpmemfree 中：</span><span class="sxs-lookup"><span data-stu-id="9be71-116">The following macros are defined in the header file mpmemfree.h:</span></span>



| <span data-ttu-id="9be71-117">Name</span><span class="sxs-lookup"><span data-stu-id="9be71-117">Name</span></span>                            | <span data-ttu-id="9be71-118">描述</span><span class="sxs-lookup"><span data-stu-id="9be71-118">Description</span></span>                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9be71-119">\_免費 MPRESOURCE 資訊 \_</span><span class="sxs-lookup"><span data-stu-id="9be71-119">MPRESOURCE\_INFO\_FREE</span></span>          | <span data-ttu-id="9be71-120">釋出已配置的 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。</span><span class="sxs-lookup"><span data-stu-id="9be71-120">Frees an allocated [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>                  |
| <span data-ttu-id="9be71-121">\_免費 MPTHREAT 資訊 \_</span><span class="sxs-lookup"><span data-stu-id="9be71-121">MPTHREAT\_INFO\_FREE</span></span>            | <span data-ttu-id="9be71-122">釋出已配置的 [**MPTHREAT \_ 資訊**](mpthreat-info.md)。</span><span class="sxs-lookup"><span data-stu-id="9be71-122">Frees an allocated [**MPTHREAT\_INFO**](mpthreat-info.md).</span></span>                      |
| <span data-ttu-id="9be71-123">\_免費 MPTHREAT 當地語系化 \_ 資訊 \_</span><span class="sxs-lookup"><span data-stu-id="9be71-123">MPTHREAT\_LOCALIZED\_INFO\_FREE</span></span> | <span data-ttu-id="9be71-124">釋出已配置的 [**MPTHREAT \_ 當地語系化 \_ 資訊**](mpthreat-localized-info.md)。</span><span class="sxs-lookup"><span data-stu-id="9be71-124">Frees an allocated [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9be71-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9be71-125">Requirements</span></span>



| <span data-ttu-id="9be71-126">需求</span><span class="sxs-lookup"><span data-stu-id="9be71-126">Requirement</span></span> | <span data-ttu-id="9be71-127">值</span><span class="sxs-lookup"><span data-stu-id="9be71-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9be71-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9be71-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9be71-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9be71-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9be71-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9be71-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9be71-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9be71-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9be71-132">標頭</span><span class="sxs-lookup"><span data-stu-id="9be71-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9be71-133"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="9be71-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9be71-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9be71-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9be71-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9be71-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9be71-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9be71-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be71-137">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="9be71-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="9be71-138">**MPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="9be71-138">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="9be71-139">**MPTHREAT \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="9be71-139">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="9be71-140">**MPTHREAT \_ 當地語系化的 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="9be71-140">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





