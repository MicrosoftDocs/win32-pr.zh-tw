---
title: ACCELTABLEENTRY 結構
description: 描述個別快速鍵對應表資源中的資料。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- ACCELTABLEENTRY 結構功能表和其他資源
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466885"
---
# <a name="acceltableentry-structure"></a><span data-ttu-id="c35ed-105">ACCELTABLEENTRY 結構</span><span class="sxs-lookup"><span data-stu-id="c35ed-105">ACCELTABLEENTRY structure</span></span>

<span data-ttu-id="c35ed-106">描述個別快速鍵對應表資源中的資料。</span><span class="sxs-lookup"><span data-stu-id="c35ed-106">Describes the data in an individual accelerator table resource.</span></span> <span data-ttu-id="c35ed-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="c35ed-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c35ed-108">語法</span><span class="sxs-lookup"><span data-stu-id="c35ed-108">Syntax</span></span>


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a><span data-ttu-id="c35ed-109">成員</span><span class="sxs-lookup"><span data-stu-id="c35ed-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c35ed-110">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="c35ed-110">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c35ed-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="c35ed-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c35ed-112">描述鍵盤快速鍵特性。</span><span class="sxs-lookup"><span data-stu-id="c35ed-112">Describes keyboard accelerator characteristics.</span></span> <span data-ttu-id="c35ed-113">這個成員可以有一個或多個 Winuser 的值。</span><span class="sxs-lookup"><span data-stu-id="c35ed-113">This member can have one or more of the following values from Winuser.h.</span></span>



| <span data-ttu-id="c35ed-114">值</span><span class="sxs-lookup"><span data-stu-id="c35ed-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="c35ed-115">意義</span><span class="sxs-lookup"><span data-stu-id="c35ed-115">Meaning</span></span>                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <span data-ttu-id="c35ed-116"><dt>**FVIRTKEY**</dt> <dt>TRUE</dt></span><span class="sxs-lookup"><span data-stu-id="c35ed-116"><dt>**FVIRTKEY**</dt> <dt>TRUE</dt></span></span> </dl>    | <span data-ttu-id="c35ed-117">快速鍵是一種 [虛擬金鑰程式碼](/windows/desktop/inputdev/virtual-key-codes)。</span><span class="sxs-lookup"><span data-stu-id="c35ed-117">The accelerator key is a [virtual-key code](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="c35ed-118">如果未指定此旗標，則會假設快速鍵指定 ASCII 字元碼。</span><span class="sxs-lookup"><span data-stu-id="c35ed-118">If this flag is not specified, the accelerator key is assumed to specify an ASCII character code.</span></span> <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <span data-ttu-id="c35ed-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="c35ed-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="c35ed-120">使用快速鍵時，不會反白顯示功能表列上的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="c35ed-120">A menu item on the menu bar is not highlighted when an accelerator is used.</span></span> <span data-ttu-id="c35ed-121">這個屬性已過時，而且只是為了與針對16位 Windows 設計的資源檔回溯相容。</span><span class="sxs-lookup"><span data-stu-id="c35ed-121">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span><br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <span data-ttu-id="c35ed-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="c35ed-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="c35ed-123">只有當使用者按下 SHIFT 鍵時，才會啟用此加速器。</span><span class="sxs-lookup"><span data-stu-id="c35ed-123">The accelerator is activated only if the user presses the SHIFT key.</span></span> <span data-ttu-id="c35ed-124">此旗標只適用于虛擬機器碼。</span><span class="sxs-lookup"><span data-stu-id="c35ed-124">This flag applies only to virtual keys.</span></span> <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <span data-ttu-id="c35ed-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="c35ed-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span></span> </dl>    | <span data-ttu-id="c35ed-126">只有當使用者按下 CTRL 鍵時，才會啟用此加速器。</span><span class="sxs-lookup"><span data-stu-id="c35ed-126">The accelerator is activated only if the user presses the CTRL key.</span></span> <span data-ttu-id="c35ed-127">此旗標只適用于虛擬機器碼。</span><span class="sxs-lookup"><span data-stu-id="c35ed-127">This flag applies only to virtual keys.</span></span> <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <span data-ttu-id="c35ed-128"><dt>**FALT**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="c35ed-128"><dt>**FALT**</dt> <dt>0x10</dt></span></span> </dl>                | <span data-ttu-id="c35ed-129">只有當使用者按下 ALT 鍵時，才會啟用此加速器。</span><span class="sxs-lookup"><span data-stu-id="c35ed-129">The accelerator is activated only if the user presses the ALT key.</span></span> <span data-ttu-id="c35ed-130">此旗標只適用于虛擬機器碼。</span><span class="sxs-lookup"><span data-stu-id="c35ed-130">This flag applies only to virtual keys.</span></span> <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <span data-ttu-id="c35ed-131"><dt>**0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="c35ed-131"><dt>**0x80**</dt></span></span> </dl>                                                                          | <span data-ttu-id="c35ed-132">專案是快速鍵對應表中的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="c35ed-132">The entry is last in an accelerator table.</span></span> <br/>                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="c35ed-133">**wAnsi**</span><span class="sxs-lookup"><span data-stu-id="c35ed-133">**wAnsi**</span></span>
</dt> <dd>

