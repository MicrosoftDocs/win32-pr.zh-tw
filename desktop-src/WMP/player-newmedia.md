---
title: NewMedia 方法
description: NewMedia 方法會建立新的媒體物件。
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- newMedia 方法 Windows Media Player
- newMedia 方法 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，newMedia 方法
topic_type:
- apiref
api_name:
- Player.newMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaafb97f836135aa9dd112372b1931c8561cb40b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984835"
---
# <a name="playernewmedia-method"></a><span data-ttu-id="d220e-106">NewMedia 方法</span><span class="sxs-lookup"><span data-stu-id="d220e-106">Player.newMedia method</span></span>

<span data-ttu-id="d220e-107">**NewMedia** 方法會建立新的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="d220e-107">The **newMedia** method creates a new **Media** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d220e-108">語法</span><span class="sxs-lookup"><span data-stu-id="d220e-108">Syntax</span></span>


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="d220e-109">參數</span><span class="sxs-lookup"><span data-stu-id="d220e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d220e-110">*URL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d220e-110">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d220e-111">**字串** ，包含要用來建立 **媒體** 物件之數位媒體檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="d220e-111">**String** containing the URL of the digital media file to create the **Media** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d220e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d220e-112">Return value</span></span>

<span data-ttu-id="d220e-113">這個方法會傳回 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="d220e-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d220e-114">備註</span><span class="sxs-lookup"><span data-stu-id="d220e-114">Remarks</span></span>

<span data-ttu-id="d220e-115">*URL* 參數不得為空字串或 null。</span><span class="sxs-lookup"><span data-stu-id="d220e-115">The *URL* parameter must not be an empty string or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="d220e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d220e-116">Requirements</span></span>



| <span data-ttu-id="d220e-117">需求</span><span class="sxs-lookup"><span data-stu-id="d220e-117">Requirement</span></span> | <span data-ttu-id="d220e-118">值</span><span class="sxs-lookup"><span data-stu-id="d220e-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d220e-119">版本</span><span class="sxs-lookup"><span data-stu-id="d220e-119">Version</span></span><br/> | <span data-ttu-id="d220e-120">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="d220e-120">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="d220e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d220e-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="d220e-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d220e-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d220e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d220e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d220e-124">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="d220e-124">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





