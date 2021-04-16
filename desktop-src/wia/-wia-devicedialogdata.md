---
description: 定義呼叫裝置對話方塊所需的資料。
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: 'DEVICEDIALOGDATA 結構 (Wiadefd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513432"
---
# <a name="devicedialogdata-structure"></a><span data-ttu-id="d4610-103">DEVICEDIALOGDATA 結構</span><span class="sxs-lookup"><span data-stu-id="d4610-103">DEVICEDIALOGDATA structure</span></span>

<span data-ttu-id="d4610-104">定義呼叫裝置對話方塊所需的資料。</span><span class="sxs-lookup"><span data-stu-id="d4610-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4610-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4610-105">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a><span data-ttu-id="d4610-106">成員</span><span class="sxs-lookup"><span data-stu-id="d4610-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4610-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d4610-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d4610-108">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d4610-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d4610-109">指定此結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d4610-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d4610-110">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="d4610-110">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="d4610-111">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="d4610-111">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="d4610-112">指定對話方塊父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d4610-112">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="d4610-113">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="d4610-113">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="d4610-114">類型： \**[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _</span><span class="sxs-lookup"><span data-stu-id="d4610-114">Type: \**[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\** _</span></span>

</dd> <dd>

<span data-ttu-id="d4610-115">指向 [_ *IWiaItem* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)介面，表示應用程式專案樹狀結構中的有效根專案。</span><span class="sxs-lookup"><span data-stu-id="d4610-115">Points to an [_ *IWiaItem*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="d4610-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d4610-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d4610-117">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d4610-117">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d4610-118">指定一組旗標來控制對話方塊的操作。</span><span class="sxs-lookup"><span data-stu-id="d4610-118">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="d4610-119">可以設定為下列任何值：</span><span class="sxs-lookup"><span data-stu-id="d4610-119">Can be set to any of the following values:</span></span>



| <span data-ttu-id="d4610-120">旗標</span><span class="sxs-lookup"><span data-stu-id="d4610-120">Flag</span></span>                                 | <span data-ttu-id="d4610-121">意義</span><span class="sxs-lookup"><span data-stu-id="d4610-121">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4610-122">0</span><span class="sxs-lookup"><span data-stu-id="d4610-122">0</span></span>                                    | <span data-ttu-id="d4610-123">預設行為。</span><span class="sxs-lookup"><span data-stu-id="d4610-123">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="d4610-124">WIA \_ 裝置 \_ 對話方塊 \_ 單一 \_ 影像</span><span class="sxs-lookup"><span data-stu-id="d4610-124">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="d4610-125">在 [裝置映射取得] 對話方塊中，將影像選取範圍限制為單一影像。</span><span class="sxs-lookup"><span data-stu-id="d4610-125">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="d4610-126">WIA \_ 裝置 \_ 對話方塊 \_ 使用 \_ 一般 \_ UI</span><span class="sxs-lookup"><span data-stu-id="d4610-126">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="d4610-127">使用系統 UI （如果有的話），而不是廠商提供的 UI。</span><span class="sxs-lookup"><span data-stu-id="d4610-127">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="d4610-128">如果系統 UI 無法使用，則會使用廠商 UI。</span><span class="sxs-lookup"><span data-stu-id="d4610-128">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="d4610-129">如果沒有可用的 UI，函數會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="d4610-129">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d4610-130">**lIntent**</span><span class="sxs-lookup"><span data-stu-id="d4610-130">**lIntent**</span></span>
</dt> <dd>

<span data-ttu-id="d4610-131">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="d4610-131">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="d4610-132">指定影像所要代表的資料類型。</span><span class="sxs-lookup"><span data-stu-id="d4610-132">Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="d4610-133">如需影像意圖值的清單，請參閱 [**影像意圖常數**](-wia-imageintentconstants.md)。</span><span class="sxs-lookup"><span data-stu-id="d4610-133">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4610-134">**lItemCount**</span><span class="sxs-lookup"><span data-stu-id="d4610-134">**lItemCount**</span></span>
</dt> <dd>

<span data-ttu-id="d4610-135">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="d4610-135">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="d4610-136">接收 **ppWiaItem** 參數所指定之陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="d4610-136">Receives the number of items in the array indicated by the **ppWiaItem** parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d4610-137">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="d4610-137">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="d4610-138">類型： **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span><span class="sxs-lookup"><span data-stu-id="d4610-138">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span></span>

</dd> <dd>

<span data-ttu-id="d4610-139">接收 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 介面指標陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="d4610-139">Receives the address of an array of pointers to [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4610-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4610-140">Requirements</span></span>



| <span data-ttu-id="d4610-141">需求</span><span class="sxs-lookup"><span data-stu-id="d4610-141">Requirement</span></span> | <span data-ttu-id="d4610-142">值</span><span class="sxs-lookup"><span data-stu-id="d4610-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4610-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4610-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d4610-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4610-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d4610-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4610-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d4610-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4610-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d4610-147">標頭</span><span class="sxs-lookup"><span data-stu-id="d4610-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4610-148"><dt>Wiadefd。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4610-148"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




