---
description: 深入瞭解： JET_TUPLELIMITS 結構
title: JET_TUPLELIMITS 結構
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945359"
---
# <a name="jet_tuplelimits-structure"></a><span data-ttu-id="49dd0-103">JET_TUPLELIMITS 結構</span><span class="sxs-lookup"><span data-stu-id="49dd0-103">JET_TUPLELIMITS Structure</span></span>


<span data-ttu-id="49dd0-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="49dd0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tuplelimits-structure"></a><span data-ttu-id="49dd0-105">JET_TUPLELIMITS 結構</span><span class="sxs-lookup"><span data-stu-id="49dd0-105">JET_TUPLELIMITS Structure</span></span>

<span data-ttu-id="49dd0-106">**JET_TUPLELIMITS** 結構允許使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md)，針對每個索引（而不是每個實例）自訂元組索引特性。</span><span class="sxs-lookup"><span data-stu-id="49dd0-106">The **JET_TUPLELIMITS** structure allows customization of the tuple index characteristics on a per-index basis, rather than a per-instance basis, using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="49dd0-107">**Windows Server 2003：\*\*\*\*JET_TUPLELIMITS** 結構是在 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="49dd0-107">**Windows Server 2003:** The **JET_TUPLELIMITS** structure is introduced in Windows Server 2003.</span></span>

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a><span data-ttu-id="49dd0-108">成員</span><span class="sxs-lookup"><span data-stu-id="49dd0-108">Members</span></span>

<span data-ttu-id="49dd0-109">**chLengthMin**</span><span class="sxs-lookup"><span data-stu-id="49dd0-109">**chLengthMin**</span></span>

<span data-ttu-id="49dd0-110">元組的最小長度。</span><span class="sxs-lookup"><span data-stu-id="49dd0-110">The minimum length of a tuple.</span></span> <span data-ttu-id="49dd0-111">預設值是 3。</span><span class="sxs-lookup"><span data-stu-id="49dd0-111">The default value is 3.</span></span>

<span data-ttu-id="49dd0-112">**chLengthMax**</span><span class="sxs-lookup"><span data-stu-id="49dd0-112">**chLengthMax**</span></span>

<span data-ttu-id="49dd0-113">元組的最大長度。</span><span class="sxs-lookup"><span data-stu-id="49dd0-113">The maximum length of a tuple.</span></span> <span data-ttu-id="49dd0-114">預設值是 10。</span><span class="sxs-lookup"><span data-stu-id="49dd0-114">The default value is 10.</span></span>

<span data-ttu-id="49dd0-115">**chToIndexMax**</span><span class="sxs-lookup"><span data-stu-id="49dd0-115">**chToIndexMax**</span></span>

<span data-ttu-id="49dd0-116">要編制索引之字串的最大長度。</span><span class="sxs-lookup"><span data-stu-id="49dd0-116">The maximum length of a string to index.</span></span> <span data-ttu-id="49dd0-117">例如，如果資料行的長度為100個字元，且 **chToIndexMax** 設定為60，則只會編制資料行的前60個字元的索引。</span><span class="sxs-lookup"><span data-stu-id="49dd0-117">For example, if a column is 100 characters long, and **chToIndexMax** is set to 60, then only the first 60 characters of the column will be indexed.</span></span> <span data-ttu-id="49dd0-118">預設值為32767。</span><span class="sxs-lookup"><span data-stu-id="49dd0-118">The default value is 32767.</span></span>

<span data-ttu-id="49dd0-119">**cchIncrement**</span><span class="sxs-lookup"><span data-stu-id="49dd0-119">**cchIncrement**</span></span>

<span data-ttu-id="49dd0-120">這可讓您根據每個索引來設定 stride。</span><span class="sxs-lookup"><span data-stu-id="49dd0-120">This allows the stride to be configured on a per index basis.</span></span>

<span data-ttu-id="49dd0-121">**Windows Vista：\*\*\*\*CchIncrement** 成員是在 Windows Vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="49dd0-121">**Windows Vista:** The **cchIncrement** member is introduced in Windows Vista.</span></span> <span data-ttu-id="49dd0-122">在 Windows Vista 之前，將視窗移 (「stride」 ) 的數量一律為1，如「備註」一節中的範例所示。</span><span class="sxs-lookup"><span data-stu-id="49dd0-122">Prior to Windows Vista, the amount to shift the window (the "stride") was always 1, as is shown in the example in the remarks section.</span></span>

<span data-ttu-id="49dd0-123">**ichStart**</span><span class="sxs-lookup"><span data-stu-id="49dd0-123">**ichStart**</span></span>

<span data-ttu-id="49dd0-124">從值開始抓取元組的值位移。</span><span class="sxs-lookup"><span data-stu-id="49dd0-124">The offset into the value to begin taking retrieving tuples from the value.</span></span>

<span data-ttu-id="49dd0-125">**Windows Vista：\*\*\*\*IchStart** 成員是在 Windows Vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="49dd0-125">**Windows Vista:** The **ichStart** member is introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="49dd0-126">備註</span><span class="sxs-lookup"><span data-stu-id="49dd0-126">Remarks</span></span>

<span data-ttu-id="49dd0-127">元組索引會引導字串，並編制其所有可能的 **chLengthMax** 子字串的索引。</span><span class="sxs-lookup"><span data-stu-id="49dd0-127">A tuple index walks a string and indexes all of its possible substrings of **chLengthMax**.</span></span> <span data-ttu-id="49dd0-128">在字串的結尾 (或位置 **chToIndexMax**（以第一個) 發生者為准），將會編制至少 **chLengthMin** 的子字串索引。</span><span class="sxs-lookup"><span data-stu-id="49dd0-128">At the end of the string (or at position **chToIndexMax**, whichever occurs first), the substrings of at least **chLengthMin** will be indexed.</span></span>

