---
title: IDWriteFactory2 GetSystemFontFallback 方法
description: 從系統字型 fallback 清單建立字型回溯物件。
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- GetSystemFontFallback 方法直接寫入
- GetSystemFontFallback 方法 Direct Write，IDWriteFactory2 介面
- IDWriteFactory2 介面 Direct Write，GetSystemFontFallback 方法
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376209"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a><span data-ttu-id="499a4-106">IDWriteFactory2：： GetSystemFontFallback 方法</span><span class="sxs-lookup"><span data-stu-id="499a4-106">IDWriteFactory2::GetSystemFontFallback method</span></span>

<span data-ttu-id="499a4-107">從系統字型 fallback 清單建立字型回溯物件。</span><span class="sxs-lookup"><span data-stu-id="499a4-107">Creates a font fallback object from the system font fallback list.</span></span>

## <a name="syntax"></a><span data-ttu-id="499a4-108">語法</span><span class="sxs-lookup"><span data-stu-id="499a4-108">Syntax</span></span>


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a><span data-ttu-id="499a4-109">參數</span><span class="sxs-lookup"><span data-stu-id="499a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="499a4-110">*fontFallback* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="499a4-110">*fontFallback* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="499a4-111">類型： **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span><span class="sxs-lookup"><span data-stu-id="499a4-111">Type: **[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span></span>

<span data-ttu-id="499a4-112">包含新建立之字型回寫物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="499a4-112">Contains an address of a pointer to the newly created font fallback object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="499a4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="499a4-113">Return value</span></span>

<span data-ttu-id="499a4-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="499a4-114">Type: **HRESULT**</span></span>

<span data-ttu-id="499a4-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="499a4-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="499a4-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="499a4-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="499a4-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="499a4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="499a4-118">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="499a4-118">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

 