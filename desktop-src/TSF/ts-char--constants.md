---
title: 'TS_CHAR_ 常數 (Textstor) '
description: TS \_ CHAR \_ \ 常數描述字元的類型。
ms.assetid: b40ca931-d45c-4101-9380-bb2b3ad25fba
topic_type:
- apiref
api_name:
- TS_CHAR_EMBEDDED
- TS_CHAR_REGION
- TS_CHAR_REPLACEMENT
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25f66006dcb37e2504785b2b28ca1f328edfcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384370"
---
# <a name="ts_char_-constants"></a><span data-ttu-id="bf675-103">TS \_ CHAR \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="bf675-103">TS\_CHAR\_\* Constants</span></span>

<span data-ttu-id="bf675-104">TS \_ CHAR \_ \* 常數描述字元的類型。</span><span class="sxs-lookup"><span data-stu-id="bf675-104">The TS\_CHAR\_\* constants describe the type of character.</span></span>



| <span data-ttu-id="bf675-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="bf675-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="bf675-106">Description</span><span class="sxs-lookup"><span data-stu-id="bf675-106">Description</span></span>                                                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| <span id="TS_CHAR_EMBEDDED"></span><span id="ts_char_embedded"></span><dl> <span data-ttu-id="bf675-107"><dt>**TS \_CHAR \_ EMBEDDED**</dt> <dt> ( 0xfffc )</dt></span><span class="sxs-lookup"><span data-stu-id="bf675-107"><dt>**TS\_CHAR\_EMBEDDED**</dt> <dt>( 0xfffc )</dt></span></span> </dl>          | <span data-ttu-id="bf675-108">字元是 Unicode 2.1 物件取代字元。</span><span class="sxs-lookup"><span data-stu-id="bf675-108">The character is a Unicode 2.1 object-replacement character.</span></span><br/>                             |
| <span id="TS_CHAR_REGION"></span><span id="ts_char_region"></span><dl> <span data-ttu-id="bf675-109"><dt>**TS \_CHAR \_ 區域**</dt> <dt> ( 0 )</dt></span><span class="sxs-lookup"><span data-stu-id="bf675-109"><dt>**TS\_CHAR\_REGION**</dt> <dt>( 0 )</dt></span></span> </dl>                     | <span data-ttu-id="bf675-110">字元是區域界限。</span><span class="sxs-lookup"><span data-stu-id="bf675-110">The character is a region boundary.</span></span><br/>                                                      |
| <span id="TS_CHAR_REPLACEMENT"></span><span id="ts_char_replacement"></span><dl> <span data-ttu-id="bf675-111"><dt>**TS \_字元 \_ 取代**</dt> <dt> ( 0xfffd )</dt></span><span class="sxs-lookup"><span data-stu-id="bf675-111"><dt>**TS\_CHAR\_REPLACEMENT**</dt> <dt>( 0xfffd )</dt></span></span> </dl> | <span data-ttu-id="bf675-112">字元是隱藏文字預留位置字元或 Unicode 取代字元。</span><span class="sxs-lookup"><span data-stu-id="bf675-112">The character is a hidden-text placeholder character or a Unicode replacement character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bf675-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf675-113">Requirements</span></span>



| <span data-ttu-id="bf675-114">需求</span><span class="sxs-lookup"><span data-stu-id="bf675-114">Requirement</span></span> | <span data-ttu-id="bf675-115">值</span><span class="sxs-lookup"><span data-stu-id="bf675-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf675-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf675-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bf675-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf675-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bf675-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf675-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bf675-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf675-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf675-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="bf675-120">Redistributable</span></span><br/>          | <span data-ttu-id="bf675-121">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="bf675-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="bf675-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bf675-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf675-123"><dt>Textstor。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf675-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf675-124">Idl</span><span class="sxs-lookup"><span data-stu-id="bf675-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bf675-125"><dt>Textstor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bf675-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf675-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf675-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf675-127">内嵌物件</span><span class="sxs-lookup"><span data-stu-id="bf675-127">Embedded Objects</span></span>](embedded-objects.md)
</dt> </dl>

 

 