<span data-ttu-id="c35ed-134">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="c35ed-134">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c35ed-135">識別快速鍵的 ANSI 字元值或虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="c35ed-135">An ANSI character value or a virtual-key code that identifies the accelerator key.</span></span>

</dd> <dt>

<span data-ttu-id="c35ed-136">**Wid**</span><span class="sxs-lookup"><span data-stu-id="c35ed-136">**wId**</span></span>
</dt> <dd>

<span data-ttu-id="c35ed-137">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="c35ed-137">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c35ed-138">鍵盤對應鍵的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c35ed-138">An identifier for the keyboard accelerator.</span></span> <span data-ttu-id="c35ed-139">當使用者按下指定的按鍵時，此值會傳遞給視窗程式。</span><span class="sxs-lookup"><span data-stu-id="c35ed-139">This is the value passed to the window procedure when the user presses the specified key.</span></span>

</dd> <dt>

<span data-ttu-id="c35ed-140">**padding**</span><span class="sxs-lookup"><span data-stu-id="c35ed-140">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="c35ed-141">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="c35ed-141">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c35ed-142">插入的位元組數目，以確保此結構在 **DWORD** 界限上對齊。</span><span class="sxs-lookup"><span data-stu-id="c35ed-142">The number of bytes inserted to ensure that the structure is aligned on a **DWORD** boundary.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c35ed-143">備註</span><span class="sxs-lookup"><span data-stu-id="c35ed-143">Remarks</span></span>

<span data-ttu-id="c35ed-144">資源中的所有快速鍵對應表專案都會重複 **ACCELTABLEENTRY** 結構。</span><span class="sxs-lookup"><span data-stu-id="c35ed-144">The **ACCELTABLEENTRY** structure is repeated for all accelerator table entries in the resource.</span></span> <span data-ttu-id="c35ed-145">資料表中的最後一個專案會標示值0x0080。</span><span class="sxs-lookup"><span data-stu-id="c35ed-145">The last entry in the table is flagged with the value 0x0080.</span></span>

<span data-ttu-id="c35ed-146">如果您將資源的長度分割為8，您可以計算資料表中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="c35ed-146">You can compute the number of elements in the table if you divide the length of the resource by eight.</span></span> <span data-ttu-id="c35ed-147">然後，您的應用程式可以隨機存取個別的固定長度專案。</span><span class="sxs-lookup"><span data-stu-id="c35ed-147">Then your application can randomly access the individual fixed-length entries.</span></span>

## <a name="requirements"></a><span data-ttu-id="c35ed-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="c35ed-148">Requirements</span></span>



| <span data-ttu-id="c35ed-149">需求</span><span class="sxs-lookup"><span data-stu-id="c35ed-149">Requirement</span></span> | <span data-ttu-id="c35ed-150">值</span><span class="sxs-lookup"><span data-stu-id="c35ed-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c35ed-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c35ed-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c35ed-152">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c35ed-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c35ed-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c35ed-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c35ed-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c35ed-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c35ed-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c35ed-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="c35ed-156">**參考**</span><span class="sxs-lookup"><span data-stu-id="c35ed-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c35ed-157">**CreateAcceleratorTable**</span><span class="sxs-lookup"><span data-stu-id="c35ed-157">**CreateAcceleratorTable**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

<span data-ttu-id="c35ed-158">**概念**</span><span class="sxs-lookup"><span data-stu-id="c35ed-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c35ed-159">資源</span><span class="sxs-lookup"><span data-stu-id="c35ed-159">Resources</span></span>](resources.md)
</dt> </dl>

 

