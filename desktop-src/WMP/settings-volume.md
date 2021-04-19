---
title: 設定。磁片區
description: Volume 屬性會指定或抓取目前的磁片區。
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- 設定. 磁片區 Windows Media Player
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f5ec4299bf33ed16143eec8570b65c548599e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978686"
---
# <a name="settingsvolume"></a><span data-ttu-id="0a013-104">設定。磁片區</span><span class="sxs-lookup"><span data-stu-id="0a013-104">Settings.volume</span></span>

<span data-ttu-id="0a013-105">**Volume** 屬性會指定或抓取目前的磁片區。</span><span class="sxs-lookup"><span data-stu-id="0a013-105">The **volume** property specifies or retrieves the current volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a013-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a013-106">Syntax</span></span>

<span data-ttu-id="0a013-107">player. 設定磁片區</span><span class="sxs-lookup"><span data-stu-id="0a013-107">player.settings.volume</span></span>

## <a name="possible-values"></a><span data-ttu-id="0a013-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="0a013-108">Possible Values</span></span>

<span data-ttu-id="0a013-109">此屬性是讀取/寫入 **號碼** (**長**) 範圍從0到100。</span><span class="sxs-lookup"><span data-stu-id="0a013-109">This property is a read/write **Number** (**long**) ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a013-110">備註</span><span class="sxs-lookup"><span data-stu-id="0a013-110">Remarks</span></span>

<span data-ttu-id="0a013-111">零未指定磁片區，且100指定完整磁片區。</span><span class="sxs-lookup"><span data-stu-id="0a013-111">Zero specifies no volume and 100 specifies full volume.</span></span> <span data-ttu-id="0a013-112">如果未指定此屬性的值，則會預設為播放程式的最後一個磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="0a013-112">If no value is specified for this property, it defaults to the last volume setting established for the player.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a013-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a013-113">Requirements</span></span>



| <span data-ttu-id="0a013-114">需求</span><span class="sxs-lookup"><span data-stu-id="0a013-114">Requirement</span></span> | <span data-ttu-id="0a013-115">值</span><span class="sxs-lookup"><span data-stu-id="0a013-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a013-116">版本</span><span class="sxs-lookup"><span data-stu-id="0a013-116">Version</span></span><br/> | <span data-ttu-id="0a013-117">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="0a013-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0a013-118">DLL</span><span class="sxs-lookup"><span data-stu-id="0a013-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="0a013-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a013-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a013-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a013-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a013-121">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="0a013-121">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





