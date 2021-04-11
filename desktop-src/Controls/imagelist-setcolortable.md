---
title: ImageList_SetColorTable 函式
description: 設定影像清單的色彩表。
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- ImageList_SetColorTable 函式 Windows 控制項
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14be5f17d83128933a35730a79726b462436e0c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935176"
---
# <a name="imagelist_setcolortable-function"></a><span data-ttu-id="2f5c8-104">ImageList \_ SetColorTable 函式</span><span class="sxs-lookup"><span data-stu-id="2f5c8-104">ImageList\_SetColorTable function</span></span>

<span data-ttu-id="2f5c8-105">設定影像清單的色彩表。</span><span class="sxs-lookup"><span data-stu-id="2f5c8-105">Sets the color table for an image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f5c8-106">語法</span><span class="sxs-lookup"><span data-stu-id="2f5c8-106">Syntax</span></span>


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a><span data-ttu-id="2f5c8-107">參數</span><span class="sxs-lookup"><span data-stu-id="2f5c8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f5c8-108">*himl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f5c8-108">*himl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5c8-109">類型： **HIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="2f5c8-109">Type: **HIMAGELIST**</span></span>

<span data-ttu-id="2f5c8-110">影像清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2f5c8-110">A handle to the image list.</span></span>

</dd> <dt>

<span data-ttu-id="2f5c8-111">*開始* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f5c8-111">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5c8-112">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="2f5c8-112">Type: **int**</span></span>

<span data-ttu-id="2f5c8-113">以零為基礎的色彩表索引，指定要設定的第一個色彩資料表專案。</span><span class="sxs-lookup"><span data-stu-id="2f5c8-113">A zero-based color table index that specifies the first color table entry to set.</span></span>

</dd> <dt>

<span data-ttu-id="2f5c8-114">*len* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f5c8-114">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5c8-115">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="2f5c8-115">Type: **int**</span></span>

<span data-ttu-id="2f5c8-116">要設定的色彩資料表專案數目。</span><span class="sxs-lookup"><span data-stu-id="2f5c8-116">The number of color table entries to set.</span></span>

</dd> <dt>

<span data-ttu-id="2f5c8-117">*prgb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f5c8-117">*prgb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f5c8-118">類型： \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) \** _</span><span class="sxs-lookup"><span data-stu-id="2f5c8-118">Type: \**[**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\** _</span></span>

<span data-ttu-id="2f5c8-119">_Len \* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 結構陣列的指標，其中包含 DIB 色彩表的新色彩資訊。</span><span class="sxs-lookup"><span data-stu-id="2f5c8-119">A pointer to an array of _len\* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structures containing new color information for the color table of the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f5c8-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f5c8-120">Return value</span></span>

<span data-ttu-id="2f5c8-121">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="2f5c8-121">Type: **int**</span></span>

<span data-ttu-id="2f5c8-122">如果函式成功，它會傳回函數所設定的色彩資料表專案數目。</span><span class="sxs-lookup"><span data-stu-id="2f5c8-122">If the function succeeds, it returns the number of color table entries set by the function.</span></span> <span data-ttu-id="2f5c8-123">如果函式失敗，則傳回值小於或等於零。</span><span class="sxs-lookup"><span data-stu-id="2f5c8-123">If the function fails, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f5c8-124">備註</span><span class="sxs-lookup"><span data-stu-id="2f5c8-124">Remarks</span></span>

<span data-ttu-id="2f5c8-125">只有使用 [**Ilc.out \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 或 [**ilc.out \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 旗標建立的影像清單有色彩表。</span><span class="sxs-lookup"><span data-stu-id="2f5c8-125">Only image lists created with the [**ILC\_COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) or [**ILC\_COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) flag have color tables.</span></span> <span data-ttu-id="2f5c8-126">這類影像清單的色彩表通常是藉由複製加入至清單的第一個影像的色彩表來自動設定 (例如，透過 [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) 函數) 如果該影像是 DIB 的話）。</span><span class="sxs-lookup"><span data-stu-id="2f5c8-126">The color table of such an image list is typically set automatically by copying the color table of the first image added to the list (for example, through the [**ImageList\_Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) function) if that image is a DIB.</span></span> <span data-ttu-id="2f5c8-127">如果新增至影像清單的第一個影像不是 DIB，則會使用半色調選擇區的色彩表來 **Ilc.out \_ COLOR8** 影像清單，並使用 VGA 色彩表來 **ilc.out \_ COLOR4**。</span><span class="sxs-lookup"><span data-stu-id="2f5c8-127">If the first image added to the image list is not a DIB, then the color table of the halftone palette is used for **ILC\_COLOR8** image lists and the VGA color table is used for **ILC\_COLOR4**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f5c8-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f5c8-128">Requirements</span></span>



| <span data-ttu-id="2f5c8-129">需求</span><span class="sxs-lookup"><span data-stu-id="2f5c8-129">Requirement</span></span> | <span data-ttu-id="2f5c8-130">值</span><span class="sxs-lookup"><span data-stu-id="2f5c8-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5c8-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f5c8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2f5c8-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f5c8-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="2f5c8-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f5c8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2f5c8-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f5c8-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2f5c8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2f5c8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f5c8-136"><dt>Comctl32.dll (3.51 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2f5c8-136"><dt>Comctl32.dll (version 3.51 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f5c8-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f5c8-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f5c8-138">[色彩表](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="2f5c8-138">[Color Table](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)</span></span>
</dt> </dl>

 

