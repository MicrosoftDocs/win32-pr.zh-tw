---
title: Show 方法
description: Show 方法
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965640"
---
# <a name="show-method"></a><span data-ttu-id="2db6d-103">Show 方法</span><span class="sxs-lookup"><span data-stu-id="2db6d-103">Show Method</span></span>

<span data-ttu-id="2db6d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2db6d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2db6d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="2db6d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2db6d-106">使指定的字元可見，並播放其相關聯的 **顯示** 動畫。</span><span class="sxs-lookup"><span data-stu-id="2db6d-106">Makes the specified character visible and plays its associated **Showing** animation.</span></span>

</dd> <dt>

<span data-ttu-id="2db6d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="2db6d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2db6d-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。顯示* \*  \[ *快速*\]</span><span class="sxs-lookup"><span data-stu-id="2db6d-108">*agent ***.Characters ("*** CharacterID\*\*\*").Show*\* \[*Fast*\]</span></span>



| <span data-ttu-id="2db6d-109">部分</span><span class="sxs-lookup"><span data-stu-id="2db6d-109">Part</span></span>   | <span data-ttu-id="2db6d-110">描述</span><span class="sxs-lookup"><span data-stu-id="2db6d-110">Description</span></span>                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db6d-111">*快速*</span><span class="sxs-lookup"><span data-stu-id="2db6d-111">*Fast*</span></span> | <span data-ttu-id="2db6d-112">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2db6d-112">Optional.</span></span> <span data-ttu-id="2db6d-113">指定伺服器是否會播放 **顯示** 動畫的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="2db6d-113">A Boolean expression specifying whether the server plays the **Showing** animation.</span></span> <span data-ttu-id="2db6d-114">**True** 略過 **顯示** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="2db6d-114">**True** Skips the **Showing** state animation.</span></span> <br/> <span data-ttu-id="2db6d-115">**False** (預設) 不會略過 **顯示** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="2db6d-115">**False** (Default) Does not skip the **Showing** state animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2db6d-116">備註</span><span class="sxs-lookup"><span data-stu-id="2db6d-116">Remarks</span></span>

<span data-ttu-id="2db6d-117">如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="2db6d-117">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="2db6d-118">此外，如果關聯的 **顯示** 動畫尚未載入，而且您尚未將 **Fast** 參數指定為 **True**，則伺服器會將 **要求** 物件的 [**Status**](status-property.md) 屬性設為「失敗」，並提供適當的錯誤號碼。</span><span class="sxs-lookup"><span data-stu-id="2db6d-118">In addition, if the associated **Showing** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="2db6d-119">因此，如果您使用 HTTP 通訊協定來存取字元動畫資料，請在呼叫 **Show** 方法之前，使用 [**Get**](get-method.md)方法載入 **顯示** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="2db6d-119">Therefore, if you are using the HTTP protocol to access character animation data, use the [**Get**](get-method.md) method to load the **Showing** state animation before calling the **Show** method.</span></span>

<span data-ttu-id="2db6d-120">避免將 **Fast** 參數設定為 **True** ，而不先事先播放動畫;否則，字元框架可能不會顯示任何影像。</span><span class="sxs-lookup"><span data-stu-id="2db6d-120">Avoid setting the **Fast** parameter to **True** without first playing an animation beforehand; otherwise, the character frame may display with no image.</span></span> <span data-ttu-id="2db6d-121">尤其要注意的是，如果您在字元未顯示時呼叫 [**MoveTo**](moveto-method.md) ，則不會播放任何動畫。</span><span class="sxs-lookup"><span data-stu-id="2db6d-121">In particular, note that if you call [**MoveTo**](moveto-method.md) when the character is not visible, it does not play any animation.</span></span> <span data-ttu-id="2db6d-122">因此，如果您以 **Fast** 設定為 **True** 來呼叫 **Show** 方法，則不會顯示任何影像。</span><span class="sxs-lookup"><span data-stu-id="2db6d-122">Therefore, if you call the **Show** method with **Fast** set to **True**, no image will display.</span></span> <span data-ttu-id="2db6d-123">同樣地，如果您呼叫 [[**隱藏**](hide-method.md)]，並將 [**快速\*\*\*\*顯示**] 設定為 [ **True**]，就不會有可見的影像。</span><span class="sxs-lookup"><span data-stu-id="2db6d-123">Similarly, if you call [**Hide**](hide-method.md) then **Show** with **Fast** set to **True**, there will be no visible image.</span></span>

## <a name="see-also"></a><span data-ttu-id="2db6d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2db6d-124">See Also</span></span>

[<span data-ttu-id="2db6d-125">**Hide 方法**</span><span class="sxs-lookup"><span data-stu-id="2db6d-125">**Hide method**</span></span>](hide-method.md)


 

