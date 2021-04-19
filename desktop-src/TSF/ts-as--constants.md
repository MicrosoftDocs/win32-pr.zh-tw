---
title: 'TS_AS_ 常數 (Textstor) '
description: 下列旗標會指定呼叫 AdviseSink 方法的事件。
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998022"
---
# <a name="ts_as_-constants"></a><span data-ttu-id="ae6a2-103">TS \_ 作為 \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="ae6a2-103">TS\_AS\_\* Constants</span></span>

<span data-ttu-id="ae6a2-104">下列旗標會指定呼叫 **AdviseSink** 方法的事件。</span><span class="sxs-lookup"><span data-stu-id="ae6a2-104">The following flags specify the events that call the **AdviseSink** methods.</span></span>



| <span data-ttu-id="ae6a2-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="ae6a2-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="ae6a2-106">Description</span><span class="sxs-lookup"><span data-stu-id="ae6a2-106">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <span data-ttu-id="ae6a2-107"><dt>**TS \_\_文字 \_ 變更**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a2-107"><dt>**TS\_AS\_TEXT\_CHANGE**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="ae6a2-108">檔中的文字已變更。</span><span class="sxs-lookup"><span data-stu-id="ae6a2-108">Text is changed in the document.</span></span><br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <span data-ttu-id="ae6a2-109"><dt>**TS \_作為 \_ SEL \_ 變更**</dt> <dt> ( 0x2 )</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a2-109"><dt>**TS\_AS\_SEL\_CHANGE**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="ae6a2-110">在檔中選取文字。</span><span class="sxs-lookup"><span data-stu-id="ae6a2-110">Text is selected in the document.</span></span><br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <span data-ttu-id="ae6a2-111"><dt>**TS \_當 \_ 版面配置 \_ 變更**</dt> <dt> ( 0x4 )</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a2-111"><dt>**TS\_AS\_LAYOUT\_CHANGE**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="ae6a2-112">檔的版面配置已變更。</span><span class="sxs-lookup"><span data-stu-id="ae6a2-112">The layout of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <span data-ttu-id="ae6a2-113"><dt>**TS \_ ( 0x8 ) 的 \_ ATTR \_ 變更**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ae6a2-113"><dt>**TS\_AS\_ATTR\_CHANGE**</dt> <dt>( 0x8 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="ae6a2-114">檔的屬性已變更。</span><span class="sxs-lookup"><span data-stu-id="ae6a2-114">The attributes of the document is changed.</span></span><br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <span data-ttu-id="ae6a2-115"><dt>**TS \_\_狀態 \_ 變更**</dt> <dt> ( 0x10 )</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a2-115"><dt>**TS\_AS\_STATUS\_CHANGE**</dt> <dt>( 0x10 )</dt></span></span> </dl>                                                                                                        | <span data-ttu-id="ae6a2-116">檔的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="ae6a2-116">The status of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <span data-ttu-id="ae6a2-117"><dt>**TS \_因為 \_ 所有 \_ 接收都**</dt> <dt> ( ts \_ 作為 \_ 文字 \_ 變更 \| ts \_ \_ \_ \| \_ \_ \_ \| \_ \_ \_ \| \_ \_ \_</dt>作為「變更 ts」做為「配置變更 ts」作為變更 ts 作為狀態變更 ) </span><span class="sxs-lookup"><span data-stu-id="ae6a2-117"><dt>**TS\_AS\_ALL\_SINKS**</dt> <dt>( TS\_AS\_TEXT\_CHANGE \| TS\_AS\_SEL\_CHANGE \| TS\_AS\_LAYOUT\_CHANGE \| TS\_AS\_ATTR\_CHANGE \| TS\_AS\_STATUS\_CHANGE )</dt></span></span> </dl> | <span data-ttu-id="ae6a2-118">檔中發生先前四個事件的其中一個。</span><span class="sxs-lookup"><span data-stu-id="ae6a2-118">One of the previous four events occurred in the document.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ae6a2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae6a2-119">Requirements</span></span>



| <span data-ttu-id="ae6a2-120">需求</span><span class="sxs-lookup"><span data-stu-id="ae6a2-120">Requirement</span></span> | <span data-ttu-id="ae6a2-121">值</span><span class="sxs-lookup"><span data-stu-id="ae6a2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6a2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae6a2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6a2-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae6a2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ae6a2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae6a2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6a2-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae6a2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae6a2-126">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ae6a2-126">Redistributable</span></span><br/>          | <span data-ttu-id="ae6a2-127">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="ae6a2-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="ae6a2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="ae6a2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae6a2-129"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a2-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae6a2-130">Idl</span><span class="sxs-lookup"><span data-stu-id="ae6a2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae6a2-131"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae6a2-131"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





