---
description: 包含可當地語系化之列印表單的相關資訊。
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: 'FORM_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192597"
---
# <a name="form_info_2-structure"></a><span data-ttu-id="f263c-103">表單 \_ 資訊 \_ 2 結構</span><span class="sxs-lookup"><span data-stu-id="f263c-103">FORM\_INFO\_2 structure</span></span>

<span data-ttu-id="f263c-104">包含可當地語系化之列印表單的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f263c-104">Contains information about a localizable print form.</span></span>

## <a name="syntax"></a><span data-ttu-id="f263c-105">語法</span><span class="sxs-lookup"><span data-stu-id="f263c-105">Syntax</span></span>


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a><span data-ttu-id="f263c-106">成員</span><span class="sxs-lookup"><span data-stu-id="f263c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f263c-107">**旗標**</span><span class="sxs-lookup"><span data-stu-id="f263c-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="f263c-108">表單內容。</span><span class="sxs-lookup"><span data-stu-id="f263c-108">The form properties.</span></span> <span data-ttu-id="f263c-109">下列是已定義的值，但只能設定一個值。</span><span class="sxs-lookup"><span data-stu-id="f263c-109">The following values are defined, but only one can be set.</span></span> <span data-ttu-id="f263c-110">當 [**GetForm**](getform.md)或 [**EnumForms**](enumforms.md)傳回 **表單 \_ INFO \_ 2** 時，**旗標** 會設定為表單資料庫中目前的值。</span><span class="sxs-lookup"><span data-stu-id="f263c-110">When the **FORM\_INFO\_2** is returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md), **Flags** is set to the current value in the forms database.</span></span>



| <span data-ttu-id="f263c-111">值</span><span class="sxs-lookup"><span data-stu-id="f263c-111">Value</span></span>         | <span data-ttu-id="f263c-112">意義</span><span class="sxs-lookup"><span data-stu-id="f263c-112">Meaning</span></span>                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f263c-113">表單 \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="f263c-113">FORM\_USER</span></span>    | <span data-ttu-id="f263c-114">如果設定此位旗標，使用者就會定義表單。</span><span class="sxs-lookup"><span data-stu-id="f263c-114">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="f263c-115">具有此旗標集合的表單是在登錄中定義。</span><span class="sxs-lookup"><span data-stu-id="f263c-115">Forms with this flag set are defined in the registry.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="f263c-116">表單內 \_ 建</span><span class="sxs-lookup"><span data-stu-id="f263c-116">FORM\_BUILTIN</span></span> | <span data-ttu-id="f263c-117">如果設定此位旗標，則表單是多工緩衝處理器的一部分。</span><span class="sxs-lookup"><span data-stu-id="f263c-117">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="f263c-118">具有此旗標設定的表單定義不會出現在登錄中。</span><span class="sxs-lookup"><span data-stu-id="f263c-118">Form definitions with this flag set do not appear in the registry.</span></span> <span data-ttu-id="f263c-119">無法修改內建表單，因此當結構傳遞至 [**AddForm**](addform.md) 或 [**SetForm**](setform.md)時，不應設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="f263c-119">Built-in forms cannot be modified, so this flag should not be set when the structure is passed to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> |
| <span data-ttu-id="f263c-120">表單 \_ 印表機</span><span class="sxs-lookup"><span data-stu-id="f263c-120">FORM\_PRINTER</span></span> | <span data-ttu-id="f263c-121">如果設定了這個位旗標，表單就會與特定的印表機相關聯，而且其定義會出現在登錄中。</span><span class="sxs-lookup"><span data-stu-id="f263c-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="f263c-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="f263c-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="f263c-123">指定表單名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="f263c-123">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="f263c-124">表單名稱不能超過31個字元。</span><span class="sxs-lookup"><span data-stu-id="f263c-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="f263c-125">**大小**</span><span class="sxs-lookup"><span data-stu-id="f263c-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="f263c-126">表單的寬度和高度（以毫米為單位）。</span><span class="sxs-lookup"><span data-stu-id="f263c-126">The width and height of the form in thousandths of millimeters.</span></span>

