---
description: GetDialogSize 函式會捕獲資源對話方塊的大小。
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: 'GetDialogSize 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979503"
---
# <a name="getdialogsize-function"></a><span data-ttu-id="b2956-103">GetDialogSize 函式</span><span class="sxs-lookup"><span data-stu-id="b2956-103">GetDialogSize function</span></span>

<span data-ttu-id="b2956-104">**GetDialogSize** 函式會捕獲資源對話方塊的大小。</span><span class="sxs-lookup"><span data-stu-id="b2956-104">The **GetDialogSize** function retrieves the size of a resource dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2956-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2956-105">Syntax</span></span>


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a><span data-ttu-id="b2956-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2956-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2956-107">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="b2956-107">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="b2956-108">對話方塊資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2956-108">Dialog box resource identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b2956-109">*pDlgProc*</span><span class="sxs-lookup"><span data-stu-id="b2956-109">*pDlgProc*</span></span> 
</dt> <dd>

<span data-ttu-id="b2956-110">對話方塊程式的指標。</span><span class="sxs-lookup"><span data-stu-id="b2956-110">Pointer to the dialog box procedure.</span></span>

</dd> <dt>

<span data-ttu-id="b2956-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2956-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2956-112">傳送 \_ 至暫存對話方塊的 INITDIALOG 訊息中的值，會在建立後立即傳送至暫存對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b2956-112">Value passed in the WM\_INITDIALOG message sent to the temporary dialog box just after it is created.</span></span>

</dd> <dt>

<span data-ttu-id="b2956-113">*pResult*</span><span class="sxs-lookup"><span data-stu-id="b2956-113">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="b2956-114">**大小** 結構的指標，該結構會接收對話方塊的尺寸（以螢幕圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b2956-114">Pointer to a **SIZE** structure that receives the dimensions of the dialog box, in screen pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2956-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2956-115">Return value</span></span>

<span data-ttu-id="b2956-116">如果找到對話方塊資源，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="b2956-116">Returns **TRUE** if the dialog box resource was found, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2956-117">備註</span><span class="sxs-lookup"><span data-stu-id="b2956-117">Remarks</span></span>

<span data-ttu-id="b2956-118">屬性頁可以使用此函式來傳回所需的實際顯示大小。</span><span class="sxs-lookup"><span data-stu-id="b2956-118">Property pages can use this function to return the actual display size they require.</span></span> <span data-ttu-id="b2956-119">大部分的屬性頁都是對話方塊，也就是將對話方塊範本儲存在資源檔中。</span><span class="sxs-lookup"><span data-stu-id="b2956-119">Most property pages are dialog boxes and, as such, have dialog box templates stored in resource files.</span></span> <span data-ttu-id="b2956-120">範本會使用未直接對應至螢幕圖元的對話方塊單位。</span><span class="sxs-lookup"><span data-stu-id="b2956-120">Templates use dialog box units that do not map directly onto screen pixels.</span></span> <span data-ttu-id="b2956-121">但是，屬性頁的 [**GetPageInfo**](cbasepropertypage-getpageinfo.md) 函式必須傳回實際的顯示大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b2956-121">However, a property page's [**GetPageInfo**](cbasepropertypage-getpageinfo.md) function must return the actual display size in pixels.</span></span> <span data-ttu-id="b2956-122">屬性頁可以呼叫 `GetDialogSize` 來計算顯示大小。</span><span class="sxs-lookup"><span data-stu-id="b2956-122">The property page can call `GetDialogSize` to calculate the display size.</span></span>

<span data-ttu-id="b2956-123">此函式會建立對話方塊的臨時實例。</span><span class="sxs-lookup"><span data-stu-id="b2956-123">This function creates a temporary instance of the dialog box.</span></span> <span data-ttu-id="b2956-124">為了避免對話方塊出現在螢幕上，資源檔中的對話方塊範本不應該有 WS \_ VISIBLE 屬性。</span><span class="sxs-lookup"><span data-stu-id="b2956-124">To avoid having the dialog box appear on the screen, the dialog box template in the resource file should not have a WS\_VISIBLE property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2956-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2956-125">Requirements</span></span>



| <span data-ttu-id="b2956-126">需求</span><span class="sxs-lookup"><span data-stu-id="b2956-126">Requirement</span></span> | <span data-ttu-id="b2956-127">值</span><span class="sxs-lookup"><span data-stu-id="b2956-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2956-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b2956-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b2956-129"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b2956-129"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b2956-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2956-130">Library</span></span><br/> | <dl> <span data-ttu-id="b2956-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b2956-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2956-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2956-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2956-133">屬性頁 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="b2956-133">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




