---
description: PF \_ PARSERINFO 結構會一次定義一個剖析器。 在 PF \_ PARSERINFO 結構中，剖析器會由剖析器偵測到之通訊協定的相關資訊定義。
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: 'PF_PARSERINFO 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 28ebeaad31e6f40ceb961d8c303a22590966947f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997826"
---
# <a name="pf_parserinfo-structure"></a><span data-ttu-id="94034-104">PF \_ PARSERINFO 結構</span><span class="sxs-lookup"><span data-stu-id="94034-104">PF\_PARSERINFO structure</span></span>

<span data-ttu-id="94034-105">**PF \_ PARSERINFO** 結構會一次定義一個剖析器。</span><span class="sxs-lookup"><span data-stu-id="94034-105">The **PF\_PARSERINFO** structure defines one parser at a time.</span></span> <span data-ttu-id="94034-106">在 **PF \_ PARSERINFO** 結構中，剖析器會由剖析器偵測到之通訊協定的相關資訊定義。</span><span class="sxs-lookup"><span data-stu-id="94034-106">In the **PF\_PARSERINFO** structure, a parser is defined by the information about the protocol that the parser detects.</span></span>

## <a name="syntax"></a><span data-ttu-id="94034-107">語法</span><span class="sxs-lookup"><span data-stu-id="94034-107">Syntax</span></span>


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a><span data-ttu-id="94034-108">成員</span><span class="sxs-lookup"><span data-stu-id="94034-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="94034-109">**szProtocolName**</span><span class="sxs-lookup"><span data-stu-id="94034-109">**szProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="94034-110">剖析器偵測到的通訊協定名稱。</span><span class="sxs-lookup"><span data-stu-id="94034-110">Name of the protocol that the parser detects.</span></span>

</dd> <dt>

<span data-ttu-id="94034-111">**szComment**</span><span class="sxs-lookup"><span data-stu-id="94034-111">**szComment**</span></span>
</dt> <dd>

<span data-ttu-id="94034-112">通訊協定的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="94034-112">Brief description of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="94034-113">**szHelpFile**</span><span class="sxs-lookup"><span data-stu-id="94034-113">**szHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="94034-114">通訊協定說明檔的名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="94034-114">Name of the protocol Help file, if any.</span></span>

</dd> <dt>

<span data-ttu-id="94034-115">**pWhoCanPrecedeMe**</span><span class="sxs-lookup"><span data-stu-id="94034-115">**pWhoCanPrecedeMe**</span></span>
</dt> <dd>

