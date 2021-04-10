---
title: Hide 方法
description: Hide 方法
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092694"
---
# <a name="hide-method"></a><span data-ttu-id="2c832-103">Hide 方法</span><span class="sxs-lookup"><span data-stu-id="2c832-103">Hide Method</span></span>

<span data-ttu-id="2c832-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2c832-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2c832-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="2c832-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2c832-106">隱藏指定的字元。</span><span class="sxs-lookup"><span data-stu-id="2c832-106">Hides the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="2c832-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="2c832-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2c832-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。隱藏* \*  \[ *快速*\]</span><span class="sxs-lookup"><span data-stu-id="2c832-108">*agent ***.Characters ("*** CharacterID\*\*\*").Hide*\* \[*Fast*\]</span></span>



| <span data-ttu-id="2c832-109">部分</span><span class="sxs-lookup"><span data-stu-id="2c832-109">Part</span></span>   | <span data-ttu-id="2c832-110">描述</span><span class="sxs-lookup"><span data-stu-id="2c832-110">Description</span></span>                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c832-111">*快速*</span><span class="sxs-lookup"><span data-stu-id="2c832-111">*Fast*</span></span> | <span data-ttu-id="2c832-112">選擇性。</span><span class="sxs-lookup"><span data-stu-id="2c832-112">Optional.</span></span> <span data-ttu-id="2c832-113">布林值，指出是否略過與字元隱藏狀態 **True** 相關聯的動畫不播放 **隱藏** 動畫。</span><span class="sxs-lookup"><span data-stu-id="2c832-113">A Boolean value that indicates whether to skip the animation associated with the character's Hiding state **True** Does not play the **Hiding** animation.</span></span> <br/> <span data-ttu-id="2c832-114">**False** (預設) 播放 **隱藏** 動畫。</span><span class="sxs-lookup"><span data-stu-id="2c832-114">**False** (Default) Plays the **Hiding** animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c832-115">備註</span><span class="sxs-lookup"><span data-stu-id="2c832-115">Remarks</span></span>

<span data-ttu-id="2c832-116">伺服器會在字元的佇列中將 **Hide** 方法的動作排入佇列，讓您可以使用它來隱藏其他動畫序列之後的字元。</span><span class="sxs-lookup"><span data-stu-id="2c832-116">The server queues the actions of the **Hide** method in the character's queue, so you can use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="2c832-117">您可以在呼叫這個方法之前，使用 [**Stop**](stop-method.md) 方法立即播放動作。</span><span class="sxs-lookup"><span data-stu-id="2c832-117">You can play the action immediately by using the [**Stop**](stop-method.md) method before calling this method.</span></span>

<span data-ttu-id="2c832-118">如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="2c832-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="2c832-119">此外，如果關聯的 **隱藏** 動畫尚未載入，而且您尚未將 **Fast** 參數指定為 **True**，則伺服器會將 [ **要求** 物件 [**狀態**](status-property.md) ] 屬性設定為 [失敗]，並提供適當的錯誤號碼。</span><span class="sxs-lookup"><span data-stu-id="2c832-119">In addition, if the associated **Hiding** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="2c832-120">因此，如果您使用 HTTP 通訊協定來存取字元或動畫資料，請使用 [**Get**](get-method.md)方法，並在呼叫 **Hide** 方法之前，指定要載入動畫的 **隱藏** 狀態。</span><span class="sxs-lookup"><span data-stu-id="2c832-120">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method and specify the **Hiding** state to load the animation before calling the **Hide** method.</span></span>

<span data-ttu-id="2c832-121">隱藏字元也可能導致觸發另一個用戶端的 [**ActivateInput**](activateinput-event.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="2c832-121">Hiding a character can also result in triggering the [**ActivateInput**](activateinput-event.md) event of another client.</span></span>

> [!Note]  
> <span data-ttu-id="2c832-122">隱藏的字元無法存取音訊通道。</span><span class="sxs-lookup"><span data-stu-id="2c832-122">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="2c832-123">如果您產生動畫要求且隱藏字元，伺服器將會在 [**RequestComplete**](requestcomplete-event.md) 事件中傳回失敗狀態。</span><span class="sxs-lookup"><span data-stu-id="2c832-123">The server will pass back a failure status in the [**RequestComplete**](requestcomplete-event.md) event if you generate an animation request and the character is hidden.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="2c832-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c832-124">See Also</span></span>

[<span data-ttu-id="2c832-125">**Show 方法**</span><span class="sxs-lookup"><span data-stu-id="2c832-125">**Show method**</span></span>](show-method.md)


 

