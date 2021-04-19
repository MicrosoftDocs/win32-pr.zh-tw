---
title: 設定。餘額
description: '[餘額] 屬性會指定或抓取目前的立體餘額。'
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- 設定。餘額 Windows Media Player
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982522"
---
# <a name="settingsbalance"></a><span data-ttu-id="e9b07-104">設定。餘額</span><span class="sxs-lookup"><span data-stu-id="e9b07-104">Settings.balance</span></span>

<span data-ttu-id="e9b07-105">[ **餘額** ] 屬性會指定或抓取目前的立體餘額。</span><span class="sxs-lookup"><span data-stu-id="e9b07-105">The **balance** property specifies or retrieves the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b07-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9b07-106">Syntax</span></span>

<span data-ttu-id="e9b07-107">播放機. 設定。餘額</span><span class="sxs-lookup"><span data-stu-id="e9b07-107">player.settings.balance</span></span>

## <a name="possible-values"></a><span data-ttu-id="e9b07-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="e9b07-108">Possible Values</span></span>

<span data-ttu-id="e9b07-109">這個屬性是 (**長**) 的讀取/寫入 **號碼**。</span><span class="sxs-lookup"><span data-stu-id="e9b07-109">This property is a read/write **Number** (**long**).</span></span> <span data-ttu-id="e9b07-110">值的範圍是從100到100，預設值為零。</span><span class="sxs-lookup"><span data-stu-id="e9b07-110">Values range from  100 to 100, with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9b07-111">備註</span><span class="sxs-lookup"><span data-stu-id="e9b07-111">Remarks</span></span>

<span data-ttu-id="e9b07-112">值為零表示音訊在左右通道的相同磁片區上播放。</span><span class="sxs-lookup"><span data-stu-id="e9b07-112">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="e9b07-113">值為100表示音訊只會在左邊的頻道播放。</span><span class="sxs-lookup"><span data-stu-id="e9b07-113">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="e9b07-114">值為100表示音訊只會在右聲道上播放。</span><span class="sxs-lookup"><span data-stu-id="e9b07-114">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9b07-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9b07-115">Requirements</span></span>



| <span data-ttu-id="e9b07-116">需求</span><span class="sxs-lookup"><span data-stu-id="e9b07-116">Requirement</span></span> | <span data-ttu-id="e9b07-117">值</span><span class="sxs-lookup"><span data-stu-id="e9b07-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b07-118">版本</span><span class="sxs-lookup"><span data-stu-id="e9b07-118">Version</span></span><br/> | <span data-ttu-id="e9b07-119">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e9b07-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e9b07-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e9b07-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="e9b07-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9b07-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9b07-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9b07-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b07-123">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="e9b07-123">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





