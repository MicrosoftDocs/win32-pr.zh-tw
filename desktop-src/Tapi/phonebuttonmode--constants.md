---
description: PHONEBUTTONMODE \_ 位旗標常數描述按鈕類別。
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: 'PHONEBUTTONMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4ee5e9835b7df06773bc1429641c91597c15e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995528"
---
# <a name="phonebuttonmode_-constants"></a><span data-ttu-id="faf45-103">PHONEBUTTONMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="faf45-103">PHONEBUTTONMODE\_ Constants</span></span>

<span data-ttu-id="faf45-104">**PHONEBUTTONMODE \_** 位旗標常數描述按鈕類別。</span><span class="sxs-lookup"><span data-stu-id="faf45-104">The **PHONEBUTTONMODE\_** bit-flag constants describe the button classes.</span></span>

<dl> <dt>

<span data-ttu-id="faf45-105"><span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**PHONEBUTTONMODE \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="faf45-105"><span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**PHONEBUTTONMODE\_CALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="faf45-106">按鈕會指派給呼叫外觀。</span><span class="sxs-lookup"><span data-stu-id="faf45-106">The button is assigned to a call appearance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faf45-107"><span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**PHONEBUTTONMODE \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="faf45-107"><span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**PHONEBUTTONMODE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="faf45-108">按鈕是與手機顯示相關聯的「軟」按鈕。</span><span class="sxs-lookup"><span data-stu-id="faf45-108">The button is a "soft" button associated with the phone's display.</span></span> <span data-ttu-id="faf45-109">電話組可以有零或多個顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="faf45-109">A phone set can have zero or more display buttons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faf45-110"><span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE \_ 虛擬**</span><span class="sxs-lookup"><span data-stu-id="faf45-110"><span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE\_DUMMY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="faf45-111">此值可用來描述沒有對應按鈕但只有燈泡的按鈕/燈泡位置。</span><span class="sxs-lookup"><span data-stu-id="faf45-111">This value is used to describe a button/lamp position that has no corresponding button but has only a lamp.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faf45-112"><span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**PHONEBUTTONMODE \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="faf45-112"><span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**PHONEBUTTONMODE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="faf45-113">此按鈕會指派給從交換器要求的功能，例如保存、會議和傳輸。</span><span class="sxs-lookup"><span data-stu-id="faf45-113">The button is assigned to requesting features from the switch, such as hold, conference, and transfer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faf45-114"><span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**PHONEBUTTONMODE \_ 鍵台**</span><span class="sxs-lookup"><span data-stu-id="faf45-114"><span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**PHONEBUTTONMODE\_KEYPAD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="faf45-115">按鈕是12鍵台按鈕的其中之一，0到9、' \* ' 和 ' \# '。</span><span class="sxs-lookup"><span data-stu-id="faf45-115">The button is one of the twelve keypad buttons, 0 through 9, '\*', and '\#'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="faf45-116"><span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ 本機**</span><span class="sxs-lookup"><span data-stu-id="faf45-116"><span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="faf45-117">按鈕是區域的功能按鈕，例如靜音或音量控制。</span><span class="sxs-lookup"><span data-stu-id="faf45-117">The button is a local function button, such as mute or volume control.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="faf45-118">備註</span><span class="sxs-lookup"><span data-stu-id="faf45-118">Remarks</span></span>

<span data-ttu-id="faf45-119">無延伸。</span><span class="sxs-lookup"><span data-stu-id="faf45-119">No extensibility.</span></span> <span data-ttu-id="faf45-120">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="faf45-120">All 32 bits are reserved.</span></span>

<span data-ttu-id="faf45-121">此列舉型別會在 [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) 資料結構中用來描述與電話按鈕相關聯的意義。</span><span class="sxs-lookup"><span data-stu-id="faf45-121">This enumeration type is used in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) data structure to describe the meaning associated with the phone's buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="faf45-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="faf45-122">Requirements</span></span>



| <span data-ttu-id="faf45-123">需求</span><span class="sxs-lookup"><span data-stu-id="faf45-123">Requirement</span></span> | <span data-ttu-id="faf45-124">值</span><span class="sxs-lookup"><span data-stu-id="faf45-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="faf45-125">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="faf45-125">TAPI version</span></span><br/> | <span data-ttu-id="faf45-126">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="faf45-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="faf45-127">標頭</span><span class="sxs-lookup"><span data-stu-id="faf45-127">Header</span></span><br/>       | <dl> <span data-ttu-id="faf45-128"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="faf45-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




