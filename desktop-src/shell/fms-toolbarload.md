---
description: 包含要新增至 [檔案管理員] 工具列之自訂按鈕的相關資訊。 這些按鈕是由檔案管理員延伸模組 DLL 提供。
title: 'FMS_TOOLBARLOAD 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 3a993312b9e365561018459c43dab87afbd3c2b2
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842159"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="755f9-104">FMS \_ TOOLBARLOAD 結構</span><span class="sxs-lookup"><span data-stu-id="755f9-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="755f9-105">包含要新增至 [檔案管理員] 工具列之自訂按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="755f9-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="755f9-106">這些按鈕是由檔案管理員延伸模組 DLL 提供。</span><span class="sxs-lookup"><span data-stu-id="755f9-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="755f9-107">語法</span><span class="sxs-lookup"><span data-stu-id="755f9-107">Syntax</span></span>


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a><span data-ttu-id="755f9-108">成員</span><span class="sxs-lookup"><span data-stu-id="755f9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="755f9-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="755f9-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="755f9-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="755f9-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="755f9-111">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="755f9-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="755f9-112">檔案管理員會在呼叫延伸模組之前設定大小，並且在擴充程式傳回後檢查大小。</span><span class="sxs-lookup"><span data-stu-id="755f9-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="755f9-113">**lpButtons**</span><span class="sxs-lookup"><span data-stu-id="755f9-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="755f9-114">類型： **LPEXT \_ 按鈕**</span><span class="sxs-lookup"><span data-stu-id="755f9-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="755f9-115">[**EXT \_ 按鈕**](ext-button.md)結構陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="755f9-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="755f9-116">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="755f9-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="755f9-117">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="755f9-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="755f9-118">**LpButtons** 成員所指向陣列中的 [**EXT \_ 按鈕**](ext-button.md)結構數目。</span><span class="sxs-lookup"><span data-stu-id="755f9-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="755f9-119">此數位等於要加入至工具列的按鈕和分隔符號數目。</span><span class="sxs-lookup"><span data-stu-id="755f9-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="755f9-120">**cBitmaps**</span><span class="sxs-lookup"><span data-stu-id="755f9-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="755f9-121">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="755f9-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="755f9-122">給定點陣圖所表示的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="755f9-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="755f9-123">**idBitmap**</span><span class="sxs-lookup"><span data-stu-id="755f9-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="755f9-124">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="755f9-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="755f9-125">延伸模組 DLL 的可執行檔中點陣圖資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="755f9-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="755f9-126">點陣圖資源包含 **cBitmaps** 所指定之按鈕數目的影像。</span><span class="sxs-lookup"><span data-stu-id="755f9-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="755f9-127">[檔案管理員] 會載入點陣圖資源，然後使用它來顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="755f9-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="755f9-128">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="755f9-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="755f9-129">類型： **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="755f9-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="755f9-130">點陣圖的控制碼，如果 **idBitmap** 為0，則會使用檔案管理員來取得和顯示按鈕影像。</span><span class="sxs-lookup"><span data-stu-id="755f9-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="755f9-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="755f9-131">Requirements</span></span>



| <span data-ttu-id="755f9-132">需求</span><span class="sxs-lookup"><span data-stu-id="755f9-132">Requirement</span></span> | <span data-ttu-id="755f9-133">值</span><span class="sxs-lookup"><span data-stu-id="755f9-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="755f9-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="755f9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="755f9-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="755f9-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="755f9-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="755f9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="755f9-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="755f9-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="755f9-138">標頭</span><span class="sxs-lookup"><span data-stu-id="755f9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="755f9-139"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="755f9-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="755f9-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="755f9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="755f9-141">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="755f9-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