<span data-ttu-id="94034-116">[Pf \_ FOLLOWSET](pf-followset.md)結構的指標，此結構會列出在 **PF \_ PARSERINFO** 結構所描述的通訊協定之前可以使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="94034-116">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocols that can precede the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="94034-117">網路監視器將剖析器通訊協定新增至集合中所有通訊協定的 [*下列集合*](f.md) 。</span><span class="sxs-lookup"><span data-stu-id="94034-117">Network Monitor adds the parser protocol to the [*follow set*](f.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="94034-118">**pWhoCanFollowMe**</span><span class="sxs-lookup"><span data-stu-id="94034-118">**pWhoCanFollowMe**</span></span>
</dt> <dd>

<span data-ttu-id="94034-119">[Pf \_ FOLLOWSET](pf-followset.md)結構的指標，此結構會列出可遵循 **PF \_ PARSERINFO** 結構所描述之通訊協定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="94034-119">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocol that can follow the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="94034-120">網路監視器將設定的通訊協定新增至剖析器通訊協定的 [*下列集合*](f.md) 。</span><span class="sxs-lookup"><span data-stu-id="94034-120">Network Monitor adds the protocols of the set to the [*follow set*](f.md) of the parser protocol.</span></span>

</dd> <dt>

<span data-ttu-id="94034-121">**pWhoHandsOffToMe**</span><span class="sxs-lookup"><span data-stu-id="94034-121">**pWhoHandsOffToMe**</span></span>
</dt> <dd>

<span data-ttu-id="94034-122">指向 pf [ \_ HANDOFFSET](pf-handoffset.md) 結構的指標，該結構會實際操作到 **pf \_ PARSERINFO** 結構所描述的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="94034-122">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that hands-off to the protocol that the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="94034-123">網路監視器會將剖析器通訊協定新增至集合中所有通訊協定的 [*遞交集*](h.md) 。</span><span class="sxs-lookup"><span data-stu-id="94034-123">Network Monitor adds the parser protocol to the [*handoff sets*](h.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="94034-124">**pWhoDoIHandOffTo**</span><span class="sxs-lookup"><span data-stu-id="94034-124">**pWhoDoIHandOffTo**</span></span>
</dt> <dd>

<span data-ttu-id="94034-125">[PF \_ HANDOFFSET](pf-handoffset.md)結構的指標，此結構會列出剖析器通訊協定所用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="94034-125">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that lists the protocols that the parser protocol hands off to.</span></span> <span data-ttu-id="94034-126">網路監視器將此集合的通訊協定新增至剖析器通訊協定的 [*遞交集*](h.md) 。</span><span class="sxs-lookup"><span data-stu-id="94034-126">Network Monitor adds the protocols of this set to the [*handoff set*](h.md) of the parser protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94034-127">備註</span><span class="sxs-lookup"><span data-stu-id="94034-127">Remarks</span></span>

<span data-ttu-id="94034-128">Pf **\_ PARSERINFO** 結構是在 **pf \_ PARSERDLLINFO** 結構中使用，以提供剖析器的描述。</span><span class="sxs-lookup"><span data-stu-id="94034-128">The **PF\_PARSERINFO** structure is used in the **PF\_PARSERDLLINFO** structure to provide a description of a parser.</span></span> <span data-ttu-id="94034-129">網路監視器使用剖析器描述來更新 [*Parser.ini*](p.md) 檔和剖析器的 INI 檔案，其位於 **PF \_ PARSERINFO** 結構中所述的通訊協定之前和之後。</span><span class="sxs-lookup"><span data-stu-id="94034-129">Network Monitor uses the parser description to update the [*Parser.ini*](p.md) file, and the INI files of the parsers that precede and follow the protocol described in the **PF\_PARSERINFO** structure.</span></span>

<span data-ttu-id="94034-130">下列集合會指定遵循通訊協定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="94034-130">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="94034-131">當剖析器無法從通訊協定實例中的資料識別下一個通訊協定時，網路監視器會使用下列資料集。</span><span class="sxs-lookup"><span data-stu-id="94034-131">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="94034-132">下列集合會儲存在 [*Parser.ini*](p.md) 檔案中。</span><span class="sxs-lookup"><span data-stu-id="94034-132">A follow set is stored in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="94034-133">第一次安裝剖析器時，網路監視器會更新 **pWhoCanPrecedeMe** 和 **pWhoCanFollowMe** 中列出的下列剖析器通訊協定集。</span><span class="sxs-lookup"><span data-stu-id="94034-133">When the parser is installed for the first time, Network Monitor updates the follow set of the parser protocols that are listed in **pWhoCanPrecedeMe** and **pWhoCanFollowMe**.</span></span>

<span data-ttu-id="94034-134">遞交集會指定遵循通訊協定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="94034-134">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="94034-135">只有當剖析器可以從通訊協定實例中的資料識別下一個通訊協定時，剖析器才會使用一組遞交集。</span><span class="sxs-lookup"><span data-stu-id="94034-135">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="94034-136">每個剖析器的 INI 檔案中都會儲存一個遞交集。</span><span class="sxs-lookup"><span data-stu-id="94034-136">A handoff set is stored in the INI files of each parser.</span></span> <span data-ttu-id="94034-137">第一次安裝剖析器時，網路監視器會更新 **pWhoHandsOffToMe** 和 **pWhoDoIHandOffTo** 中所列之剖析器通訊協定的遞交集。</span><span class="sxs-lookup"><span data-stu-id="94034-137">When the parser is installed for the first time, Network Monitor updates the handoff set of the parser protocols that are listed in **pWhoHandsOffToMe** and **pWhoDoIHandOffTo**.</span></span>



| <span data-ttu-id="94034-138">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="94034-138">For information on</span></span>                                               | <span data-ttu-id="94034-139">請參閱</span><span class="sxs-lookup"><span data-stu-id="94034-139">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="94034-140">什麼是剖析器，以及它們如何搭配網路監視器運作。</span><span class="sxs-lookup"><span data-stu-id="94034-140">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="94034-141">解析 器</span><span class="sxs-lookup"><span data-stu-id="94034-141">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="94034-142">接下來的集合包含。</span><span class="sxs-lookup"><span data-stu-id="94034-142">What follow sets contain.</span></span>                                        | [<span data-ttu-id="94034-143">指定追蹤集</span><span class="sxs-lookup"><span data-stu-id="94034-143">Specifying a Follow Set</span></span>](specifying-a-follow-set.md)                       |
| <span data-ttu-id="94034-144">哪些遞交集包含。</span><span class="sxs-lookup"><span data-stu-id="94034-144">What handoff sets contain.</span></span>                                       | [<span data-ttu-id="94034-145">指定遞交集</span><span class="sxs-lookup"><span data-stu-id="94034-145">Specifying a Handoff Set</span></span>](specifying-a-handoff-set.md)                     |
| <span data-ttu-id="94034-146">剖析器 DLL 中包含了哪些進入點。</span><span class="sxs-lookup"><span data-stu-id="94034-146">What entry points are included in the parser DLL.</span></span>                | [<span data-ttu-id="94034-147">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="94034-147">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="94034-148">如何執行 **ParserAutoInstallInfo**  包含範例。</span><span class="sxs-lookup"><span data-stu-id="94034-148">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="94034-149">執行 ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="94034-149">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="94034-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="94034-150">Requirements</span></span>



| <span data-ttu-id="94034-151">需求</span><span class="sxs-lookup"><span data-stu-id="94034-151">Requirement</span></span> | <span data-ttu-id="94034-152">值</span><span class="sxs-lookup"><span data-stu-id="94034-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="94034-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94034-153">Minimum supported client</span></span><br/> | <span data-ttu-id="94034-154">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94034-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="94034-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94034-155">Minimum supported server</span></span><br/> | <span data-ttu-id="94034-156">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94034-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="94034-157">標頭</span><span class="sxs-lookup"><span data-stu-id="94034-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="94034-158"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="94034-158"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94034-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94034-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94034-160">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="94034-160">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> <dt>

[<span data-ttu-id="94034-161">PF \_ FOLLOWSET</span><span class="sxs-lookup"><span data-stu-id="94034-161">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> <dt>

[<span data-ttu-id="94034-162">PF \_ HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="94034-162">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> <dt>

[<span data-ttu-id="94034-163">PF \_ PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="94034-163">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




