---
description: 定義處理 ITablet 介面事件的方法。
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: ITabletEventSink 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fc42bfe8a6e69504c35d7926c4c5a8b688404897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195111"
---
# <a name="itableteventsink-interface"></a><span data-ttu-id="6dbc2-103">ITabletEventSink 介面</span><span class="sxs-lookup"><span data-stu-id="6dbc2-103">ITabletEventSink interface</span></span>

<span data-ttu-id="6dbc2-104">定義處理 [**ITablet 介面**](itablet.md) 事件的方法。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-104">Defines methods that handle the [**ITablet Interface**](itablet.md) events.</span></span>

## <a name="members"></a><span data-ttu-id="6dbc2-105">成員</span><span class="sxs-lookup"><span data-stu-id="6dbc2-105">Members</span></span>

<span data-ttu-id="6dbc2-106">**ITabletEventSink** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-106">The **ITabletEventSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6dbc2-107">**ITabletEventSink** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6dbc2-107">**ITabletEventSink** also has these types of members:</span></span>

-   [<span data-ttu-id="6dbc2-108">方法</span><span class="sxs-lookup"><span data-stu-id="6dbc2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6dbc2-109">方法</span><span class="sxs-lookup"><span data-stu-id="6dbc2-109">Methods</span></span>

<span data-ttu-id="6dbc2-110">**ITabletEventSink** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-110">The **ITabletEventSink** interface has these methods.</span></span>



| <span data-ttu-id="6dbc2-111">方法</span><span class="sxs-lookup"><span data-stu-id="6dbc2-111">Method</span></span>                                                        | <span data-ttu-id="6dbc2-112">描述</span><span class="sxs-lookup"><span data-stu-id="6dbc2-112">Description</span></span>                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6dbc2-113">**CoNtextCreate**</span><span class="sxs-lookup"><span data-stu-id="6dbc2-113">**ContextCreate**</span></span>](itableteventsink-contextcreate.md)       | <span data-ttu-id="6dbc2-114">建立新的平板電腦內容時發生。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-114">Occurs when a new tablet context is created.</span></span><br/>                                          |
| [<span data-ttu-id="6dbc2-115">**CoNtextDestroy**</span><span class="sxs-lookup"><span data-stu-id="6dbc2-115">**ContextDestroy**</span></span>](itableteventsink-contextdestroy.md)     | <span data-ttu-id="6dbc2-116">當 tablet 內容終結時發生。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-116">Occurs when a tablet context is being destroyed.</span></span><br/>                                      |
| [<span data-ttu-id="6dbc2-117">**CursorDown**</span><span class="sxs-lookup"><span data-stu-id="6dbc2-117">**CursorDown**</span></span>](itableteventsink-cursordown.md)             | <span data-ttu-id="6dbc2-118">手寫筆提示接觸到數位化的平板電腦介面時發生。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-118">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span><br/>                    |
| [<span data-ttu-id="6dbc2-119">**CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="6dbc2-119">**CursorInRange**</span></span>](itableteventsink-cursorinrange.md)       | <span data-ttu-id="6dbc2-120">手寫筆進入數位板的偵測範圍內時發生。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-120">Occurs when a stylus comes within the digitizer's range of detection.</span></span><br/>                 |
| [<span data-ttu-id="6dbc2-121">**CursorMove**</span><span class="sxs-lookup"><span data-stu-id="6dbc2-121">**CursorMove**</span></span>](itableteventsink-cursormove.md)             | <span data-ttu-id="6dbc2-122">發生于游標移至 tablet 數位化板上時。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-122">Occurs when the cursor moves over the tablet digitizer.</span></span><br/>                               |
| [<span data-ttu-id="6dbc2-123">**CursorNew**</span><span class="sxs-lookup"><span data-stu-id="6dbc2-123">**CursorNew**</span></span>](itableteventsink-cursornew.md)               | <span data-ttu-id="6dbc2-124">當新的手寫筆新增至系統時發生。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-124">Occurs when a new stylus is added to the system.</span></span><br/>                                      |
| [<span data-ttu-id="6dbc2-125">**CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="6dbc2-125">**CursorOutOfRange**</span></span>](itableteventsink-cursoroutofrange.md) | <span data-ttu-id="6dbc2-126">手寫筆離開 tablet 的實體偵測範圍 (近) 時發生。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-126">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span><br/> |
| [<span data-ttu-id="6dbc2-127">**CursorUp**</span><span class="sxs-lookup"><span data-stu-id="6dbc2-127">**CursorUp**</span></span>](itableteventsink-cursorup.md)                 | <span data-ttu-id="6dbc2-128">發生于使用者從 tablet 數位板介面引發手寫筆時。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-128">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span><br/>         |
| [<span data-ttu-id="6dbc2-129">**封包**</span><span class="sxs-lookup"><span data-stu-id="6dbc2-129">**Packets**</span></span>](itableteventsink-packets.md)                   | <span data-ttu-id="6dbc2-130">手寫筆在數位板上移動時發生。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-130">Occurs when the stylus is moving on the digitizer.</span></span><br/>                                    |
| [<span data-ttu-id="6dbc2-131">**SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="6dbc2-131">**SystemEvent**</span></span>](itableteventsink-systemevent.md)           | <span data-ttu-id="6dbc2-132">發生于可用的系統事件時。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-132">Occurs when a system event is available.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="6dbc2-133">備註</span><span class="sxs-lookup"><span data-stu-id="6dbc2-133">Remarks</span></span>

<span data-ttu-id="6dbc2-134">開發人員不應使用此介面。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-134">Developers should not use this interface.</span></span>

<span data-ttu-id="6dbc2-135">下列程式碼說明如何定義 **ITabletEventSink** 介面。</span><span class="sxs-lookup"><span data-stu-id="6dbc2-135">The following code shows how the **ITabletEventSink** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a><span data-ttu-id="6dbc2-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dbc2-136">Requirements</span></span>



| <span data-ttu-id="6dbc2-137">需求</span><span class="sxs-lookup"><span data-stu-id="6dbc2-137">Requirement</span></span> | <span data-ttu-id="6dbc2-138">值</span><span class="sxs-lookup"><span data-stu-id="6dbc2-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dbc2-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6dbc2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6dbc2-140">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dbc2-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6dbc2-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6dbc2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6dbc2-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="6dbc2-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6dbc2-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="6dbc2-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="6dbc2-144"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6dbc2-144"><dt>Wisptis.exe</dt></span></span> </dl> |



 