</dd> <dt>

<span data-ttu-id="f263c-127">**ImageableArea**</span><span class="sxs-lookup"><span data-stu-id="f263c-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="f263c-128">印表機可以列印之頁面區域的寬度和高度（以千為單位）。</span><span class="sxs-lookup"><span data-stu-id="f263c-128">The width and height, in thousandths of millimeters, of the area of the page on which the printer can print.</span></span>

</dd> <dt>

<span data-ttu-id="f263c-129">**pKeyword**</span><span class="sxs-lookup"><span data-stu-id="f263c-129">**pKeyword**</span></span>
</dt> <dd>

<span data-ttu-id="f263c-130">表單的不可當地語系化字串識別碼指標。</span><span class="sxs-lookup"><span data-stu-id="f263c-130">A pointer to a non-localizable string identifier of the form.</span></span> <span data-ttu-id="f263c-131">傳遞至 [**AddForm**](addform.md) 或 [**SetForm**](setform.md)時，這會提供呼叫端在所有地區設定中識別表單的方法。</span><span class="sxs-lookup"><span data-stu-id="f263c-131">When passed to [**AddForm**](addform.md) or [**SetForm**](setform.md), this gives the caller a means of identifying the form in all locales.</span></span>

</dd> <dt>

<span data-ttu-id="f263c-132">**StringType**</span><span class="sxs-lookup"><span data-stu-id="f263c-132">**StringType**</span></span>
</dt> <dd>

<span data-ttu-id="f263c-133">指定如何在執行時間取得表單的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f263c-133">Specifies how a localized display name for the form is obtained at runtime.</span></span> <span data-ttu-id="f263c-134">以下是定義的值。</span><span class="sxs-lookup"><span data-stu-id="f263c-134">The following values are defined.</span></span> <span data-ttu-id="f263c-135">在任何指定的 [**AddForm**](addform.md) 或 [**SetForm**](setform.md)呼叫中只能設定一個。</span><span class="sxs-lookup"><span data-stu-id="f263c-135">Only one can be set in any given call to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> <span data-ttu-id="f263c-136">您 \_ \_ 可以使用 [**GetForm**](getform.md)或 [**EnumForms**](enumforms.md)所傳回的 **表單 \_ INFO \_ 2** (s) 來設定字串 MUIDLL 和字串 LANGPAIR。</span><span class="sxs-lookup"><span data-stu-id="f263c-136">Both STRING\_MUIDLL and STRING\_LANGPAIR can be set in the **FORM\_INFO\_2** (s) returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md).</span></span> <span data-ttu-id="f263c-137">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f263c-137">See Remarks.</span></span>



| <span data-ttu-id="f263c-138">值</span><span class="sxs-lookup"><span data-stu-id="f263c-138">Value</span></span>            | <span data-ttu-id="f263c-139">意義</span><span class="sxs-lookup"><span data-stu-id="f263c-139">Meaning</span></span>                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f263c-140">字串 \_ 無</span><span class="sxs-lookup"><span data-stu-id="f263c-140">STRING\_NONE</span></span>     | <span data-ttu-id="f263c-141">沒有當地語系化的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f263c-141">There is no localized display name.</span></span>                                                                                                                                                            |
| <span data-ttu-id="f263c-142">字串 \_ MUIDLL</span><span class="sxs-lookup"><span data-stu-id="f263c-142">STRING\_MUIDLL</span></span>   | <span data-ttu-id="f263c-143">顯示名稱會從 **pMuiDll** 中指定的 [多語系消費者介面](/windows/desktop/Intl/mui-resource-management)當地語系化的資源 DLL 中解壓縮。</span><span class="sxs-lookup"><span data-stu-id="f263c-143">The display name is extracted from the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resources DLL specified in **pMuiDll**.</span></span> <span data-ttu-id="f263c-144">識別碼位於 **dwResourceId** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f263c-144">The ID is in the **dwResourceId** member.</span></span> |
| <span data-ttu-id="f263c-145">字串 \_ LANGPAIR</span><span class="sxs-lookup"><span data-stu-id="f263c-145">STRING\_LANGPAIR</span></span> | <span data-ttu-id="f263c-146">顯示名稱和語言識別項是由 **pDisplayName** 直接提供，而語言則是由 **wLangId** 所指定。</span><span class="sxs-lookup"><span data-stu-id="f263c-146">The display name and language ID are provided directly by **pDisplayName** and the language is specified by **wLangId**.</span></span>                                                                       |



 

