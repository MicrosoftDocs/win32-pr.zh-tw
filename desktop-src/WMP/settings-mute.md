---
title: 設定。靜音
description: '[靜音] 屬性會指定並抓取值，指出音訊是否為靜音。'
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- 設定。靜音 Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989582"
---
# <a name="settingsmute"></a><span data-ttu-id="8c446-104">設定。靜音</span><span class="sxs-lookup"><span data-stu-id="8c446-104">Settings.mute</span></span>

<span data-ttu-id="8c446-105">[ **靜音** ] 屬性會指定並抓取值，指出音訊是否為靜音。</span><span class="sxs-lookup"><span data-stu-id="8c446-105">The **mute** property specifies and retrieves a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c446-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c446-106">Syntax</span></span>

<span data-ttu-id="8c446-107">播放的設定。靜音</span><span class="sxs-lookup"><span data-stu-id="8c446-107">player.settings.mute</span></span>

## <a name="possible-values"></a><span data-ttu-id="8c446-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="8c446-108">Possible Values</span></span>

<span data-ttu-id="8c446-109">這個屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="8c446-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="8c446-110">值</span><span class="sxs-lookup"><span data-stu-id="8c446-110">Value</span></span> | <span data-ttu-id="8c446-111">描述</span><span class="sxs-lookup"><span data-stu-id="8c446-111">Description</span></span>                  |
|-------|------------------------------|
| <span data-ttu-id="8c446-112">true</span><span class="sxs-lookup"><span data-stu-id="8c446-112">true</span></span>  | <span data-ttu-id="8c446-113">音訊已靜音。</span><span class="sxs-lookup"><span data-stu-id="8c446-113">Audio is muted.</span></span>              |
| <span data-ttu-id="8c446-114">false</span><span class="sxs-lookup"><span data-stu-id="8c446-114">false</span></span> | <span data-ttu-id="8c446-115">預設值。</span><span class="sxs-lookup"><span data-stu-id="8c446-115">Default.</span></span> <span data-ttu-id="8c446-116">音訊未靜音。</span><span class="sxs-lookup"><span data-stu-id="8c446-116">Audio is not muted.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="8c446-117">範例</span><span class="sxs-lookup"><span data-stu-id="8c446-117">Examples</span></span>

<span data-ttu-id="8c446-118">下列範例會建立一個 HTML CHECKBOX 元素，讓使用者可以將音訊靜音並取消靜音。</span><span class="sxs-lookup"><span data-stu-id="8c446-118">The following example creates an HTML CHECKBOX element that allows the user to mute and un-mute audio.</span></span> <span data-ttu-id="8c446-119">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c446-119">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a><span data-ttu-id="8c446-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c446-120">Requirements</span></span>



| <span data-ttu-id="8c446-121">需求</span><span class="sxs-lookup"><span data-stu-id="8c446-121">Requirement</span></span> | <span data-ttu-id="8c446-122">值</span><span class="sxs-lookup"><span data-stu-id="8c446-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c446-123">版本</span><span class="sxs-lookup"><span data-stu-id="8c446-123">Version</span></span><br/> | <span data-ttu-id="8c446-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8c446-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8c446-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8c446-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c446-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c446-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c446-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c446-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c446-128">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="8c446-128">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





