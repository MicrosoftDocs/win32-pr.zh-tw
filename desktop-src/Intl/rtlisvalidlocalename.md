---
description: 判斷是否已在作業系統上安裝或支援依名稱指定的地區設定。
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: 'RtlIsValidLocaleName 函式 (Ntrtl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847958"
---
# <a name="rtlisvalidlocalename-function"></a><span data-ttu-id="b3dc2-103">RtlIsValidLocaleName 函式</span><span class="sxs-lookup"><span data-stu-id="b3dc2-103">RtlIsValidLocaleName function</span></span>

<span data-ttu-id="b3dc2-104">判斷是否已在作業系統上安裝或支援依名稱指定的地區設定。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-104">Determines if a locale specified by name is installed or supported on the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="b3dc2-105">這項功能僅適用于 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-105">This function is available for use in Windows Vista only.</span></span> <span data-ttu-id="b3dc2-106">它可能會在後續版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-106">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b3dc2-107">應用程式應該使用 [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-107">Applications should use [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b3dc2-108">語法</span><span class="sxs-lookup"><span data-stu-id="b3dc2-108">Syntax</span></span>


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a><span data-ttu-id="b3dc2-109">參數</span><span class="sxs-lookup"><span data-stu-id="b3dc2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3dc2-110">*>localename* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3dc2-110">*LocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3dc2-111">要驗證的[地區設定名稱](locale-names.md)。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-111">[Locale name](locale-names.md) to validate.</span></span> <span data-ttu-id="b3dc2-112">此參數可指定 [自訂地區](custom-locales.md)設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-112">This parameter can specify the name of a [custom locale](custom-locales.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3dc2-113">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b3dc2-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3dc2-114">指出中性地區設定是否視為有效的旗標。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-114">Flags indicating if neutral locales are considered valid.</span></span> <span data-ttu-id="b3dc2-115">目前唯一定義的旗標是 [地區設定 \_ 允許 \_ 中立](locale-allow-neutral.md)的。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-115">Currently the only defined flag is [LOCALE\_ALLOW\_NEUTRAL](locale-allow-neutral.md).</span></span> <span data-ttu-id="b3dc2-116">預設值為不是。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-116">The default value is that they are not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3dc2-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3dc2-117">Return value</span></span>

<span data-ttu-id="b3dc2-118">如果成功，則傳回非零值，否則傳回0。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-118">Returns a nonzero value if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3dc2-119">備註</span><span class="sxs-lookup"><span data-stu-id="b3dc2-119">Remarks</span></span>

<span data-ttu-id="b3dc2-120">此函數類似于 [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-120">This function is similar to [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span> <span data-ttu-id="b3dc2-121">唯一的差別在於，如果 \_ \_ 設定了 LOCALE 允許中性， **RtlIsValidLocaleName** 會針對對應至中性 (地區設定的名稱傳回 **true** ，例如 "en" ) ，而 [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) 只會針對特定 (地區設定傳回 **true** ，例如 "en-us" ) 。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-121">The only difference is that if LOCALE\_ALLOW\_NEUTRAL is set, **RtlIsValidLocaleName** returns **TRUE** for a name that corresponds to a neutral locale (such as "en"), while [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) returns **TRUE** only for a specific locale (such as "en-US").</span></span> <span data-ttu-id="b3dc2-122">在 Windows Vista 和更新版本中，會使用中性地區設定作為資源載入策略的一部分。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-122">Neutral locales are used as part of the resource loading strategy in Windows Vista and later.</span></span> <span data-ttu-id="b3dc2-123">只有小型的高度特製化應用程式會使用 **RtlIsValidLocaleName** 並設定地區設定 \_ \_ ，因為中性地區設定的用途有限。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-123">Only a small class of highly specialized applications use **RtlIsValidLocaleName** and set LOCALE\_ALLOW\_NEUTRAL, because neutral locales are of very limited use.</span></span> <span data-ttu-id="b3dc2-124">[呼叫「地區設定名稱](calling-the--locale-name--functions.md)」函式中所述的任何函式都不接受中性地區設定做為輸入。</span><span class="sxs-lookup"><span data-stu-id="b3dc2-124">None of the functions described in [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md) accept neutral locales as inputs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3dc2-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3dc2-125">Requirements</span></span>



| <span data-ttu-id="b3dc2-126">需求</span><span class="sxs-lookup"><span data-stu-id="b3dc2-126">Requirement</span></span> | <span data-ttu-id="b3dc2-127">值</span><span class="sxs-lookup"><span data-stu-id="b3dc2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3dc2-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3dc2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b3dc2-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3dc2-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b3dc2-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3dc2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b3dc2-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3dc2-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3dc2-132">標頭</span><span class="sxs-lookup"><span data-stu-id="b3dc2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3dc2-133"><dt>Ntrtl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b3dc2-133"><dt>Ntrtl.h</dt></span></span> </dl>      |
| <span data-ttu-id="b3dc2-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="b3dc2-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3dc2-135"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3dc2-135"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3dc2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b3dc2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3dc2-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3dc2-137"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3dc2-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3dc2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3dc2-139">國家語言支援</span><span class="sxs-lookup"><span data-stu-id="b3dc2-139">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="b3dc2-140">國家語言支援功能</span><span class="sxs-lookup"><span data-stu-id="b3dc2-140">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="b3dc2-141">**IsValidLocaleName**</span><span class="sxs-lookup"><span data-stu-id="b3dc2-141">**IsValidLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




