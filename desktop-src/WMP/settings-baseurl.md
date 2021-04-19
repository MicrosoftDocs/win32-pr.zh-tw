---
title: 設定. baseURL
description: BaseURL 屬性會指定或抓取基底 URL，這個基底 URL 使用內嵌在媒體專案中的 URL 指令碼命令來解析相對路徑。
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- 設定. baseURL Windows Media Player
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994183"
---
# <a name="settingsbaseurl"></a><span data-ttu-id="53aa7-104">設定. baseURL</span><span class="sxs-lookup"><span data-stu-id="53aa7-104">Settings.baseURL</span></span>

<span data-ttu-id="53aa7-105">**BaseURL** 屬性會指定或抓取基底 URL，這個基底 url 使用內嵌在媒體專案中的 URL 指令碼命令來解析相對路徑。</span><span class="sxs-lookup"><span data-stu-id="53aa7-105">The **baseURL** property specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="53aa7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="53aa7-106">Syntax</span></span>

<span data-ttu-id="53aa7-107">baseURL</span><span class="sxs-lookup"><span data-stu-id="53aa7-107">player.settings.baseURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="53aa7-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="53aa7-108">Possible Values</span></span>

<span data-ttu-id="53aa7-109">這個屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="53aa7-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="53aa7-110">備註</span><span class="sxs-lookup"><span data-stu-id="53aa7-110">Remarks</span></span>

<span data-ttu-id="53aa7-111">這個屬性會指定 **ScriptCommand** 事件以命令參數形式傳遞的基底 HTTP URL。</span><span class="sxs-lookup"><span data-stu-id="53aa7-111">This property specifies the base HTTP URL that is passed as the command parameter by the **ScriptCommand** event.</span></span> <span data-ttu-id="53aa7-112">基底 URL 會與相對 URL 串連，如下所示：</span><span class="sxs-lookup"><span data-stu-id="53aa7-112">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="53aa7-113">尾端正斜線 (/) 會新增至 **baseURL** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="53aa7-113">A trailing forward slash (/) is added to the value of the **baseURL** property.</span></span>
2.  <span data-ttu-id="53aa7-114">前置句點、反斜線或正斜線 (.、 \\ 和/) 會從相對 URL 中刪除。</span><span class="sxs-lookup"><span data-stu-id="53aa7-114">A leading period, backward slash, or forward slash (., \\, and /) are deleted from the relative URL.</span></span>
3.  <span data-ttu-id="53aa7-115">相對 URL 會新增至基底 URL 的結尾。</span><span class="sxs-lookup"><span data-stu-id="53aa7-115">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="53aa7-116">產生的完整 URL 中的所有斜線都會指向相同方向 (轉換成正斜線或反斜線) 根據新 URL 中遇到的第一個斜線字元的方向。</span><span class="sxs-lookup"><span data-stu-id="53aa7-116">All slashes in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="53aa7-117">**注意**</span><span class="sxs-lookup"><span data-stu-id="53aa7-117">**Note**</span></span>

<span data-ttu-id="53aa7-118">播放機控制項不支援使用兩個期間 (。在相對 URL 中 ) ，表示目前位置的父系。</span><span class="sxs-lookup"><span data-stu-id="53aa7-118">The player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

<span data-ttu-id="53aa7-119">**Windows Media Player 10** 行動裝置版：此屬性是唯讀的，而且一律會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="53aa7-119">**Windows Media Player 10 Mobile**: This property is read-only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="53aa7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="53aa7-120">Requirements</span></span>



| <span data-ttu-id="53aa7-121">需求</span><span class="sxs-lookup"><span data-stu-id="53aa7-121">Requirement</span></span> | <span data-ttu-id="53aa7-122">值</span><span class="sxs-lookup"><span data-stu-id="53aa7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53aa7-123">版本</span><span class="sxs-lookup"><span data-stu-id="53aa7-123">Version</span></span><br/> | <span data-ttu-id="53aa7-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="53aa7-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="53aa7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="53aa7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="53aa7-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53aa7-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53aa7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53aa7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53aa7-128">**ScriptCommand 事件**</span><span class="sxs-lookup"><span data-stu-id="53aa7-128">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="53aa7-129">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="53aa7-129">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





