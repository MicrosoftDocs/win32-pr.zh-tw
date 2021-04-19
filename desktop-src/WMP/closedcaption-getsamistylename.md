---
title: ClosedCaption. getSAMIStyleName 方法
description: GetSAMIStyleName 方法會抓取目前的薩米文檔案所支援的樣式名稱。
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- getSAMIStyleName 方法 Windows Media Player
- getSAMIStyleName 方法 Windows Media Player，ClosedCaption 類別
- ClosedCaption 類別 Windows Media Player，getSAMIStyleName 方法
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977477"
---
# <a name="closedcaptiongetsamistylename-method"></a><span data-ttu-id="0de2b-106">ClosedCaption. getSAMIStyleName 方法</span><span class="sxs-lookup"><span data-stu-id="0de2b-106">ClosedCaption.getSAMIStyleName method</span></span>

<span data-ttu-id="0de2b-107">**GetSAMIStyleName** 方法會抓取目前的薩米文檔案所支援的樣式名稱。</span><span class="sxs-lookup"><span data-stu-id="0de2b-107">The **getSAMIStyleName** method retrieves the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de2b-108">語法</span><span class="sxs-lookup"><span data-stu-id="0de2b-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="0de2b-109">參數</span><span class="sxs-lookup"><span data-stu-id="0de2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0de2b-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0de2b-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0de2b-111">**數值** (**long**) 指定要抓取之樣式名稱的索引。</span><span class="sxs-lookup"><span data-stu-id="0de2b-111">**Number** (**long**) specifying the index of the style name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0de2b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0de2b-112">Return value</span></span>

<span data-ttu-id="0de2b-113">這個方法會傳回 **字串** ，其中包含以薩米文檔案指定的樣式名稱。</span><span class="sxs-lookup"><span data-stu-id="0de2b-113">This method returns a **String** containing the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="0de2b-114">備註</span><span class="sxs-lookup"><span data-stu-id="0de2b-114">Remarks</span></span>

<span data-ttu-id="0de2b-115">薩米文檔案中的樣式會依照檔案中顯示的順序編制索引，從零開始。</span><span class="sxs-lookup"><span data-stu-id="0de2b-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="0de2b-116">在 (*播放機* 開啟數位媒體檔案之前，無法使用此方法。**openState** 等於13個) 。</span><span class="sxs-lookup"><span data-stu-id="0de2b-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="0de2b-117">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0de2b-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0de2b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0de2b-118">Requirements</span></span>



| <span data-ttu-id="0de2b-119">需求</span><span class="sxs-lookup"><span data-stu-id="0de2b-119">Requirement</span></span> | <span data-ttu-id="0de2b-120">值</span><span class="sxs-lookup"><span data-stu-id="0de2b-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0de2b-121">版本</span><span class="sxs-lookup"><span data-stu-id="0de2b-121">Version</span></span><br/> | <span data-ttu-id="0de2b-122">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="0de2b-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0de2b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0de2b-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0de2b-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0de2b-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0de2b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0de2b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0de2b-126">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="0de2b-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="0de2b-127">**ClosedCaption 物件**</span><span class="sxs-lookup"><span data-stu-id="0de2b-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="0de2b-128">**ClosedCaption.SAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="0de2b-128">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





