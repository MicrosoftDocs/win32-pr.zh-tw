---
title: 'ISoftKbd SetSoftKeyboardColors 方法 (Softkbdc .h) '
description: ISoftKbd SetSoftKeyboardColors 方法會為指定的色彩類型設定軟鍵盤色彩。
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- SetSoftKeyboardColors 方法文字服務架構
- SetSoftKeyboardColors 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SetSoftKeyboardColors 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38357331db2440c35ca7557d08c97729fde9c9f0
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2021
ms.locfileid: "106992219"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a><span data-ttu-id="6979a-106">ISoftKbd：： SetSoftKeyboardColors 方法</span><span class="sxs-lookup"><span data-stu-id="6979a-106">ISoftKbd::SetSoftKeyboardColors method</span></span>

<span data-ttu-id="6979a-107">**ISoftKbd：： SetSoftKeyboardColors** 方法會為指定的色彩類型設定軟鍵盤色彩。</span><span class="sxs-lookup"><span data-stu-id="6979a-107">The **ISoftKbd::SetSoftKeyboardColors** method sets the soft keyboard color for the specified color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6979a-108">語法</span><span class="sxs-lookup"><span data-stu-id="6979a-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a><span data-ttu-id="6979a-109">參數</span><span class="sxs-lookup"><span data-stu-id="6979a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6979a-110">*colorType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6979a-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6979a-111">值，指定軟鍵盤的色彩類型。</span><span class="sxs-lookup"><span data-stu-id="6979a-111">A value specifying the color type for the soft keyboard.</span></span> <span data-ttu-id="6979a-112">可能的值是針對 [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) 列舉而定義的。</span><span class="sxs-lookup"><span data-stu-id="6979a-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="6979a-113">*色彩* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6979a-113">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6979a-114">指定 RGB 色彩的32位 [**COLORREF**](/windows/desktop/gdi/colorref) 值。</span><span class="sxs-lookup"><span data-stu-id="6979a-114">A 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6979a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6979a-115">Return value</span></span>

<span data-ttu-id="6979a-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6979a-116">This method can return one of these values.</span></span>



| <span data-ttu-id="6979a-117">值</span><span class="sxs-lookup"><span data-stu-id="6979a-117">Value</span></span>                                                                                        | <span data-ttu-id="6979a-118">描述</span><span class="sxs-lookup"><span data-stu-id="6979a-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6979a-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6979a-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6979a-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="6979a-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="6979a-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6979a-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6979a-122">其中一個參數無效。</span><span class="sxs-lookup"><span data-stu-id="6979a-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6979a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6979a-123">Requirements</span></span>



| <span data-ttu-id="6979a-124">需求</span><span class="sxs-lookup"><span data-stu-id="6979a-124">Requirement</span></span> | <span data-ttu-id="6979a-125">值</span><span class="sxs-lookup"><span data-stu-id="6979a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6979a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6979a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6979a-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6979a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6979a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6979a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6979a-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6979a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6979a-130">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6979a-130">Redistributable</span></span><br/>          | <span data-ttu-id="6979a-131">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="6979a-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="6979a-132">標頭</span><span class="sxs-lookup"><span data-stu-id="6979a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6979a-133"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="6979a-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="6979a-134">Idl</span><span class="sxs-lookup"><span data-stu-id="6979a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6979a-135"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6979a-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="6979a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6979a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6979a-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6979a-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6979a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6979a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6979a-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="6979a-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="6979a-140">**ISoftKbd::GetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="6979a-140">**ISoftKbd::GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[<span data-ttu-id="6979a-141">**COLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="6979a-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="6979a-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="6979a-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

