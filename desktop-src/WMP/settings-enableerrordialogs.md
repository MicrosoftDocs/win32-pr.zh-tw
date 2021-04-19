---
title: 設定. enableErrorDialogs
description: EnableErrorDialogs 屬性會指定或抓取值，指出是否會自動顯示錯誤對話方塊。
ms.assetid: 16b10bea-4b3e-469f-a903-02f19ffcdf31
keywords:
- 設定. enableErrorDialogs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.enableErrorDialogs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5746bb68da71ca827da3923e4956b613eabdb50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990033"
---
# <a name="settingsenableerrordialogs"></a><span data-ttu-id="822ee-104">設定. enableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="822ee-104">Settings.enableErrorDialogs</span></span>

<span data-ttu-id="822ee-105">**EnableErrorDialogs** 屬性會指定或抓取值，指出是否會自動顯示錯誤對話方塊。</span><span class="sxs-lookup"><span data-stu-id="822ee-105">The **enableErrorDialogs** property specifies or retrieves a value indicating whether error dialog boxes are shown automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="822ee-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="822ee-106">Syntax</span></span>

<span data-ttu-id="822ee-107">enableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="822ee-107">player.settings.enableErrorDialogs</span></span>

## <a name="possible-values"></a><span data-ttu-id="822ee-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="822ee-108">Possible Values</span></span>

<span data-ttu-id="822ee-109">這個屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="822ee-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="822ee-110">值</span><span class="sxs-lookup"><span data-stu-id="822ee-110">Value</span></span> | <span data-ttu-id="822ee-111">描述</span><span class="sxs-lookup"><span data-stu-id="822ee-111">Description</span></span>                                     |
|-------|-------------------------------------------------|
| <span data-ttu-id="822ee-112">true</span><span class="sxs-lookup"><span data-stu-id="822ee-112">true</span></span>  | <span data-ttu-id="822ee-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="822ee-113">Default.</span></span> <span data-ttu-id="822ee-114">錯誤對話方塊會自動顯示。</span><span class="sxs-lookup"><span data-stu-id="822ee-114">Error dialogs are shown automatically.</span></span> |
| <span data-ttu-id="822ee-115">false</span><span class="sxs-lookup"><span data-stu-id="822ee-115">false</span></span> | <span data-ttu-id="822ee-116">錯誤對話方塊不會自動顯示。</span><span class="sxs-lookup"><span data-stu-id="822ee-116">Error dialogs are not shown automatically.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="822ee-117">備註</span><span class="sxs-lookup"><span data-stu-id="822ee-117">Remarks</span></span>

<span data-ttu-id="822ee-118">這個屬性會展示播放程式控制項之遠端實例的特定行為。</span><span class="sxs-lookup"><span data-stu-id="822ee-118">This property exhibits specific behavior for remoted instances of the Player control.</span></span> <span data-ttu-id="822ee-119">如需詳細資訊，請參閱 [遠端處理 Windows Media Player 控制項](remoting-the-windows-media-player-control.md)。</span><span class="sxs-lookup"><span data-stu-id="822ee-119">For more information, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="822ee-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="822ee-120">Requirements</span></span>



| <span data-ttu-id="822ee-121">需求</span><span class="sxs-lookup"><span data-stu-id="822ee-121">Requirement</span></span> | <span data-ttu-id="822ee-122">值</span><span class="sxs-lookup"><span data-stu-id="822ee-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="822ee-123">版本</span><span class="sxs-lookup"><span data-stu-id="822ee-123">Version</span></span><br/> | <span data-ttu-id="822ee-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="822ee-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="822ee-125">DLL</span><span class="sxs-lookup"><span data-stu-id="822ee-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="822ee-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="822ee-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="822ee-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="822ee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="822ee-128">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="822ee-128">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