<span data-ttu-id="49dd0-129">元組索引可以用來搜尋具有開頭和尾端萬用字元的字串。</span><span class="sxs-lookup"><span data-stu-id="49dd0-129">A tuple index can be used for searching strings with both leading and trailing wildcards.</span></span>

<span data-ttu-id="49dd0-130">假設有一個資料列的文字欄位為 "RAIN IN 西班牙 \! "，且如果元組索引是以參數 **chLengthMin**= 2 和 **chLengthMax**= 3 建立的，則索引中會建立下列專案：</span><span class="sxs-lookup"><span data-stu-id="49dd0-130">Assuming a row with a text field of "RAIN IN SPAIN\!", if a tuple index gets created with parameters **chLengthMin**=2, and **chLengthMax**=3, the following entries are created in the index:</span></span>

<span data-ttu-id="49dd0-131">"RAI"</span><span class="sxs-lookup"><span data-stu-id="49dd0-131">"RAI"</span></span>  
<span data-ttu-id="49dd0-132">AIN</span><span class="sxs-lookup"><span data-stu-id="49dd0-132">"AIN"</span></span>  
<span data-ttu-id="49dd0-133">在</span><span class="sxs-lookup"><span data-stu-id="49dd0-133">"IN "</span></span>  
<span data-ttu-id="49dd0-134">"N I"</span><span class="sxs-lookup"><span data-stu-id="49dd0-134">"N I"</span></span>  
<span data-ttu-id="49dd0-135">在</span><span class="sxs-lookup"><span data-stu-id="49dd0-135">" IN"</span></span>  
<span data-ttu-id="49dd0-136">在</span><span class="sxs-lookup"><span data-stu-id="49dd0-136">"IN "</span></span>  
<span data-ttu-id="49dd0-137">"N S"</span><span class="sxs-lookup"><span data-stu-id="49dd0-137">"N S"</span></span>  
<span data-ttu-id="49dd0-138">SP-1</span><span class="sxs-lookup"><span data-stu-id="49dd0-138">" SP"</span></span>  
<span data-ttu-id="49dd0-139">SPA</span><span class="sxs-lookup"><span data-stu-id="49dd0-139">"SPA"</span></span>  
<span data-ttu-id="49dd0-140">PAI</span><span class="sxs-lookup"><span data-stu-id="49dd0-140">"PAI"</span></span>  
<span data-ttu-id="49dd0-141">AIN</span><span class="sxs-lookup"><span data-stu-id="49dd0-141">"AIN"</span></span>  
<span data-ttu-id="49dd0-142">"IN \! "</span><span class="sxs-lookup"><span data-stu-id="49dd0-142">"IN\!"</span></span>  
<span data-ttu-id="49dd0-143">"N \! "</span><span class="sxs-lookup"><span data-stu-id="49dd0-143">"N\!"</span></span>

<span data-ttu-id="49dd0-144">請注意，"IN" 發生兩次，而且最後一個專案 ( "N \! " ) 小於 3 (**chLengthMax**) 。</span><span class="sxs-lookup"><span data-stu-id="49dd0-144">Note that "IN " occurs twice, and that the last entry ("N\!") is shorter than 3 (**chLengthMax**).</span></span> <span data-ttu-id="49dd0-145">另請注意，分割演算法不會察覺空格或單字，並將所有字元視為相同。</span><span class="sxs-lookup"><span data-stu-id="49dd0-145">Also note that the splitting algorithm is not aware of spaces or words, and treats all characters identically.</span></span>

<span data-ttu-id="49dd0-146">**WINDOWS XP：** Windows XP 支援元組索引，但沒有 **JET_TUPLELIMITS**。</span><span class="sxs-lookup"><span data-stu-id="49dd0-146">**Windows XP:** Windows XP supports tuple indexes, but does not have **JET_TUPLELIMITS**.</span></span> <span data-ttu-id="49dd0-147">資料庫引擎會使用預設值 (**chLengthMin**= 3、 **chLengthMax**= 10、 **chToIndexMax**= 32767) 。</span><span class="sxs-lookup"><span data-stu-id="49dd0-147">The database engine will used the default values (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767).</span></span> <span data-ttu-id="49dd0-148">您仍然可以變更這些值，但會使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramIndexTuplesLengthMin](./index-parameters.md)、 [JET_paramIndexTuplesLengthMax](./index-parameters.md)和 [JET_paramIndexTuplesToIndexMax](./index-parameters.md)，以每個實例為基礎設定這些值。</span><span class="sxs-lookup"><span data-stu-id="49dd0-148">It is still possible to change these values, but they are set on a per-instance basis using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md), and [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="49dd0-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="49dd0-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49dd0-150"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="49dd0-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="49dd0-151">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="49dd0-151">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49dd0-152"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="49dd0-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="49dd0-153">需要 Windows Server 2008、Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="49dd0-153">Requires Windows Server 2008, Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49dd0-154"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="49dd0-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="49dd0-155">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="49dd0-155">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="49dd0-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49dd0-156">See Also</span></span>

[<span data-ttu-id="49dd0-157">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="49dd0-157">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="49dd0-158">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="49dd0-158">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="49dd0-159">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="49dd0-159">JET_TUPLELIMITS</span></span>]()  
[<span data-ttu-id="49dd0-160">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="49dd0-160">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
