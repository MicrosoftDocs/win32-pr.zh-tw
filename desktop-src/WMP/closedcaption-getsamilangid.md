---
title: ClosedCaption. getSAMILangID 方法
description: GetSAMILangID 方法會抓取目前薩米文檔案所支援之語言 (LCID) 的地區設定識別碼。
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- getSAMILangID 方法 Windows Media Player
- getSAMILangID 方法 Windows Media Player，ClosedCaption 類別
- ClosedCaption 類別 Windows Media Player，getSAMILangID 方法
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991051"
---
# <a name="closedcaptiongetsamilangid-method"></a><span data-ttu-id="326ae-106">ClosedCaption. getSAMILangID 方法</span><span class="sxs-lookup"><span data-stu-id="326ae-106">ClosedCaption.getSAMILangID method</span></span>

<span data-ttu-id="326ae-107">**GetSAMILangID** 方法會抓取目前薩米文檔案所支援之語言 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="326ae-107">The **getSAMILangID** method retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="326ae-108">語法</span><span class="sxs-lookup"><span data-stu-id="326ae-108">Syntax</span></span>


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="326ae-109">參數</span><span class="sxs-lookup"><span data-stu-id="326ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="326ae-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="326ae-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="326ae-111">**數值** (**long**) 指定要抓取之 LCID 的索引。</span><span class="sxs-lookup"><span data-stu-id="326ae-111">**Number** (**long**) specifying the index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="326ae-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="326ae-112">Return value</span></span>

<span data-ttu-id="326ae-113">這個方法會傳回 **數位** (**Long**) ，其中包含具有指定索引之語言的 LCID。</span><span class="sxs-lookup"><span data-stu-id="326ae-113">This method returns a **Number** (**long**) containing the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="326ae-114">備註</span><span class="sxs-lookup"><span data-stu-id="326ae-114">Remarks</span></span>

<span data-ttu-id="326ae-115">薩米文檔案中的語言會依照檔案中顯示的順序編制索引，從零開始。</span><span class="sxs-lookup"><span data-stu-id="326ae-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="326ae-116">在 (*播放機* 開啟數位媒體檔案之前，無法使用此方法。**openState** 等於13個) 。</span><span class="sxs-lookup"><span data-stu-id="326ae-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="326ae-117">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="326ae-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="326ae-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="326ae-118">Requirements</span></span>



| <span data-ttu-id="326ae-119">需求</span><span class="sxs-lookup"><span data-stu-id="326ae-119">Requirement</span></span> | <span data-ttu-id="326ae-120">值</span><span class="sxs-lookup"><span data-stu-id="326ae-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="326ae-121">版本</span><span class="sxs-lookup"><span data-stu-id="326ae-121">Version</span></span><br/> | <span data-ttu-id="326ae-122">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="326ae-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="326ae-123">DLL</span><span class="sxs-lookup"><span data-stu-id="326ae-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="326ae-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="326ae-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="326ae-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="326ae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="326ae-126">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="326ae-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="326ae-127">**ClosedCaption 物件**</span><span class="sxs-lookup"><span data-stu-id="326ae-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





