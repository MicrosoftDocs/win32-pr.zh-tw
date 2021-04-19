---
description: 定義 Uniscribe 字型度量快取。
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: 'SCRIPT_CACHE (Usp10) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988970"
---
# <a name="script_cache"></a><span data-ttu-id="b77ee-103">腳本 \_ 快取</span><span class="sxs-lookup"><span data-stu-id="b77ee-103">SCRIPT\_CACHE</span></span>

<span data-ttu-id="b77ee-104">定義 Uniscribe 字型度量快取。</span><span class="sxs-lookup"><span data-stu-id="b77ee-104">Defines a Uniscribe font metric cache.</span></span>


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a><span data-ttu-id="b77ee-105">備註</span><span class="sxs-lookup"><span data-stu-id="b77ee-105">Remarks</span></span>

<span data-ttu-id="b77ee-106">這是不透明的結構。</span><span class="sxs-lookup"><span data-stu-id="b77ee-106">This is an opaque structure.</span></span> <span data-ttu-id="b77ee-107">應用程式必須 \_ 針對所使用的每個字元樣式，配置和保留一個腳本快取變數。</span><span class="sxs-lookup"><span data-stu-id="b77ee-107">The application must allocate and retain one SCRIPT\_CACHE variable for each character style used.</span></span> <span data-ttu-id="b77ee-108">變數必須初始化為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b77ee-108">The variable must be initialized to **NULL**.</span></span>

<span data-ttu-id="b77ee-109">許多腳本函式都採用硬體裝置內容控制碼和腳本快取 \_ 變數的組合。</span><span class="sxs-lookup"><span data-stu-id="b77ee-109">Many script functions take a combination of a hardware device context handle and a SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="b77ee-110">Uniscribe 會先嘗試使用腳本快取變數來存取字型資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b77ee-110">Uniscribe first attempts to access font data by using the SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="b77ee-111">如果尚未快取所需的資料，它只會檢查硬體裝置內容。</span><span class="sxs-lookup"><span data-stu-id="b77ee-111">It only inspects the hardware device context if the required data is not already cached.</span></span>

<span data-ttu-id="b77ee-112">硬體裝置內容控制碼可傳遞至 Uniscribe 作為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b77ee-112">The hardware device context handle can be passed to Uniscribe as **NULL**.</span></span> <span data-ttu-id="b77ee-113">如果已快取 Uniscribe 所需的資料，則不會存取裝置內容，而且作業會繼續正常運作。</span><span class="sxs-lookup"><span data-stu-id="b77ee-113">If data required by Uniscribe is already cached, the device context is not accessed, and the operation continues normally.</span></span>

<span data-ttu-id="b77ee-114">如果裝置內容傳遞為 **Null** ，而 Uniscribe 需要基於任何原因存取它，Uniscribe 會傳回錯誤碼 E E \_ 擱置。</span><span class="sxs-lookup"><span data-stu-id="b77ee-114">If the device context is passed as **NULL** and Uniscribe needs to access it for any reason, Uniscribe returns the error code E\_PENDING.</span></span> <span data-ttu-id="b77ee-115">這段程式碼會快速傳回，讓應用程式避免耗時的 [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="b77ee-115">This code is returned quickly, allowing the application to avoid time-consuming [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) calls.</span></span>

## <a name="examples"></a><span data-ttu-id="b77ee-116">範例</span><span class="sxs-lookup"><span data-stu-id="b77ee-116">Examples</span></span>

<span data-ttu-id="b77ee-117">下列範例適用于所有採用腳本快取變數的函 \_ 式，以及選擇性的硬體裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="b77ee-117">The following example applies to all functions that take a SCRIPT\_CACHE variable and an optional handle to a hardware device context.</span></span>


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a><span data-ttu-id="b77ee-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b77ee-118">Requirements</span></span>



| <span data-ttu-id="b77ee-119">需求</span><span class="sxs-lookup"><span data-stu-id="b77ee-119">Requirement</span></span> | <span data-ttu-id="b77ee-120">值</span><span class="sxs-lookup"><span data-stu-id="b77ee-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b77ee-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b77ee-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b77ee-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b77ee-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b77ee-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b77ee-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b77ee-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b77ee-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b77ee-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b77ee-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b77ee-126"><dt>Usp10。h</dt></span><span class="sxs-lookup"><span data-stu-id="b77ee-126"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b77ee-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b77ee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b77ee-128">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="b77ee-128">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="b77ee-129">Uniscribe 結構</span><span class="sxs-lookup"><span data-stu-id="b77ee-129">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="b77ee-130">Caching</span><span class="sxs-lookup"><span data-stu-id="b77ee-130">Caching</span></span>](caching.md)
</dt> </dl>

 

 
