---
description: 下列常數形成一組有效的 Windows 映像取得 (WIA) 硬體裝置命令。
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: 'WIA 裝置命令 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848065"
---
# <a name="wia-device-commands"></a><span data-ttu-id="b0f10-103">WIA 裝置命令</span><span class="sxs-lookup"><span data-stu-id="b0f10-103">WIA Device Commands</span></span>

<span data-ttu-id="b0f10-104">下列常數形成一組有效的 Windows 映像取得 (WIA) 硬體裝置命令。</span><span class="sxs-lookup"><span data-stu-id="b0f10-104">The following constants form the set of valid Windows Image Acquisition (WIA) hardware device commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b0f10-105">常數</span><span class="sxs-lookup"><span data-stu-id="b0f10-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b0f10-106">描述</span><span class="sxs-lookup"><span data-stu-id="b0f10-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <span data-ttu-id="b0f10-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0f10-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0f10-108">使裝置的迷你驅動程式與硬體裝置同步處理快取的專案。</span><span class="sxs-lookup"><span data-stu-id="b0f10-108">Causes the device's minidriver to synchronize cached items with the hardware device.</span></span> <span data-ttu-id="b0f10-109">如果裝置支援 <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem：： AnalyzeItem</strong></a> 方法，發出此命令會導致迷你驅動程式捨棄分析結果，並將專案重設為其初始狀態。</span><span class="sxs-lookup"><span data-stu-id="b0f10-109">If the device supports the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem::AnalyzeItem</strong></a> method, issuing this command causes the minidriver to discard the analysis results and reset the item to its initial state.</span></span> <span data-ttu-id="b0f10-110">所有驅動程式都必須支援此命令。</span><span class="sxs-lookup"><span data-stu-id="b0f10-110">All drivers must support this command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <span data-ttu-id="b0f10-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0f10-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0f10-112">導致 WIA 裝置取得映射。</span><span class="sxs-lookup"><span data-stu-id="b0f10-112">Causes a WIA device to acquire an image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <span data-ttu-id="b0f10-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0f10-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0f10-114">告知裝置刪除所有可從代表裝置之 <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> 物件的樹狀結構中刪除的專案。</span><span class="sxs-lookup"><span data-stu-id="b0f10-114">Tells the device to delete all items that can be deleted from the tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> objects that represent the device.</span></span> <span data-ttu-id="b0f10-115">藉由設定專案的屬性，即可防止刪除專案。</span><span class="sxs-lookup"><span data-stu-id="b0f10-115">Item deletion is prevented by setting the item's properties.</span></span> <span data-ttu-id="b0f10-116">如需詳細資訊，請參閱 <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage：： SetPropertyStream</strong></a> 和 <a href="-wia-property-attributes.md">屬性屬性</a>。</span><span class="sxs-lookup"><span data-stu-id="b0f10-116">For details, see <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage::SetPropertyStream</strong></a> and <a href="-wia-property-attributes.md">Property Attributes</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <span data-ttu-id="b0f10-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0f10-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0f10-118">用於檔掃描器。</span><span class="sxs-lookup"><span data-stu-id="b0f10-118">Used for document scanners.</span></span> <span data-ttu-id="b0f10-119">使掃描器在其檔處理常式中載入下一個頁面。</span><span class="sxs-lookup"><span data-stu-id="b0f10-119">Causes the scanner to load the next page in its document handler.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <span data-ttu-id="b0f10-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0f10-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0f10-121">用於檔掃描器。</span><span class="sxs-lookup"><span data-stu-id="b0f10-121">Used for document scanners.</span></span> <span data-ttu-id="b0f10-122">告知裝置卸載其檔處理常式中所有剩餘的頁面。</span><span class="sxs-lookup"><span data-stu-id="b0f10-122">Tells the device to unload all remaining pages in its document handler.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <span data-ttu-id="b0f10-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0f10-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0f10-124">用於具有頁面送紙器的檔掃描器。</span><span class="sxs-lookup"><span data-stu-id="b0f10-124">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="b0f10-125">告知裝置啟動送紙器馬達。</span><span class="sxs-lookup"><span data-stu-id="b0f10-125">Tells the device to start the feeder motor.</span></span> <span data-ttu-id="b0f10-126">從 Windows 8 開始，可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="b0f10-126">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b0f10-127">當<a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a>屬性不受支援，或設定為 WIA_FEEDER_CONTROL_AUTO 時，WIA 迷你驅動程式必須拒絕這個命令，並傳回<strong>WIA_ERROR_INVALID_COMMAND</strong> 。</span><span class="sxs-lookup"><span data-stu-id="b0f10-127">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <span data-ttu-id="b0f10-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0f10-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0f10-129">用於具有頁面送紙器的檔掃描器。</span><span class="sxs-lookup"><span data-stu-id="b0f10-129">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="b0f10-130">告知裝置停止送紙器馬達。</span><span class="sxs-lookup"><span data-stu-id="b0f10-130">Tells the device to stop the feeder motor.</span></span> <span data-ttu-id="b0f10-131">從 Windows 8 開始，可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="b0f10-131">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b0f10-132">當<strong>WIA_IPS_FEEDER_CONTROL</strong>屬性不受支援，或設定為 WIA_FEEDER_CONTROL_AUTO 時，WIA 迷你驅動程式必須拒絕這個命令，並傳回<strong>WIA_ERROR_INVALID_COMMAND</strong> 。</span><span class="sxs-lookup"><span data-stu-id="b0f10-132">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <span data-ttu-id="b0f10-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b0f10-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b0f10-134">用於具有頁面送紙器的檔掃描器。</span><span class="sxs-lookup"><span data-stu-id="b0f10-134">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="b0f10-135">告知裝置暫停送紙器馬達。</span><span class="sxs-lookup"><span data-stu-id="b0f10-135">Tells the device to pause the feeder motor.</span></span> <span data-ttu-id="b0f10-136">從 Windows 8 開始，可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="b0f10-136">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b0f10-137">當<strong>WIA_IPS_FEEDER_CONTROL</strong>屬性不受支援，或設定為 WIA_FEEDER_CONTROL_AUTO 時，WIA 迷你驅動程式必須拒絕這個命令，並傳回<strong>WIA_ERROR_INVALID_COMMAND</strong> 。</span><span class="sxs-lookup"><span data-stu-id="b0f10-137">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="b0f10-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0f10-138">Requirements</span></span>



| <span data-ttu-id="b0f10-139">需求</span><span class="sxs-lookup"><span data-stu-id="b0f10-139">Requirement</span></span> | <span data-ttu-id="b0f10-140">值</span><span class="sxs-lookup"><span data-stu-id="b0f10-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f10-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0f10-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b0f10-142">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0f10-142">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b0f10-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0f10-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b0f10-144">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0f10-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b0f10-145">標頭</span><span class="sxs-lookup"><span data-stu-id="b0f10-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0f10-146"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0f10-146"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
