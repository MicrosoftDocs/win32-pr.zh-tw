---
title: StopAll 方法
description: StopAll 方法
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968276"
---
# <a name="stopall-method"></a><span data-ttu-id="d73dd-103">StopAll 方法</span><span class="sxs-lookup"><span data-stu-id="d73dd-103">StopAll Method</span></span>

<span data-ttu-id="d73dd-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d73dd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d73dd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="d73dd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d73dd-106">停止指定字元的所有動畫要求或指定類型的要求。</span><span class="sxs-lookup"><span data-stu-id="d73dd-106">Stops all animation requests or specified types of requests for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="d73dd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="d73dd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d73dd-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。StopAll* \*  \[ *類型*\]</span><span class="sxs-lookup"><span data-stu-id="d73dd-108">*agent ***.Characters ("*** CharacterID\*\*\*").StopAll*\* \[*Type*\]</span></span>



| <span data-ttu-id="d73dd-109">部分</span><span class="sxs-lookup"><span data-stu-id="d73dd-109">Part</span></span>   | <span data-ttu-id="d73dd-110">描述</span><span class="sxs-lookup"><span data-stu-id="d73dd-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d73dd-111">*型別*</span><span class="sxs-lookup"><span data-stu-id="d73dd-111">*Type*</span></span> | <span data-ttu-id="d73dd-112">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d73dd-112">Optional.</span></span> <span data-ttu-id="d73dd-113">若要使用此參數，您可以使用下列任何一個值。</span><span class="sxs-lookup"><span data-stu-id="d73dd-113">To use this parameter you can use any of the following values.</span></span> <span data-ttu-id="d73dd-114">您也可以使用逗號分隔來指定多個類型。</span><span class="sxs-lookup"><span data-stu-id="d73dd-114">You can also specify multiple types by separating them with commas.</span></span> <br/> <span data-ttu-id="d73dd-115">"**Get**"</span><span class="sxs-lookup"><span data-stu-id="d73dd-115">"**Get**"</span></span> <br/> <span data-ttu-id="d73dd-116">停止所有已排入佇列的 [**Get**](get-method.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="d73dd-116">To stop all queued [**Get**](get-method.md) requests.</span></span><br/> <span data-ttu-id="d73dd-117">"**NonQueuedGet**"</span><span class="sxs-lookup"><span data-stu-id="d73dd-117">"**NonQueuedGet**"</span></span> <br/> <span data-ttu-id="d73dd-118">若要停止所有非佇列的 [**get**](get-method.md) 要求 (**Get** 方法，並將 **Queue** 參數設定為 **False**) 。</span><span class="sxs-lookup"><span data-stu-id="d73dd-118">To stop all non-queued [**Get**](get-method.md) requests (**Get** method with **Queue** parameter set to **False**).</span></span><br/> <span data-ttu-id="d73dd-119">「**移動**」</span><span class="sxs-lookup"><span data-stu-id="d73dd-119">"**Move**"</span></span> <br/> <span data-ttu-id="d73dd-120">停止所有已排入佇列的 [**MoveTo**](moveto-method.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="d73dd-120">To stop all queued [**MoveTo**](moveto-method.md) requests.</span></span><br/> <span data-ttu-id="d73dd-121">「**播放**」</span><span class="sxs-lookup"><span data-stu-id="d73dd-121">"**Play**"</span></span> <br/> <span data-ttu-id="d73dd-122">停止所有已排入佇列的 [**播放**](play-method.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="d73dd-122">To stop all queued [**Play**](play-method.md) requests.</span></span><br/> <span data-ttu-id="d73dd-123">「**說話**」</span><span class="sxs-lookup"><span data-stu-id="d73dd-123">"**Speak**"</span></span> <br/> <span data-ttu-id="d73dd-124">停止所有已排入佇列的 [**朗讀**](speak-method.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="d73dd-124">To stop all queued [**Speak**](speak-method.md) requests.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d73dd-125">備註</span><span class="sxs-lookup"><span data-stu-id="d73dd-125">Remarks</span></span>

<span data-ttu-id="d73dd-126">如果您未設定 **Type** 參數，伺服器會停止該字元的所有動畫，包括已排入佇列和非佇列的 [**Get**](get-method.md) 要求，並清除其動畫佇列。</span><span class="sxs-lookup"><span data-stu-id="d73dd-126">If you don't set the **Type** parameter, the server stops all animations for the character, including queued and non-queued [**Get**](get-method.md) requests, and clears its animation queue.</span></span> <span data-ttu-id="d73dd-127">它也會停止播放隱藏或顯示動畫的字元。</span><span class="sxs-lookup"><span data-stu-id="d73dd-127">It also stops playing a character's Hiding or Showing animation.</span></span>

<span data-ttu-id="d73dd-128">這個方法不會產生 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="d73dd-128">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="d73dd-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d73dd-129">See Also</span></span>

[<span data-ttu-id="d73dd-130">**Stop 方法**</span><span class="sxs-lookup"><span data-stu-id="d73dd-130">**Stop method**</span></span>](stop-method.md)


 

