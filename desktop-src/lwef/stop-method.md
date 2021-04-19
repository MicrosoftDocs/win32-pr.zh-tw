---
title: " (舊版 Windows 環境功能的 Stop 方法) "
description: Stop 方法
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106968735"
---
# <a name="stop-method-legacy-windows-environment-features"></a><span data-ttu-id="38aa8-103"> (舊版 Windows 環境功能的 Stop 方法) </span><span class="sxs-lookup"><span data-stu-id="38aa8-103">Stop Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="38aa8-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="38aa8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="38aa8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="38aa8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="38aa8-106">停止指定字元的動畫。</span><span class="sxs-lookup"><span data-stu-id="38aa8-106">Stops the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="38aa8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="38aa8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="38aa8-108">\*代理程式 \***。 ( "**_CharacterID_\*_" ) 的字元。停止_ \*  \[ *要求*\]</span><span class="sxs-lookup"><span data-stu-id="38aa8-108">*agent\***.Characters ("**_CharacterID_*_").Stop_\* \[*Request*\]</span></span>



| <span data-ttu-id="38aa8-109">部分</span><span class="sxs-lookup"><span data-stu-id="38aa8-109">Part</span></span>      | <span data-ttu-id="38aa8-110">描述</span><span class="sxs-lookup"><span data-stu-id="38aa8-110">Description</span></span>                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="38aa8-111">*要求*</span><span class="sxs-lookup"><span data-stu-id="38aa8-111">*Request*</span></span> | <span data-ttu-id="38aa8-112">選擇性。</span><span class="sxs-lookup"><span data-stu-id="38aa8-112">Optional.</span></span> <span data-ttu-id="38aa8-113">指定特定動畫呼叫的 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="38aa8-113">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38aa8-114">備註</span><span class="sxs-lookup"><span data-stu-id="38aa8-114">Remarks</span></span>

<span data-ttu-id="38aa8-115">若要指定要求參數，您必須建立變數，並指派您要停止的動畫要求。</span><span class="sxs-lookup"><span data-stu-id="38aa8-115">To specify the request parameter, you must create a variable and assign the animation request you want to stop.</span></span> <span data-ttu-id="38aa8-116">如果您未設定 **Request** 參數，伺服器會停止該字元的所有動畫，包括已排入佇列的 [**Get**](get-method.md) 呼叫，並清除其動畫佇列，除非該字元目前現正播放 **隱藏** 或 **顯示** 動畫。</span><span class="sxs-lookup"><span data-stu-id="38aa8-116">If you don't set the **Request** parameter, the server stops all animations for the character, including queued [**Get**](get-method.md) calls, and clears its animation queue unless the character is currently playing its **Hiding** or **Showing** animation.</span></span> <span data-ttu-id="38aa8-117">這個方法不會停止未排入佇列的 **Get** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="38aa8-117">This method does not stop non-queued **Get** calls.</span></span>

<span data-ttu-id="38aa8-118">若要停止特定動畫或 [**取得**](get-method.md) 呼叫，請宣告物件變數，並將您的動畫要求指派給該變數：</span><span class="sxs-lookup"><span data-stu-id="38aa8-118">To stop a specific animation or [**Get**](get-method.md) call, declare an object variable and assign your animation request to that variable:</span></span>


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



<span data-ttu-id="38aa8-119">這個方法不會產生 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="38aa8-119">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="38aa8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38aa8-120">See Also</span></span>

[<span data-ttu-id="38aa8-121">**StopAll 方法**</span><span class="sxs-lookup"><span data-stu-id="38aa8-121">**StopAll method**</span></span>](stopall-method.md)


 

 
