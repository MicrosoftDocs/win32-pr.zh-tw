---
description: PROPERTYINST 結構會在一段可辨識的資料中定義屬性的實例。 當屬性附加至 capture 時，網路監視器會配置並填入 PROPERTYINST 結構。
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: 'PROPERTYINST 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ee4ba108b8231646a2c0749dee6b5cc9f0f21c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977042"
---
# <a name="propertyinst-structure"></a><span data-ttu-id="c55b9-104">PROPERTYINST 結構</span><span class="sxs-lookup"><span data-stu-id="c55b9-104">PROPERTYINST structure</span></span>

<span data-ttu-id="c55b9-105">**PROPERTYINST** 結構會在一段可辨識的資料中定義屬性的實例。</span><span class="sxs-lookup"><span data-stu-id="c55b9-105">The **PROPERTYINST** structure defines an instance of a property in a piece of recognized data.</span></span> <span data-ttu-id="c55b9-106">當屬性附加至 capture 時，網路監視器會配置並填入 **PROPERTYINST** 結構。</span><span class="sxs-lookup"><span data-stu-id="c55b9-106">Network Monitor allocates and fills in a **PROPERTYINST** structure when a property is attached to the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55b9-107">語法</span><span class="sxs-lookup"><span data-stu-id="c55b9-107">Syntax</span></span>


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a><span data-ttu-id="c55b9-108">成員</span><span class="sxs-lookup"><span data-stu-id="c55b9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c55b9-109">**lpPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="c55b9-109">**lpPropertyInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-110">定義屬性之 [PROPERTYINFO](propertyinfo.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c55b9-110">Pointer to the [PROPERTYINFO](propertyinfo.md) structure that defines the property.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-111">**szPropertyText**</span><span class="sxs-lookup"><span data-stu-id="c55b9-111">**szPropertyText**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-112">在網路監視器 UI 的詳細資料窗格中顯示之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="c55b9-112">Pointer to a string that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-113">**lpData**</span><span class="sxs-lookup"><span data-stu-id="c55b9-113">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-114">屬性之資料開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="c55b9-114">Pointer to the start of the data for the property.</span></span> <span data-ttu-id="c55b9-115">剖析器會決定屬性資料的開始位置。</span><span class="sxs-lookup"><span data-stu-id="c55b9-115">The parser determines where the property data starts.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-116">**lpByte**</span><span class="sxs-lookup"><span data-stu-id="c55b9-116">**lpByte**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-117">**位元組** 資料的指標。</span><span class="sxs-lookup"><span data-stu-id="c55b9-117">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-118">**lpWord**</span><span class="sxs-lookup"><span data-stu-id="c55b9-118">**lpWord**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-119">**文字** 資料的指標。</span><span class="sxs-lookup"><span data-stu-id="c55b9-119">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-120">**lpDword**</span><span class="sxs-lookup"><span data-stu-id="c55b9-120">**lpDword**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-121">**DWORD** 資料的指標。</span><span class="sxs-lookup"><span data-stu-id="c55b9-121">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-122">**lpLargeInt**</span><span class="sxs-lookup"><span data-stu-id="c55b9-122">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-123">[**LARGEINT**](largeint.md)資料的指標。</span><span class="sxs-lookup"><span data-stu-id="c55b9-123">Pointer to the [**LARGEINT**](largeint.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-124">**lpSysTime**</span><span class="sxs-lookup"><span data-stu-id="c55b9-124">**lpSysTime**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-125">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)資料的指標。</span><span class="sxs-lookup"><span data-stu-id="c55b9-125">Pointer to the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) data.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-126">**lpPropertyInstEx**</span><span class="sxs-lookup"><span data-stu-id="c55b9-126">**lpPropertyInstEx**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-127">[PROPERTYINSTEX](propertyinstex.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c55b9-127">Pointer to a [PROPERTYINSTEX](propertyinstex.md) structure.</span></span> <span data-ttu-id="c55b9-128">只有在呼叫 [AttachPropertyInstanceEx](attachpropertyinstanceex.md)時，才會使用 **lpPropertyInstEx** 成員。</span><span class="sxs-lookup"><span data-stu-id="c55b9-128">The **lpPropertyInstEx** member is used only when you call [AttachPropertyInstanceEx](attachpropertyinstanceex.md).</span></span>

<span data-ttu-id="c55b9-129">如果使用 **lpPropertyInstEx** ，您必須將 **DataLength** 成員設定為0xffff。</span><span class="sxs-lookup"><span data-stu-id="c55b9-129">If **lpPropertyInstEx** is used, you must set the **DataLength** member to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-130">**DataLength**</span><span class="sxs-lookup"><span data-stu-id="c55b9-130">**DataLength**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-131">這個屬性實例的資料長度。</span><span class="sxs-lookup"><span data-stu-id="c55b9-131">Data length for this instance of the property.</span></span> <span data-ttu-id="c55b9-132">如果 **lpPropertyInstEx** 成員指向 [**PROPERTYINSTEX**](propertyinstex.md) 結構，則必須將 **DataLength** 設定為0xffff。</span><span class="sxs-lookup"><span data-stu-id="c55b9-132">If the **lpPropertyInstEx** member points to a [**PROPERTYINSTEX**](propertyinstex.md) structure, you must set **DataLength** to 0xFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-133">**Level**</span><span class="sxs-lookup"><span data-stu-id="c55b9-133">**Level**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-134">層級資訊。</span><span class="sxs-lookup"><span data-stu-id="c55b9-134">Level information.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-135">**HelpID**</span><span class="sxs-lookup"><span data-stu-id="c55b9-135">**HelpID**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-136">說明檔內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="c55b9-136">Help file context identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c55b9-137">**IFlags**</span><span class="sxs-lookup"><span data-stu-id="c55b9-137">**IFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c55b9-138">錯誤條件旗標。</span><span class="sxs-lookup"><span data-stu-id="c55b9-138">Error condition flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c55b9-139">備註</span><span class="sxs-lookup"><span data-stu-id="c55b9-139">Remarks</span></span>

<span data-ttu-id="c55b9-140">**PROPERTYINST** 結構會定義附加屬性的實例。</span><span class="sxs-lookup"><span data-stu-id="c55b9-140">The **PROPERTYINST** structure defines an instance of an attached property.</span></span> <span data-ttu-id="c55b9-141">剖析器會透過數個 helper 函數來存取 **PROPERTYINST** 結構。</span><span class="sxs-lookup"><span data-stu-id="c55b9-141">The parser accesses the **PROPERTYINST** structure through several helper functions.</span></span> <span data-ttu-id="c55b9-142">例如，當呼叫 [**FormatPropertyInstance**](formatpropertyinstance.md)函數來格式化屬性的資料時，它會修改 **PROPERTYINST** 結構的 **szPropertyText** 成員。</span><span class="sxs-lookup"><span data-stu-id="c55b9-142">For example, when the [**FormatPropertyInstance**](formatpropertyinstance.md) function is called to format the data of a property, it modifies the **szPropertyText** member of the **PROPERTYINST** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55b9-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="c55b9-143">Requirements</span></span>



| <span data-ttu-id="c55b9-144">需求</span><span class="sxs-lookup"><span data-stu-id="c55b9-144">Requirement</span></span> | <span data-ttu-id="c55b9-145">值</span><span class="sxs-lookup"><span data-stu-id="c55b9-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c55b9-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c55b9-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c55b9-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c55b9-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c55b9-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c55b9-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c55b9-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c55b9-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c55b9-150">標頭</span><span class="sxs-lookup"><span data-stu-id="c55b9-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="c55b9-151"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c55b9-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c55b9-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c55b9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c55b9-153">AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="c55b9-153">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="c55b9-154">AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="c55b9-154">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> </dl>

 

