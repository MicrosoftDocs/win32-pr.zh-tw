---
description: PF \_ HANDOFFENTRY 結構會定義網路監視器新增至剖析器之遞交集的通訊協定。
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: 'PF_HANDOFFENTRY 結構 (Netmon) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ad431e936265be96831778f9949ae67ef737beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979239"
---
# <a name="pf_handoffentry-structure"></a><span data-ttu-id="bc9b3-103">PF \_ HANDOFFENTRY 結構</span><span class="sxs-lookup"><span data-stu-id="bc9b3-103">PF\_HANDOFFENTRY structure</span></span>

<span data-ttu-id="bc9b3-104">**PF \_ HANDOFFENTRY** 結構會定義網路監視器新增至剖析器之遞交集的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bc9b3-104">The **PF\_HANDOFFENTRY** structure defines a protocol that Network Monitor adds to the handoff set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc9b3-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc9b3-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="bc9b3-106">成員</span><span class="sxs-lookup"><span data-stu-id="bc9b3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc9b3-107">**szIniFile**</span><span class="sxs-lookup"><span data-stu-id="bc9b3-107">**szIniFile**</span></span>
</dt> <dd>

<span data-ttu-id="bc9b3-108">與通訊協定相關聯的 INI 檔案名。</span><span class="sxs-lookup"><span data-stu-id="bc9b3-108">Name of the INI file associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="bc9b3-109">**szIniSection**</span><span class="sxs-lookup"><span data-stu-id="bc9b3-109">**szIniSection**</span></span>
</dt> <dd>

<span data-ttu-id="bc9b3-110">INI 檔案中的區段標籤。</span><span class="sxs-lookup"><span data-stu-id="bc9b3-110">Section label within the INI file.</span></span>

</dd> <dt>

<span data-ttu-id="bc9b3-111">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="bc9b3-111">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="bc9b3-112">通訊協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc9b3-112">Name of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="bc9b3-113">**dwHandOffValue**</span><span class="sxs-lookup"><span data-stu-id="bc9b3-113">**dwHandOffValue**</span></span>
</dt> <dd>

<span data-ttu-id="bc9b3-114">與通訊協定相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="bc9b3-114">Value associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="bc9b3-115">**ValueFormatBase**</span><span class="sxs-lookup"><span data-stu-id="bc9b3-115">**ValueFormatBase**</span></span>
</dt> <dd>

<span data-ttu-id="bc9b3-116">**DwHandOffValue** 中指定之通訊協定值的數位基底。</span><span class="sxs-lookup"><span data-stu-id="bc9b3-116">Numeric base of the protocol value that is specified in **dwHandOffValue**.</span></span> <span data-ttu-id="bc9b3-117">**ValueFormatBase** 函數必須設定為下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="bc9b3-117">The **ValueFormatBase** function must be set to one of the following:</span></span>



| <span data-ttu-id="bc9b3-118">值</span><span class="sxs-lookup"><span data-stu-id="bc9b3-118">Value</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="bc9b3-119">意義</span><span class="sxs-lookup"><span data-stu-id="bc9b3-119">Meaning</span></span>                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <span data-ttu-id="bc9b3-120"><dt>**提交 \_ 值 \_ 格式 \_ 基底 \_ 未知**</dt></span><span class="sxs-lookup"><span data-stu-id="bc9b3-120"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="bc9b3-121">未知的基底</span><span class="sxs-lookup"><span data-stu-id="bc9b3-121">Unknown base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <span data-ttu-id="bc9b3-122"><dt>**切換 \_ 值 \_ 格式 \_ 基底 \_ 十進位**</dt></span><span class="sxs-lookup"><span data-stu-id="bc9b3-122"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_DECIMAL**</dt></span></span> </dl> | <span data-ttu-id="bc9b3-123">十進位基底</span><span class="sxs-lookup"><span data-stu-id="bc9b3-123">Decimal base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <span data-ttu-id="bc9b3-124"><dt>**提交 \_ 值 \_ 格式 \_ 基底 \_ 十六進位**</dt></span><span class="sxs-lookup"><span data-stu-id="bc9b3-124"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_HEX**</dt></span></span> </dl>             | <span data-ttu-id="bc9b3-125">十六進位基底</span><span class="sxs-lookup"><span data-stu-id="bc9b3-125">Hexadecimal base</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc9b3-126">備註</span><span class="sxs-lookup"><span data-stu-id="bc9b3-126">Remarks</span></span>

<span data-ttu-id="bc9b3-127">Pf [ \_ HANDOFFSET](pf-handoffset.md)結構中會使用 **pf \_ HANDOFFENTRY** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="bc9b3-127">An array of the **PF\_HANDOFFENTRY** structures is used in the [PF\_HANDOFFSET](pf-handoffset.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc9b3-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc9b3-128">Requirements</span></span>



| <span data-ttu-id="bc9b3-129">需求</span><span class="sxs-lookup"><span data-stu-id="bc9b3-129">Requirement</span></span> | <span data-ttu-id="bc9b3-130">值</span><span class="sxs-lookup"><span data-stu-id="bc9b3-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bc9b3-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc9b3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bc9b3-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc9b3-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bc9b3-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc9b3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bc9b3-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc9b3-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bc9b3-135">標頭</span><span class="sxs-lookup"><span data-stu-id="bc9b3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc9b3-136"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="bc9b3-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc9b3-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc9b3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc9b3-138">PF \_ HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="bc9b3-138">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> </dl>

 

 




