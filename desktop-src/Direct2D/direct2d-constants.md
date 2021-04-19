---
title: Direct2D 常數
description: Direct2D 會定義下列常數清單。
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969994"
---
# <a name="direct2d-constants"></a><span data-ttu-id="ea1ed-103">Direct2D 常數</span><span class="sxs-lookup"><span data-stu-id="ea1ed-103">Direct2D constants</span></span>

<span data-ttu-id="ea1ed-104">下列常數是在 `d2d1effectauthor.h` 、 `d2d1.h` 、 `d2d1_1.h` 和 `d2d1effects_2.h` 標頭檔中宣告的。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-104">The following constants are declared in the `d2d1effectauthor.h`, `d2d1.h`, `d2d1_1.h`, and `d2d1effects_2.h` header files.</span></span>

## <a name="d2d1_append_aligned_element--1"></a><span data-ttu-id="ea1ed-105">D2D1_APPEND_ALIGNED_ELEMENT (-1) </span><span class="sxs-lookup"><span data-stu-id="ea1ed-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span></span>
<span data-ttu-id="ea1ed-106">在封裝輸入配置元素時使用。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-106">Used when packing input layout elements.</span></span> <span data-ttu-id="ea1ed-107">它指出元素必須連續封裝。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-107">It indicates that the elements must be packed contiguously.</span></span>

## <a name="d2d1_default_flattening_tolerance-025f"></a><span data-ttu-id="ea1ed-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0.25 f) </span><span class="sxs-lookup"><span data-stu-id="ea1ed-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0.25f)</span></span>
<span data-ttu-id="ea1ed-109">幾何壓平合併作業的預設容錯。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-109">The default tolerance for geometric flattening operations.</span></span>

## <a name="d2d1_invalid_property_index-uint_max"></a><span data-ttu-id="ea1ed-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX) </span><span class="sxs-lookup"><span data-stu-id="ea1ed-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span></span>
<span data-ttu-id="ea1ed-111">定義不正確屬性索引。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-111">Defines an invalid property index.</span></span>

<span data-ttu-id="ea1ed-112">從 [**ID2D1Properties：： GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) 傳回這個常數，表示您提供的命名屬性在屬性介面中沒有索引。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-112">This constant is returned from [**ID2D1Properties::GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) to indicate that the named property that you provided doesn't have an index in the property interface.</span></span>

<span data-ttu-id="ea1ed-113">如果您將這個常數傳遞給 [**ID2D1Properties：： GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) 或 [**ID2D1Properties：： GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32))，則呼叫會失敗，而且輸出緩衝區會填入零。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-113">If you pass this constant to [**ID2D1Properties::GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) or [**ID2D1Properties::GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), then the call fails, and the output buffer is zero-filled.</span></span>

## <a name="d2d1_invalid_tag-ulonglong_max"></a><span data-ttu-id="ea1ed-114">D2D1_INVALID_TAG (ULONGLONG_MAX) </span><span class="sxs-lookup"><span data-stu-id="ea1ed-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span></span>
<span data-ttu-id="ea1ed-115">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-115">Reserved; don't use.</span></span>

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a><span data-ttu-id="ea1ed-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0 f) </span><span class="sxs-lookup"><span data-stu-id="ea1ed-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0f)</span></span>
<span data-ttu-id="ea1ed-117">SRGB 或 scRGB 色彩空間用於 SDR 白色或 1.0 f 浮點值的 nits 數目。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-117">The number of nits that sRGB or scRGB color space uses for SDR white, or floating point values of 1.0f.</span></span> <span data-ttu-id="ea1ed-118">只有當色彩空間使用場景參考的亮度時，此值才會是常數， (HDR) 內容的高度動態範圍則為 true。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-118">This value is constant only when the color space uses scene-referred luminance, which is true for high dynamic range (HDR) content.</span></span> <span data-ttu-id="ea1ed-119">如果色彩空間改為使用顯示參考的亮度，則應該從顯示中查詢 SDR 白色層級。</span><span class="sxs-lookup"><span data-stu-id="ea1ed-119">If the color space uses display-referred luminance instead, then the SDR white level should be queried from the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea1ed-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea1ed-120">Requirements</span></span>

| <span data-ttu-id="ea1ed-121">需求</span><span class="sxs-lookup"><span data-stu-id="ea1ed-121">Requirement</span></span> | <span data-ttu-id="ea1ed-122">值</span><span class="sxs-lookup"><span data-stu-id="ea1ed-122">Value</span></span> |
|-|-|
| <span data-ttu-id="ea1ed-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea1ed-123">Minimum supported client</span></span> | <span data-ttu-id="ea1ed-124">Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="ea1ed-124">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="ea1ed-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea1ed-125">Minimum supported server</span></span> | <span data-ttu-id="ea1ed-126">Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea1ed-126">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="ea1ed-127">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="ea1ed-127">Minimum supported phone</span></span> | <span data-ttu-id="ea1ed-128">Windows Phone 8.1 \[ Windows Phone silverlight 8.1 和 Windows 執行階段應用程式 \] ，Windows Phone 8.1 \[ Windows Phone silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea1ed-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\], Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span> |
| <span data-ttu-id="ea1ed-129">標頭</span><span class="sxs-lookup"><span data-stu-id="ea1ed-129">Header</span></span> | <span data-ttu-id="ea1ed-130">d2d1effectauthor .h、d2d1 .h、d2d1_1 .h、d2d1effects_2。h</span><span class="sxs-lookup"><span data-stu-id="ea1ed-130">d2d1effectauthor.h, d2d1.h, d2d1_1.h, d2d1effects_2.h</span></span> |
