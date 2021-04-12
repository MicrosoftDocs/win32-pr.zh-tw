---
title: 'ISoftKbd GetSoftKeyboardPosSize 方法 (Softkbdc .h) '
description: ISoftKbd GetSoftKeyboardPosSize 方法會抓取軟鍵盤的開始位置和大小。
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- GetSoftKeyboardPosSize 方法文字服務架構
- GetSoftKeyboardPosSize 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，GetSoftKeyboardPosSize 方法
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317340"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a><span data-ttu-id="4ca9e-106">ISoftKbd：： GetSoftKeyboardPosSize 方法</span><span class="sxs-lookup"><span data-stu-id="4ca9e-106">ISoftKbd::GetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="4ca9e-107">**ISoftKbd：： GetSoftKeyboardPosSize** 方法會抓取軟鍵盤的開始位置和大小。</span><span class="sxs-lookup"><span data-stu-id="4ca9e-107">The **ISoftKbd::GetSoftKeyboardPosSize** method retrieves the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca9e-108">語法</span><span class="sxs-lookup"><span data-stu-id="4ca9e-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a><span data-ttu-id="4ca9e-109">參數</span><span class="sxs-lookup"><span data-stu-id="4ca9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ca9e-110">*lpStartPoint* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4ca9e-110">*lpStartPoint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca9e-111">緩衝區的指標，此方法會在此位置中抓取 [點](/previous-versions//dd162805(v=vs.85)) 結構，指出軟鍵盤左上角的座標。</span><span class="sxs-lookup"><span data-stu-id="4ca9e-111">Pointer to a buffer in which this method retrieves a [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="4ca9e-112">*lpwidth* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4ca9e-112">*lpwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca9e-113">緩衝區的指標，此方法會在其中抓取軟鍵盤的寬度。</span><span class="sxs-lookup"><span data-stu-id="4ca9e-113">Pointer to a buffer in which this method retrieves the width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="4ca9e-114">*lpheight* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4ca9e-114">*lpheight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ca9e-115">緩衝區的指標，此方法會在其中抓取軟鍵盤的高度。</span><span class="sxs-lookup"><span data-stu-id="4ca9e-115">Pointer to a buffer in which this method retrieves the height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ca9e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ca9e-116">Return value</span></span>

<span data-ttu-id="4ca9e-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4ca9e-117">This method can return one of these values.</span></span>



| <span data-ttu-id="4ca9e-118">值</span><span class="sxs-lookup"><span data-stu-id="4ca9e-118">Value</span></span>                                                                                        | <span data-ttu-id="4ca9e-119">描述</span><span class="sxs-lookup"><span data-stu-id="4ca9e-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4ca9e-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4ca9e-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4ca9e-121">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="4ca9e-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="4ca9e-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4ca9e-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4ca9e-123">其中一個參數無效。</span><span class="sxs-lookup"><span data-stu-id="4ca9e-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4ca9e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ca9e-124">Requirements</span></span>



| <span data-ttu-id="4ca9e-125">需求</span><span class="sxs-lookup"><span data-stu-id="4ca9e-125">Requirement</span></span> | <span data-ttu-id="4ca9e-126">值</span><span class="sxs-lookup"><span data-stu-id="4ca9e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca9e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ca9e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca9e-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ca9e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4ca9e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ca9e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca9e-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ca9e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4ca9e-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4ca9e-131">Redistributable</span></span><br/>          | <span data-ttu-id="4ca9e-132">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="4ca9e-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="4ca9e-133">標頭</span><span class="sxs-lookup"><span data-stu-id="4ca9e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ca9e-134"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ca9e-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="4ca9e-135">Idl</span><span class="sxs-lookup"><span data-stu-id="4ca9e-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ca9e-136"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ca9e-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="4ca9e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4ca9e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ca9e-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ca9e-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ca9e-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ca9e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca9e-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="4ca9e-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="4ca9e-141">**ISoftKbd::SetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="4ca9e-141">**ISoftKbd::SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

