---
description: 深入瞭解： JET_UNICODEINDEX 結構
title: JET_UNICODEINDEX 結構
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: c4a2332551fb1f624b75e32596b2941d97ffa47d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104386534"
---
# <a name="jet_unicodeindex-structure"></a><span data-ttu-id="9f0d2-103">JET_UNICODEINDEX 結構</span><span class="sxs-lookup"><span data-stu-id="9f0d2-103">JET_UNICODEINDEX Structure</span></span>


<span data-ttu-id="9f0d2-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9f0d2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_unicodeindex-structure"></a><span data-ttu-id="9f0d2-105">JET_UNICODEINDEX 結構</span><span class="sxs-lookup"><span data-stu-id="9f0d2-105">JET_UNICODEINDEX Structure</span></span>

<span data-ttu-id="9f0d2-106">**JET_UNICODEINDEX** 結構自訂在 unicode 資料行上建立索引時，如何將 Unicode 資料正規化。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-106">The **JET_UNICODEINDEX** structure customizes how Unicode data gets normalized when an index is created over a Unicode column.</span></span>

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a><span data-ttu-id="9f0d2-107">成員</span><span class="sxs-lookup"><span data-stu-id="9f0d2-107">Members</span></span>

<span data-ttu-id="9f0d2-108">**lcid**</span><span class="sxs-lookup"><span data-stu-id="9f0d2-108">**lcid**</span></span>

<span data-ttu-id="9f0d2-109">正規化資料時要使用的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-109">The Locale ID to use when normalizing the data.</span></span> <span data-ttu-id="9f0d2-110">只要電腦上已安裝適當的語言套件，即可使用任何地區設定。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-110">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="9f0d2-111">其中一個例外狀況是，非語言相關地區設定 (LCID 為零) 不合法。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-111">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="9f0d2-112">**dwMapFlags**</span><span class="sxs-lookup"><span data-stu-id="9f0d2-112">**dwMapFlags**</span></span>

<span data-ttu-id="9f0d2-113">當 Unicode 資料正規化至索引鍵時，這些旗標會傳遞至 [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) ，如此可讓使用者定義旗標覆寫預設值。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-113">These flags get passed to [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) when Unicode data gets normalized to a key, which enables user-defined flags to override the default.</span></span>

<span data-ttu-id="9f0d2-114">**Windows 2000**： **dwFlags** 的唯一兩個合法值為：</span><span class="sxs-lookup"><span data-stu-id="9f0d2-114">**Windows 2000**:  The only two legal values for **dwFlags** are:</span></span>

  - <span data-ttu-id="9f0d2-115"> ( LCMAP_SORTKEY |NORM_IGNORECASE |NORM_IGNOREKANATYPE |NORM_IGNOREWIDTH |NORM_IGNORENONSPACE ) </span><span class="sxs-lookup"><span data-stu-id="9f0d2-115">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE )</span></span>

<!-- end list -->

  - <span data-ttu-id="9f0d2-116"> ( LCMAP_SORTKEY |NORM_IGNORECASE |NORM_IGNOREKANATYPE |NORM_IGNOREWIDTH ) </span><span class="sxs-lookup"><span data-stu-id="9f0d2-116">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH )</span></span>

<span data-ttu-id="9f0d2-117">**dwMapFlags** 具有下列限制。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-117">**dwMapFlags** has the following restrictions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f0d2-118">值</span><span class="sxs-lookup"><span data-stu-id="9f0d2-118">Value</span></span></p></th>
<th><p><span data-ttu-id="9f0d2-119">意義</span><span class="sxs-lookup"><span data-stu-id="9f0d2-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f0d2-120">LCMAP_SORTKEY</span><span class="sxs-lookup"><span data-stu-id="9f0d2-120">LCMAP_SORTKEY</span></span></p></td>
<td><p><span data-ttu-id="9f0d2-121">Mandatory。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-121">Mandatory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f0d2-122">LCMAP_BYTEREV</span><span class="sxs-lookup"><span data-stu-id="9f0d2-122">LCMAP_BYTEREV</span></span></p></td>
<td><p><span data-ttu-id="9f0d2-123">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-123">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f0d2-124">NORM_IGNORECASE</span><span class="sxs-lookup"><span data-stu-id="9f0d2-124">NORM_IGNORECASE</span></span></p></td>
<td><p><span data-ttu-id="9f0d2-125">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-125">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f0d2-126">NORM_IGNORENONSPACE</span><span class="sxs-lookup"><span data-stu-id="9f0d2-126">NORM_IGNORENONSPACE</span></span></p></td>
<td><p><span data-ttu-id="9f0d2-127">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-127">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f0d2-128">NORM_IGNORESYMBOLS</span><span class="sxs-lookup"><span data-stu-id="9f0d2-128">NORM_IGNORESYMBOLS</span></span></p></td>
<td><p><span data-ttu-id="9f0d2-129">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-129">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f0d2-130">NORM_IGNOREKANATYPE</span><span class="sxs-lookup"><span data-stu-id="9f0d2-130">NORM_IGNOREKANATYPE</span></span></p></td>
<td><p><span data-ttu-id="9f0d2-131">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-131">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f0d2-132">NORM_IGNOREWIDTH</span><span class="sxs-lookup"><span data-stu-id="9f0d2-132">NORM_IGNOREWIDTH</span></span></p></td>
<td><p><span data-ttu-id="9f0d2-133">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-133">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f0d2-134">SORT_STRINGSORT</span><span class="sxs-lookup"><span data-stu-id="9f0d2-134">SORT_STRINGSORT</span></span></p></td>
<td><p><span data-ttu-id="9f0d2-135">選擇性。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-135">Optional.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="9f0d2-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f0d2-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f0d2-137"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="9f0d2-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9f0d2-138">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-138">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f0d2-139"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="9f0d2-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9f0d2-140">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-140">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f0d2-141"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="9f0d2-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9f0d2-142">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="9f0d2-142">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9f0d2-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f0d2-143">See Also</span></span>

[<span data-ttu-id="9f0d2-144">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="9f0d2-144">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="9f0d2-145">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="9f0d2-145">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="9f0d2-146">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="9f0d2-146">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)
