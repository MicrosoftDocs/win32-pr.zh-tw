---
description: 由 Shell 所執行，以協助編寫腳本和 Microsoft Visual Basic 開發人員使用 Shell 中提供的一些功能。 ShellUIHelper 物件沒有任何屬性或事件。 提供方法以將專案新增至 Shell。
title: 'ShellUIHelper 物件 (Exdisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: b77d618c4c772859a9009f3cca761c59df83257a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842429"
---
# <a name="shelluihelper-object"></a><span data-ttu-id="9951b-105">ShellUIHelper 物件</span><span class="sxs-lookup"><span data-stu-id="9951b-105">ShellUIHelper object</span></span>

<span data-ttu-id="9951b-106">由 Shell 所執行，以協助編寫腳本和 Microsoft Visual Basic 開發人員使用 Shell 中提供的一些功能。</span><span class="sxs-lookup"><span data-stu-id="9951b-106">Implemented by the Shell to help script and Microsoft Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="9951b-107">**ShellUIHelper** 物件沒有任何屬性或事件。</span><span class="sxs-lookup"><span data-stu-id="9951b-107">The **ShellUIHelper** object does not have any properties or events.</span></span> <span data-ttu-id="9951b-108">提供方法以將專案新增至 Shell。</span><span class="sxs-lookup"><span data-stu-id="9951b-108">Methods are provided to add items to the Shell.</span></span>

## <a name="members"></a><span data-ttu-id="9951b-109">成員</span><span class="sxs-lookup"><span data-stu-id="9951b-109">Members</span></span>

<span data-ttu-id="9951b-110">**ShellUIHelper** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9951b-110">The **ShellUIHelper** object has these types of members:</span></span>

-   [<span data-ttu-id="9951b-111">方法</span><span class="sxs-lookup"><span data-stu-id="9951b-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9951b-112">方法</span><span class="sxs-lookup"><span data-stu-id="9951b-112">Methods</span></span>

<span data-ttu-id="9951b-113">**ShellUIHelper** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9951b-113">The **ShellUIHelper** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="9951b-114">方法</span><span class="sxs-lookup"><span data-stu-id="9951b-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="9951b-115">描述</span><span class="sxs-lookup"><span data-stu-id="9951b-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="9951b-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span><span class="sxs-lookup"><span data-stu-id="9951b-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="9951b-117">將新通道新增至 [我 Internet Explorer 的最愛 <strong>]</strong> 功能表中的通道清單和桌面上的 <strong>頻道</strong> 列。</span><span class="sxs-lookup"><span data-stu-id="9951b-117">Adds a new channel to the list of channels in the Internet Explorer <strong>Favorites</strong> menu and to the <strong>Channel</strong> bar on the desktop.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9951b-118">Windows Vista 下已不再支援此方法。</span><span class="sxs-lookup"><span data-stu-id="9951b-118">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="9951b-119">在該作業系統下，它會傳回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="9951b-119">Under that operating system, it returns E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="9951b-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="9951b-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="9951b-121">將專案加入至 Active Desktop。</span><span class="sxs-lookup"><span data-stu-id="9951b-121">Adds an item to the Active Desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="9951b-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span><span class="sxs-lookup"><span data-stu-id="9951b-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="9951b-123">顯示用來建立我的最愛專案的預設使用者介面。</span><span class="sxs-lookup"><span data-stu-id="9951b-123">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="9951b-124">使用者介面會初始化為指定的參數。</span><span class="sxs-lookup"><span data-stu-id="9951b-124">The user interface is initialized to the specified parameters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="9951b-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span><span class="sxs-lookup"><span data-stu-id="9951b-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="9951b-126">指出是否已訂閱指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="9951b-126">Indicates whether a specified URL is subscribed to.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9951b-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="9951b-127">Requirements</span></span>



| <span data-ttu-id="9951b-128">需求</span><span class="sxs-lookup"><span data-stu-id="9951b-128">Requirement</span></span> | <span data-ttu-id="9951b-129">值</span><span class="sxs-lookup"><span data-stu-id="9951b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9951b-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9951b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9951b-131">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9951b-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9951b-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9951b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9951b-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9951b-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9951b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="9951b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9951b-135"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9951b-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="9951b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9951b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9951b-137"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="9951b-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




