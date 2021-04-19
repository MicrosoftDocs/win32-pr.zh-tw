---
description: 在事件檢視器的上方窗格中提供一條線，作為所有可能插入資料行之資料的容器。
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: 'NMCOLUMNVARIANT 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978178"
---
# <a name="nmcolumnvariant-structure"></a><span data-ttu-id="c17b0-103">NMCOLUMNVARIANT 結構</span><span class="sxs-lookup"><span data-stu-id="c17b0-103">NMCOLUMNVARIANT structure</span></span>

<span data-ttu-id="c17b0-104">**NMCOLUMNVARIANT** 結構會在事件檢視器的上方窗格中提供一條線，作為所有可能插入資料行之資料的容器。</span><span class="sxs-lookup"><span data-stu-id="c17b0-104">The **NMCOLUMNVARIANT** structure provides a line in the top pane of the Event Viewer that serves as a container for all possible data inserted into a column.</span></span>

## <a name="syntax"></a><span data-ttu-id="c17b0-105">語法</span><span class="sxs-lookup"><span data-stu-id="c17b0-105">Syntax</span></span>


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a><span data-ttu-id="c17b0-106">成員</span><span class="sxs-lookup"><span data-stu-id="c17b0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c17b0-107">**型別**</span><span class="sxs-lookup"><span data-stu-id="c17b0-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-108">[**NMCOLUMNTYPE**](nmcolumntype.md)列舉型別中的值。</span><span class="sxs-lookup"><span data-stu-id="c17b0-108">A value from the [**NMCOLUMNTYPE**](nmcolumntype.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-109">**值**</span><span class="sxs-lookup"><span data-stu-id="c17b0-109">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c17b0-110">**Uint8Val**</span><span class="sxs-lookup"><span data-stu-id="c17b0-110">**Uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-111">8位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="c17b0-111">8-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-112">**Sint8Val**</span><span class="sxs-lookup"><span data-stu-id="c17b0-112">**Sint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-113">8位帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="c17b0-113">8-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-114">**Uint16Val**</span><span class="sxs-lookup"><span data-stu-id="c17b0-114">**Uint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-115">16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="c17b0-115">16-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-116">**Sint16Val**</span><span class="sxs-lookup"><span data-stu-id="c17b0-116">**Sint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-117">16位帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="c17b0-117">16-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-118">**Uint32Val**</span><span class="sxs-lookup"><span data-stu-id="c17b0-118">**Uint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-119">32位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="c17b0-119">32-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-120">**Sint32Val**</span><span class="sxs-lookup"><span data-stu-id="c17b0-120">**Sint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-121">32位帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="c17b0-121">32-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-122">**Float64Val**</span><span class="sxs-lookup"><span data-stu-id="c17b0-122">**Float64Val**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-123">64位浮點值。</span><span class="sxs-lookup"><span data-stu-id="c17b0-123">64-bit float value.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-124">**FrameVal**</span><span class="sxs-lookup"><span data-stu-id="c17b0-124">**FrameVal**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-125">畫面格編號。</span><span class="sxs-lookup"><span data-stu-id="c17b0-125">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-126">**YesNoVal**</span><span class="sxs-lookup"><span data-stu-id="c17b0-126">**YesNoVal**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-127">顯示 [是] 或 [否]。</span><span class="sxs-lookup"><span data-stu-id="c17b0-127">Displays Yes or No.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-128">**OnOffVal**</span><span class="sxs-lookup"><span data-stu-id="c17b0-128">**OnOffVal**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-129">顯示為開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="c17b0-129">Displays On or Off.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-130">**TrueFalseVal**</span><span class="sxs-lookup"><span data-stu-id="c17b0-130">**TrueFalseVal**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-131">顯示 True 或 False。</span><span class="sxs-lookup"><span data-stu-id="c17b0-131">Displays True or False.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-132">**MACAddrVal**</span><span class="sxs-lookup"><span data-stu-id="c17b0-132">**MACAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-133">MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="c17b0-133">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-134">**IPXAddrVal**</span><span class="sxs-lookup"><span data-stu-id="c17b0-134">**IPXAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-135">IPX 位址。</span><span class="sxs-lookup"><span data-stu-id="c17b0-135">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-136">**IPAddrVal**</span><span class="sxs-lookup"><span data-stu-id="c17b0-136">**IPAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-137">IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c17b0-137">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-138">**VarTimeVal**</span><span class="sxs-lookup"><span data-stu-id="c17b0-138">**VarTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-139">變異時間。</span><span class="sxs-lookup"><span data-stu-id="c17b0-139">Variant time.</span></span> <span data-ttu-id="c17b0-140">使用 **VariantTimetoSystemTime** 轉換為系統時間。</span><span class="sxs-lookup"><span data-stu-id="c17b0-140">Use **VariantTimetoSystemTime** to convert to system time.</span></span>

</dd> <dt>

<span data-ttu-id="c17b0-141">**pStringVal**</span><span class="sxs-lookup"><span data-stu-id="c17b0-141">**pStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="c17b0-142">字串的指標。</span><span class="sxs-lookup"><span data-stu-id="c17b0-142">Pointer to a string.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c17b0-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="c17b0-143">Requirements</span></span>



| <span data-ttu-id="c17b0-144">需求</span><span class="sxs-lookup"><span data-stu-id="c17b0-144">Requirement</span></span> | <span data-ttu-id="c17b0-145">值</span><span class="sxs-lookup"><span data-stu-id="c17b0-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c17b0-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c17b0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c17b0-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c17b0-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c17b0-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c17b0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c17b0-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c17b0-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c17b0-150">標頭</span><span class="sxs-lookup"><span data-stu-id="c17b0-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="c17b0-151"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c17b0-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c17b0-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c17b0-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c17b0-153">**NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="c17b0-153">**NMCOLUMNTYPE**</span></span>](nmcolumntype.md)
</dt> </dl>

 

 




