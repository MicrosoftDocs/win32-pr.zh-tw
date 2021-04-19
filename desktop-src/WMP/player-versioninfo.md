---
title: VersionInfo
description: VersionInfo 屬性會捕獲指定 Windows Media Player 版本的字串值。
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- VersionInfo Windows Media Player
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998608"
---
# <a name="playerversioninfo"></a><span data-ttu-id="f7fe5-104">VersionInfo</span><span class="sxs-lookup"><span data-stu-id="f7fe5-104">Player.versionInfo</span></span>

<span data-ttu-id="f7fe5-105">**VersionInfo** 屬性會捕獲指定 Windows Media Player 版本的字串值。</span><span class="sxs-lookup"><span data-stu-id="f7fe5-105">The **versionInfo** property retrieves a String value specifying the version of the Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7fe5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7fe5-106">Syntax</span></span>

<span data-ttu-id="f7fe5-107">*玩家* 。**versionInfo**</span><span class="sxs-lookup"><span data-stu-id="f7fe5-107">*player* .**versionInfo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f7fe5-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="f7fe5-108">Possible Values</span></span>

<span data-ttu-id="f7fe5-109">這個屬性是唯讀 **字串** ，格式如下： "*X*. 0.0。*Yyyy*」，其中 *X* 代表主要版本號碼，而 *yyyy* 代表組建編號。</span><span class="sxs-lookup"><span data-stu-id="f7fe5-109">This property is a read-only **String** in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="f7fe5-110">範例</span><span class="sxs-lookup"><span data-stu-id="f7fe5-110">Examples</span></span>

<span data-ttu-id="f7fe5-111">下列範例會建立 HTML BUTTON 專案，按此按鈕時，會顯示訊息方塊，其中包含 Windows Media Player 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="f7fe5-111">The following example creates an HTML BUTTON element that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="f7fe5-112">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="f7fe5-112">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a><span data-ttu-id="f7fe5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7fe5-113">Requirements</span></span>



| <span data-ttu-id="f7fe5-114">需求</span><span class="sxs-lookup"><span data-stu-id="f7fe5-114">Requirement</span></span> | <span data-ttu-id="f7fe5-115">值</span><span class="sxs-lookup"><span data-stu-id="f7fe5-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f7fe5-116">版本</span><span class="sxs-lookup"><span data-stu-id="f7fe5-116">Version</span></span><br/> | <span data-ttu-id="f7fe5-117">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f7fe5-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f7fe5-118">DLL</span><span class="sxs-lookup"><span data-stu-id="f7fe5-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="f7fe5-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7fe5-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7fe5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7fe5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7fe5-121">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="f7fe5-121">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





