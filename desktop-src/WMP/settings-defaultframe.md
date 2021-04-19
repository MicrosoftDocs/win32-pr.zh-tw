---
title: 設定. defaultFrame
description: DefaultFrame 屬性會指定或抓取用來顯示 ScriptCommand 事件中所接收之 URL 的框架名稱。
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- 設定. defaultFrame Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984060"
---
# <a name="settingsdefaultframe"></a><span data-ttu-id="9743f-104">設定. defaultFrame</span><span class="sxs-lookup"><span data-stu-id="9743f-104">Settings.defaultFrame</span></span>

<span data-ttu-id="9743f-105">**DefaultFrame** 屬性會指定或抓取用來顯示 **ScriptCommand** 事件中所接收之 URL 的框架名稱。</span><span class="sxs-lookup"><span data-stu-id="9743f-105">The **defaultFrame** property specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="9743f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9743f-106">Syntax</span></span>

<span data-ttu-id="9743f-107">defaultFrame</span><span class="sxs-lookup"><span data-stu-id="9743f-107">player.settings.defaultFrame</span></span>

## <a name="possible-values"></a><span data-ttu-id="9743f-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="9743f-108">Possible Values</span></span>

<span data-ttu-id="9743f-109">這個屬性是讀取/寫入 **字串** ，對應至目標框架元素的 **name** 屬性值。</span><span class="sxs-lookup"><span data-stu-id="9743f-109">This property is a read/write **String** corresponding to the value of the **name** attribute of the target FRAME element.</span></span>

## <a name="remarks"></a><span data-ttu-id="9743f-110">備註</span><span class="sxs-lookup"><span data-stu-id="9743f-110">Remarks</span></span>

<span data-ttu-id="9743f-111">如果在 **ScriptCommand** 事件本身指定了目標框架，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9743f-111">If a target frame is specified in the **ScriptCommand** event itself, this property is ignored.</span></span>

<span data-ttu-id="9743f-112">使用 JAVA applet Netscape Navigator 時，會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9743f-112">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="9743f-113">在 [導覽器] 中，每個收到的 URL 指令碼命令都會在新的瀏覽器視窗中顯示 URL，不論 *設定* 的值為何。**defaultFrame**。</span><span class="sxs-lookup"><span data-stu-id="9743f-113">In Navigator, each URL script command received displays the URL in a new browser window, regardless of the value of *Settings*.**defaultFrame**.</span></span>

<span data-ttu-id="9743f-114">**Windows Media Player 10** 行動裝置版：此屬性是唯讀的，而且一律會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="9743f-114">**Windows Media Player 10 Mobile**: This property is read only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="9743f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9743f-115">Requirements</span></span>



| <span data-ttu-id="9743f-116">需求</span><span class="sxs-lookup"><span data-stu-id="9743f-116">Requirement</span></span> | <span data-ttu-id="9743f-117">值</span><span class="sxs-lookup"><span data-stu-id="9743f-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9743f-118">版本</span><span class="sxs-lookup"><span data-stu-id="9743f-118">Version</span></span><br/> | <span data-ttu-id="9743f-119">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9743f-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9743f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9743f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="9743f-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9743f-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9743f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9743f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9743f-123">**ScriptCommand 事件**</span><span class="sxs-lookup"><span data-stu-id="9743f-123">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="9743f-124">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="9743f-124">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="9743f-125">**使用 Windows Media Player 搭配 Netscape 7.1**</span><span class="sxs-lookup"><span data-stu-id="9743f-125">**Using Windows Media Player with Netscape 7.1**</span></span>](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





