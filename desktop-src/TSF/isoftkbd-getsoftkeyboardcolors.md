---
title: 'ISoftKbd GetSoftKeyboardColors 方法 (Softkbdc .h) '
description: ISoftKbd GetSoftKeyboardColors 方法會抓取與所提供色彩類型對應的軟鍵盤色彩。
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- GetSoftKeyboardColors 方法文字服務架構
- GetSoftKeyboardColors 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，GetSoftKeyboardColors 方法
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2021
ms.locfileid: "106981715"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a><span data-ttu-id="601a2-106">ISoftKbd：： GetSoftKeyboardColors 方法</span><span class="sxs-lookup"><span data-stu-id="601a2-106">ISoftKbd::GetSoftKeyboardColors method</span></span>

<span data-ttu-id="601a2-107">**ISoftKbd：： GetSoftKeyboardColors** 方法會抓取與所提供色彩類型對應的軟鍵盤色彩。</span><span class="sxs-lookup"><span data-stu-id="601a2-107">The **ISoftKbd::GetSoftKeyboardColors** method retrieves the soft keyboard color corresponding to the supplied color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="601a2-108">語法</span><span class="sxs-lookup"><span data-stu-id="601a2-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a><span data-ttu-id="601a2-109">參數</span><span class="sxs-lookup"><span data-stu-id="601a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="601a2-110">*colorType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="601a2-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601a2-111">值，指定要為軟鍵盤取出的色彩類型。</span><span class="sxs-lookup"><span data-stu-id="601a2-111">A value specifying the color type to retrieve for the soft keyboard.</span></span> <span data-ttu-id="601a2-112">可能的值是針對 [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) 列舉而定義的。</span><span class="sxs-lookup"><span data-stu-id="601a2-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="601a2-113">*lpColor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="601a2-113">*lpColor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="601a2-114">緩衝區的指標，此方法會在其中捕獲指定 RGB 色彩的32位 [**COLORREF**](/windows/desktop/gdi/colorref) 值。</span><span class="sxs-lookup"><span data-stu-id="601a2-114">Pointer to a buffer in which this method retrieves a 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="601a2-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="601a2-115">Return value</span></span>

<span data-ttu-id="601a2-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="601a2-116">This method can return one of these values.</span></span>



| <span data-ttu-id="601a2-117">值</span><span class="sxs-lookup"><span data-stu-id="601a2-117">Value</span></span>                                                                                        | <span data-ttu-id="601a2-118">描述</span><span class="sxs-lookup"><span data-stu-id="601a2-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="601a2-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="601a2-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="601a2-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="601a2-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="601a2-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="601a2-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="601a2-122">其中一個參數無效。</span><span class="sxs-lookup"><span data-stu-id="601a2-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="601a2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="601a2-123">Requirements</span></span>



| <span data-ttu-id="601a2-124">需求</span><span class="sxs-lookup"><span data-stu-id="601a2-124">Requirement</span></span> | <span data-ttu-id="601a2-125">值</span><span class="sxs-lookup"><span data-stu-id="601a2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="601a2-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="601a2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="601a2-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="601a2-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="601a2-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="601a2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="601a2-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="601a2-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="601a2-130">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="601a2-130">Redistributable</span></span><br/>          | <span data-ttu-id="601a2-131">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="601a2-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="601a2-132">標頭</span><span class="sxs-lookup"><span data-stu-id="601a2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="601a2-133"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="601a2-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="601a2-134">Idl</span><span class="sxs-lookup"><span data-stu-id="601a2-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="601a2-135"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="601a2-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="601a2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="601a2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="601a2-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="601a2-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="601a2-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="601a2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601a2-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="601a2-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="601a2-140">**ISoftKbd::SetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="601a2-140">**ISoftKbd::SetSoftKeyboardColors**</span></span>](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[<span data-ttu-id="601a2-141">**COLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="601a2-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="601a2-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="601a2-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

