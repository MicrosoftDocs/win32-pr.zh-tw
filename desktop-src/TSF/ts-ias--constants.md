---
title: 'TS_IAS_ 常數 (Textstor) '
description: TS \_ IAS \_ \ 常數用來作為位旗標，以控制在選取範圍或插入點插入文字或内嵌物件。
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103817"
---
# <a name="ts_ias_-constants"></a><span data-ttu-id="ab1d4-103">TS \_ IAS \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="ab1d4-103">TS\_IAS\_\* Constants</span></span>

<span data-ttu-id="ab1d4-104">TS \_ IAS \_ \* 常數是用來做為位旗標，以控制在選取範圍或插入點插入文字或内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="ab1d4-104">The TS\_IAS\_\* constants are used as bitfield flags to control insertion of text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="ab1d4-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="ab1d4-105">Constant/value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="ab1d4-106">Description</span><span class="sxs-lookup"><span data-stu-id="ab1d4-106">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <span data-ttu-id="ab1d4-107"><dt>**TS \_IAS \_ NOQUERY**</dt> <dt> ( 0x1 )</dt></span><span class="sxs-lookup"><span data-stu-id="ab1d4-107"><dt>**TS\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>       | <span data-ttu-id="ab1d4-108">在結束時插入文字，範圍指標會設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ab1d4-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="ab1d4-109">無法與 TS \_ IAS \_ QUERYONLY 旗標合併。</span><span class="sxs-lookup"><span data-stu-id="ab1d4-109">Cannot be combined with the TS\_IAS\_QUERYONLY flag.</span></span><br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <span data-ttu-id="ab1d4-110"><dt>**TS \_IAS \_ QUERYONLY**</dt> <dt> ( 0x2 )</dt></span><span class="sxs-lookup"><span data-stu-id="ab1d4-110"><dt>**TS\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="ab1d4-111">請勿執行插入。</span><span class="sxs-lookup"><span data-stu-id="ab1d4-111">Do not perform the insertion.</span></span> <span data-ttu-id="ab1d4-112">呼叫端只需要設定範圍指標。</span><span class="sxs-lookup"><span data-stu-id="ab1d4-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="ab1d4-113">無法與 TS \_ IAS \_ NOQUERY 旗標合併。</span><span class="sxs-lookup"><span data-stu-id="ab1d4-113">Cannot be combined with the TS\_IAS\_NOQUERY flag.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ab1d4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab1d4-114">Requirements</span></span>



| <span data-ttu-id="ab1d4-115">需求</span><span class="sxs-lookup"><span data-stu-id="ab1d4-115">Requirement</span></span> | <span data-ttu-id="ab1d4-116">值</span><span class="sxs-lookup"><span data-stu-id="ab1d4-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1d4-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab1d4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ab1d4-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab1d4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ab1d4-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab1d4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ab1d4-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab1d4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab1d4-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ab1d4-121">Redistributable</span></span><br/>          | <span data-ttu-id="ab1d4-122">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="ab1d4-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="ab1d4-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ab1d4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab1d4-124"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab1d4-124"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab1d4-125">Idl</span><span class="sxs-lookup"><span data-stu-id="ab1d4-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab1d4-126"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab1d4-126"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





