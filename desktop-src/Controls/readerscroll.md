---
title: ReaderScroll 回呼函式
description: 應用程式定義的回呼函式，當滑鼠指標在已宣告為使用中捲動區域的讀取器強制回應視窗部分內移動時，就會使用這個函數。
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- ReaderScroll 回呼函式 Windows 控制項
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934313"
---
# <a name="readerscroll-callback-function"></a><span data-ttu-id="93efe-104">ReaderScroll 回呼函式</span><span class="sxs-lookup"><span data-stu-id="93efe-104">ReaderScroll callback function</span></span>

<span data-ttu-id="93efe-105">\[*ReaderScroll* 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="93efe-105">\[*ReaderScroll* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="93efe-106">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="93efe-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="93efe-107">應用程式定義的回呼函式，當滑鼠指標在已宣告為使用中捲動區域的讀取器強制回應視窗部分內移動時，就會使用這個函數。</span><span class="sxs-lookup"><span data-stu-id="93efe-107">An application-defined callback function used when the mouse pointer is moved within the portion of the reader mode window that has been declared as the active scrolling area.</span></span>

## <a name="syntax"></a><span data-ttu-id="93efe-108">語法</span><span class="sxs-lookup"><span data-stu-id="93efe-108">Syntax</span></span>


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a><span data-ttu-id="93efe-109">參數</span><span class="sxs-lookup"><span data-stu-id="93efe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93efe-110">*prmi* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93efe-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93efe-111">類型： **PREADERMODEINFO**</span><span class="sxs-lookup"><span data-stu-id="93efe-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="93efe-112">傳遞給 [**DoReaderMode**](doreadermode.md)函數的 [**READERMODEINFO**](readermodeinfo.md)結構指標。</span><span class="sxs-lookup"><span data-stu-id="93efe-112">A pointer to the [**READERMODEINFO**](readermodeinfo.md) structure that was passed to the [**DoReaderMode**](doreadermode.md) function.</span></span> <span data-ttu-id="93efe-113">此結構會定義讀取器強制回應視窗和現用捲動區域。</span><span class="sxs-lookup"><span data-stu-id="93efe-113">This structure defines the reader mode window and the active scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="93efe-114"> \[ 中的 dx\]</span><span class="sxs-lookup"><span data-stu-id="93efe-114">*dx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93efe-115">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="93efe-115">Type: **int**</span></span>

<span data-ttu-id="93efe-116">水準滾動的距離。</span><span class="sxs-lookup"><span data-stu-id="93efe-116">The distance to scroll horizontally.</span></span> <span data-ttu-id="93efe-117">如果在 \_ [**READERMODEINFO**](readermodeinfo.md) 結構中設定 RMF VERTICALONLY 旗標，則此值一律為0。</span><span class="sxs-lookup"><span data-stu-id="93efe-117">If the RMF\_VERTICALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> <dt>

<span data-ttu-id="93efe-118">*dy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93efe-118">*dy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93efe-119">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="93efe-119">Type: **int**</span></span>

<span data-ttu-id="93efe-120">要垂直捲動的距離。</span><span class="sxs-lookup"><span data-stu-id="93efe-120">The distance to scroll vertically.</span></span> <span data-ttu-id="93efe-121">如果在 \_ [**READERMODEINFO**](readermodeinfo.md) 結構中設定 RMF HORIZONTALONLY 旗標，則此值一律為0。</span><span class="sxs-lookup"><span data-stu-id="93efe-121">If the RMF\_HORIZONTALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93efe-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="93efe-122">Return value</span></span>

<span data-ttu-id="93efe-123">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="93efe-123">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="93efe-124">此函數應該一律傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="93efe-124">This function should always return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="93efe-125">備註</span><span class="sxs-lookup"><span data-stu-id="93efe-125">Remarks</span></span>

<span data-ttu-id="93efe-126">當應用程式收到來自此函式的通知時，應用程式會負責以 *dx* 和 *dy* 參數所指定的方向來滾動讀取器強制回應視窗。</span><span class="sxs-lookup"><span data-stu-id="93efe-126">When the application receives notification from this function, the application is responsible for scrolling the reader mode window in the direction specified by the *dx* and *dy* parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="93efe-127">範例</span><span class="sxs-lookup"><span data-stu-id="93efe-127">Examples</span></span>

<span data-ttu-id="93efe-128">下列範例概述使用自訂函式完成滾動的函式執行。</span><span class="sxs-lookup"><span data-stu-id="93efe-128">The following example outlines an implementation of this function using a custom function to accomplish the scrolling.</span></span>


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a><span data-ttu-id="93efe-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="93efe-129">Requirements</span></span>



| <span data-ttu-id="93efe-130">需求</span><span class="sxs-lookup"><span data-stu-id="93efe-130">Requirement</span></span> | <span data-ttu-id="93efe-131">值</span><span class="sxs-lookup"><span data-stu-id="93efe-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="93efe-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93efe-132">Minimum supported client</span></span><br/> | <span data-ttu-id="93efe-133">Windows Vista、Windows Vista \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93efe-133">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="93efe-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93efe-134">Minimum supported server</span></span><br/> | <span data-ttu-id="93efe-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93efe-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