</dd> <dt>

<span data-ttu-id="f263c-147">**pMuiDll**</span><span class="sxs-lookup"><span data-stu-id="f263c-147">**pMuiDll**</span></span>
</dt> <dd>

<span data-ttu-id="f263c-148">包含當地語系化顯示名稱的 [多語系消費者介面](/windows/desktop/Intl/mui-resource-management) 當地語系化資源 DLL。</span><span class="sxs-lookup"><span data-stu-id="f263c-148">The [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resource DLL that contains the localized display name.</span></span>

</dd> <dt>

<span data-ttu-id="f263c-149">**dwResourceId**</span><span class="sxs-lookup"><span data-stu-id="f263c-149">**dwResourceId**</span></span>
</dt> <dd>

<span data-ttu-id="f263c-150">表單在 **pMuiDll** 中的顯示名稱的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f263c-150">The resource ID of the form's display name in **pMuiDll**.</span></span>

</dd> <dt>

<span data-ttu-id="f263c-151">**pDisplayName**</span><span class="sxs-lookup"><span data-stu-id="f263c-151">**pDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="f263c-152">表單的顯示名稱，以 **wLangId** 所指定的語言顯示。</span><span class="sxs-lookup"><span data-stu-id="f263c-152">The form's display name in the language specified by **wLangId**.</span></span>

</dd> <dt>

<span data-ttu-id="f263c-153">**wLangId**</span><span class="sxs-lookup"><span data-stu-id="f263c-153">**wLangId**</span></span>
</dt> <dd>

<span data-ttu-id="f263c-154">**PDisplayName** 的語言。</span><span class="sxs-lookup"><span data-stu-id="f263c-154">The language of the **pDisplayName**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f263c-155">備註</span><span class="sxs-lookup"><span data-stu-id="f263c-155">Remarks</span></span>

<span data-ttu-id="f263c-156">呼叫 [**AddForm**](addform.md) 或 [**SetForm**](setform.md)時：</span><span class="sxs-lookup"><span data-stu-id="f263c-156">On a call to [**AddForm**](addform.md) or [**SetForm**](setform.md):</span></span>

-   <span data-ttu-id="f263c-157">如果 **StringType** 為 STRING \_ NONE，則 **pMuiDll** 和 **pDisplayName** 都必須是 **Null** ，而且 **dwResourceId** 和 **wLangId** 都必須是0。</span><span class="sxs-lookup"><span data-stu-id="f263c-157">If **StringType** is STRING\_NONE, both **pMuiDll** and **pDisplayName** must be **NULL** and both **dwResourceId** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="f263c-158">如果 **StringType** 是字串 \_ MUIDLL，則 **pDisplayName** 必須是 **Null** ，而 **wLangId** 必須是0。</span><span class="sxs-lookup"><span data-stu-id="f263c-158">If **StringType** is STRING\_MUIDLL, **pDisplayName** must be **NULL** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="f263c-159">如果 **StringType** 是字串 \_ LANGPAIR，則 **pMuiDll** 必須是 **Null** ，而 **dwResourceId** 必須是0。</span><span class="sxs-lookup"><span data-stu-id="f263c-159">If **StringType** is STRING\_LANGPAIR, **pMuiDll** must be **NULL** and **dwResourceId** must be 0.</span></span>

<span data-ttu-id="f263c-160">針對 [**GetForm**](getform.md)或 [**EnumForms**](enumforms.md)的呼叫所傳回的 **表單 \_ 資訊 \_ 2** ：</span><span class="sxs-lookup"><span data-stu-id="f263c-160">For a **FORM\_INFO\_2** returned by a call to [**GetForm**](getform.md) or [**EnumForms**](enumforms.md):</span></span>

-   <span data-ttu-id="f263c-161">如果 **StringType** 同時是字串 \_ MUIDLL 和字串 \_ LANGPAIR， **pMuiDll**、 **pDisplayName**、 **dwResourceId** 和 **wLangId** 都會有有效的值。</span><span class="sxs-lookup"><span data-stu-id="f263c-161">If **StringType** is both STRING\_MUIDLL and STRING\_LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId**, and **wLangId** will all have valid values.</span></span>
-   <span data-ttu-id="f263c-162">如果 **StringType** \_ 僅限字串 MUIDLL，則 **pMuiDll** 和 **dwResourceId** 將會有有效的值。</span><span class="sxs-lookup"><span data-stu-id="f263c-162">If **StringType** is STRING\_MUIDLL only, **pMuiDll** and **dwResourceId** will have valid values.</span></span> <span data-ttu-id="f263c-163">**pDisplayName** 會是 **Null** ，而 **wLangId** 將會是0。</span><span class="sxs-lookup"><span data-stu-id="f263c-163">**pDisplayName** will be **NULL** and **wLangId** will be 0.</span></span>
-   <span data-ttu-id="f263c-164">如果 **StringType** \_ 僅限字串 LANGPAIR，則 **pDisplayName** 和 **wLangId** 將會有有效的值。</span><span class="sxs-lookup"><span data-stu-id="f263c-164">If **StringType** is STRING\_LANGPAIR only, **pDisplayName** and **wLangId** will have valid values.</span></span> <span data-ttu-id="f263c-165">**pMuiDll** 會是 **Null** ，而 **dwResourceId** 將會是0。</span><span class="sxs-lookup"><span data-stu-id="f263c-165">**pMuiDll** will be **NULL** and **dwResourceId** will be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f263c-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="f263c-166">Requirements</span></span>



| <span data-ttu-id="f263c-167">需求</span><span class="sxs-lookup"><span data-stu-id="f263c-167">Requirement</span></span> | <span data-ttu-id="f263c-168">值</span><span class="sxs-lookup"><span data-stu-id="f263c-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f263c-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f263c-169">Minimum supported client</span></span><br/> | <span data-ttu-id="f263c-170">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f263c-170">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f263c-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f263c-171">Minimum supported server</span></span><br/> | <span data-ttu-id="f263c-172">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f263c-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f263c-173">標頭</span><span class="sxs-lookup"><span data-stu-id="f263c-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="f263c-174"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f263c-174"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f263c-175">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="f263c-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f263c-176">**\_ 表單 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 表單 \_ 資訊 \_ 2a** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="f263c-176">**\_FORM\_INFO\_2W** (Unicode) and **\_FORM\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="f263c-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f263c-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f263c-178">列印</span><span class="sxs-lookup"><span data-stu-id="f263c-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f263c-179">列印多工緩衝處理器 API 結構</span><span class="sxs-lookup"><span data-stu-id="f263c-179">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f263c-180">多語系使用者介面</span><span class="sxs-lookup"><span data-stu-id="f263c-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[<span data-ttu-id="f263c-181">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="f263c-181">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="f263c-182">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="f263c-182">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="f263c-183">**EnumForms**</span><span class="sxs-lookup"><span data-stu-id="f263c-183">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="f263c-184">**SetForm**</span><span class="sxs-lookup"><span data-stu-id="f263c-184">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

