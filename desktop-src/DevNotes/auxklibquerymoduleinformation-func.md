---
description: 抓取系統目前載入之模組集的相關資訊。
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: 'AuxKlibQueryModuleInformation function (Aux \_ klib .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992820"
---
# <a name="auxklibquerymoduleinformation-function"></a><span data-ttu-id="db5d6-103">AuxKlibQueryModuleInformation 函式</span><span class="sxs-lookup"><span data-stu-id="db5d6-103">AuxKlibQueryModuleInformation function</span></span>

<span data-ttu-id="db5d6-104">抓取系統目前載入之模組集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="db5d6-104">Retrieves information about the currently loaded set of modules for the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="db5d6-105">語法</span><span class="sxs-lookup"><span data-stu-id="db5d6-105">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a><span data-ttu-id="db5d6-106">參數</span><span class="sxs-lookup"><span data-stu-id="db5d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db5d6-107">*BufferSize* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="db5d6-107">*BufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="db5d6-108">在輸入時， *QueryInfo* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="db5d6-108">On input, the size of the *QueryInfo* buffer, in bytes.</span></span> <span data-ttu-id="db5d6-109">在輸出時，會接收實際所需的大小。</span><span class="sxs-lookup"><span data-stu-id="db5d6-109">On output, receives the actual required size.</span></span> <span data-ttu-id="db5d6-110">由於系統模組清單可以在呼叫之間變更，因此此值也可以在呼叫之間變更。</span><span class="sxs-lookup"><span data-stu-id="db5d6-110">Because the system module list can change between calls, this value can also change between calls.</span></span>

</dd> <dt>

<span data-ttu-id="db5d6-111">*ElementSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db5d6-111">*ElementSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db5d6-112">陣列元素的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="db5d6-112">The size, in bytes, of an array element.</span></span> <span data-ttu-id="db5d6-113">此大小會決定輸出的格式。</span><span class="sxs-lookup"><span data-stu-id="db5d6-113">This size determines the format of the output.</span></span>

</dd> <dt>

<span data-ttu-id="db5d6-114">*QueryInfo* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="db5d6-114">*QueryInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db5d6-115">接收模組資訊的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="db5d6-115">A pointer to a buffer that receives the module information.</span></span> <span data-ttu-id="db5d6-116">這項資訊會在陣列中傳回，而陣列的元素是下列其中一個結構： [**AUX \_ module \_ 基本 \_ 資訊**](aux-module-basic-info-struct.md) 或 [**aux \_ 模組 \_ 延伸 \_ 資訊**](aux-module-extended-info-struct.md)。</span><span class="sxs-lookup"><span data-stu-id="db5d6-116">This information is returned in an array whose elements are one of the following structures: [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) or [**AUX\_MODULE\_EXTENDED\_INFO**](aux-module-extended-info-struct.md).</span></span> <span data-ttu-id="db5d6-117">使用的特定結構取決於指定的元素大小。</span><span class="sxs-lookup"><span data-stu-id="db5d6-117">The specific structure used depends on the specified element size.</span></span>

<span data-ttu-id="db5d6-118">如果此參數為 **Null**，則函式會傳回所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="db5d6-118">If this parameter is **NULL**, the function returns the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db5d6-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="db5d6-119">Return value</span></span>

<span data-ttu-id="db5d6-120">如果函式成功，則傳回值為「狀態 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="db5d6-120">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="db5d6-121">如果函式失敗，則傳回值可以是在 WDK 中定義的其中一個狀態碼，也就是在 WDK 中可用。</span><span class="sxs-lookup"><span data-stu-id="db5d6-121">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="db5d6-122">備註</span><span class="sxs-lookup"><span data-stu-id="db5d6-122">Remarks</span></span>

<span data-ttu-id="db5d6-123">呼叫此函式之前，您必須先呼叫 [**AuxKlibInitialize**](auxklibinitialize-func.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="db5d6-123">You must call the [**AuxKlibInitialize**](auxklibinitialize-func.md) function before calling this function.</span></span>

<span data-ttu-id="db5d6-124">您可以從 [這裡](https://www.microsoft.com/?ref=go)下載可執行此 API 的物件程式庫。</span><span class="sxs-lookup"><span data-stu-id="db5d6-124">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="db5d6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="db5d6-125">Requirements</span></span>



| <span data-ttu-id="db5d6-126">需求</span><span class="sxs-lookup"><span data-stu-id="db5d6-126">Requirement</span></span> | <span data-ttu-id="db5d6-127">值</span><span class="sxs-lookup"><span data-stu-id="db5d6-127">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db5d6-128">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="db5d6-128">Redistributable</span></span><br/> | <span data-ttu-id="db5d6-129">Windows 輔助 API 程式庫1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="db5d6-129">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="db5d6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="db5d6-130">Header</span></span><br/>          | <dl> <span data-ttu-id="db5d6-131"><dt>Aux \_ klib。h</dt></span><span class="sxs-lookup"><span data-stu-id="db5d6-131"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="db5d6-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="db5d6-132">Library</span></span><br/>         | <dl> <span data-ttu-id="db5d6-133"><dt>Aux \_ klib .lib</dt></span><span class="sxs-lookup"><span data-stu-id="db5d6-133"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db5d6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db5d6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5d6-135">**AuxKlibInitialize**</span><span class="sxs-lookup"><span data-stu-id="db5d6-135">**AuxKlibInitialize**</span></span>](auxklibinitialize-func.md)
</dt> <dt>

[<span data-ttu-id="db5d6-136">**AUX \_ 模組 \_ 基本 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="db5d6-136">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> <dt>

[<span data-ttu-id="db5d6-137">**AUX \_ 模組 \_ 擴充 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="db5d6-137">**AUX\_MODULE\_EXTENDED\_INFO**</span></span>](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




