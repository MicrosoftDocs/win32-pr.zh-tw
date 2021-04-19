---
title: " (舊版 Windows 環境功能的 Play 方法) "
description: Play 方法
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967303"
---
# <a name="play-method-legacy-windows-environment-features"></a><span data-ttu-id="5974e-103"> (舊版 Windows 環境功能的 Play 方法) </span><span class="sxs-lookup"><span data-stu-id="5974e-103">Play Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="5974e-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5974e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5974e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="5974e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5974e-106">針對指定的字元播放指定的動畫。</span><span class="sxs-lookup"><span data-stu-id="5974e-106">Plays the specified animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="5974e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="5974e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5974e-108">\*代理程式 \***。 ( "**_CharacterID_*_" ) 的字元。Play_* "*AnimationName*"</span><span class="sxs-lookup"><span data-stu-id="5974e-108">*agent\***.Characters ("**_CharacterID_*_").Play_\* "*AnimationName*"</span></span>

</dd> </dl> 

| <span data-ttu-id="5974e-109">部分</span><span class="sxs-lookup"><span data-stu-id="5974e-109">Part</span></span>            | <span data-ttu-id="5974e-110">描述</span><span class="sxs-lookup"><span data-stu-id="5974e-110">Description</span></span>                                                          |
|-----------------|----------------------------------------------------------------------|
| <span data-ttu-id="5974e-111">*AnimationName*</span><span class="sxs-lookup"><span data-stu-id="5974e-111">*AnimationName*</span></span> | <span data-ttu-id="5974e-112">必要。</span><span class="sxs-lookup"><span data-stu-id="5974e-112">Required.</span></span> <span data-ttu-id="5974e-113">指定動畫順序名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="5974e-113">A string that specifies the name of an animation sequence.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5974e-114">備註</span><span class="sxs-lookup"><span data-stu-id="5974e-114">Remarks</span></span>

<span data-ttu-id="5974e-115">使用 Microsoft Agent 字元編輯器來編譯字元時，會定義動畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5974e-115">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="5974e-116">在播放指定的動畫之前，伺服器會嘗試播放先前 **動畫的傳回動畫（** 如果已指派）。</span><span class="sxs-lookup"><span data-stu-id="5974e-116">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation, if one has been assigned.</span></span>

<span data-ttu-id="5974e-117">使用傳統檔案通訊協定來存取字元的動畫時，您可以直接使用 **Play** 方法指定動畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5974e-117">When accessing a character's animations using a conventional file protocol, you can simply use the **Play** method specifying the name of the animation.</span></span> <span data-ttu-id="5974e-118">但是，如果您使用 HTTP 通訊協定來存取字元動畫資料，請在呼叫 **Play** 方法之前，使用 **Get** 方法載入動畫。</span><span class="sxs-lookup"><span data-stu-id="5974e-118">However, if you are using the HTTP protocol to access character animation data, use the **Get** method to load the animation before calling the **Play** method.</span></span>

<span data-ttu-id="5974e-119">如需詳細資訊，請參閱 **Get** 方法。</span><span class="sxs-lookup"><span data-stu-id="5974e-119">For more information, see the **Get** method.</span></span>

<span data-ttu-id="5974e-120">若要簡化您的語法，您可以宣告物件參考，並將它設定為參考 [**字元**](/windows/desktop/lwef/the-characters-object)集合中的 [**字元**](/windows/desktop/lwef/the-characters-object)物件，並使用參考作為 **播放** 語句的一部分：</span><span class="sxs-lookup"><span data-stu-id="5974e-120">To simplify your syntax, you can declare an object reference and set it to reference the [**Character**](/windows/desktop/lwef/the-characters-object) object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection and use the reference as part of your **Play** statements:</span></span>


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



<span data-ttu-id="5974e-121">如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="5974e-121">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="5974e-122">此外，如果您指定未載入的動畫或未成功載入該字元，伺服器會將 **要求** 物件的 [**Status**](status-property.md)屬性設為「失敗」，並提供適當的錯誤號碼。</span><span class="sxs-lookup"><span data-stu-id="5974e-122">In addition, if you specify an animation that is not loaded or if the character has not been successfully loaded, the server sets the [**Status**](status-property.md) property of **Request** object to "failed" with an appropriate error number.</span></span> <span data-ttu-id="5974e-123">但是，如果動畫不存在，且已成功載入字元的資料，伺服器就會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="5974e-123">However, if the animation does not exist and the character's data has already been successfully loaded, the server raises an error.</span></span>

<span data-ttu-id="5974e-124">**Play** 方法不會讓字元變成可見。</span><span class="sxs-lookup"><span data-stu-id="5974e-124">The **Play** method does not make the character visible.</span></span> <span data-ttu-id="5974e-125">如果看不到字元，伺服器會以不可見的狀態播放動畫，並設定 [**Request**](/windows/desktop/lwef/the-request-object)物件的 [**Status**](status-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="5974e-125">If the character is not visible, the server plays the animation invisibly, and sets the [**Status**](status-property.md) property of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 
