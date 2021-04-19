---
title: ClosedCaption. getSAMILangName 方法
description: GetSAMILangName 方法會抓取目前的薩米文檔案所支援的語言名稱。
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- getSAMILangName 方法 Windows Media Player
- getSAMILangName 方法 Windows Media Player，ClosedCaption 類別
- ClosedCaption 類別 Windows Media Player，getSAMILangName 方法
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd4b481de808ac8814e596cfc038aec38c7f19b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984105"
---
# <a name="closedcaptiongetsamilangname-method"></a><span data-ttu-id="4eb9d-106">ClosedCaption. getSAMILangName 方法</span><span class="sxs-lookup"><span data-stu-id="4eb9d-106">ClosedCaption.getSAMILangName method</span></span>

<span data-ttu-id="4eb9d-107">**GetSAMILangName** 方法會抓取目前的薩米文檔案所支援的語言名稱。</span><span class="sxs-lookup"><span data-stu-id="4eb9d-107">The **getSAMILangName** method retrieves the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb9d-108">語法</span><span class="sxs-lookup"><span data-stu-id="4eb9d-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="4eb9d-109">參數</span><span class="sxs-lookup"><span data-stu-id="4eb9d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb9d-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4eb9d-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb9d-111">**(** **long**) 指定要取出之語言名稱的索引。</span><span class="sxs-lookup"><span data-stu-id="4eb9d-111">**Number** (**long**) specifying the index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eb9d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4eb9d-112">Return value</span></span>

<span data-ttu-id="4eb9d-113">這個方法會傳回 **字串** ，其中包含以薩米文檔案指定的語言名稱。</span><span class="sxs-lookup"><span data-stu-id="4eb9d-113">This method returns a **String** containing the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb9d-114">備註</span><span class="sxs-lookup"><span data-stu-id="4eb9d-114">Remarks</span></span>

<span data-ttu-id="4eb9d-115">薩米文檔案中的語言會依照檔案中顯示的順序編制索引，從零開始。</span><span class="sxs-lookup"><span data-stu-id="4eb9d-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="4eb9d-116">在 (*播放機* 開啟數位媒體檔案之前，無法使用此方法。**openState** 等於13個) 。</span><span class="sxs-lookup"><span data-stu-id="4eb9d-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="4eb9d-117">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="4eb9d-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb9d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4eb9d-118">Requirements</span></span>



| <span data-ttu-id="4eb9d-119">需求</span><span class="sxs-lookup"><span data-stu-id="4eb9d-119">Requirement</span></span> | <span data-ttu-id="4eb9d-120">值</span><span class="sxs-lookup"><span data-stu-id="4eb9d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb9d-121">版本</span><span class="sxs-lookup"><span data-stu-id="4eb9d-121">Version</span></span><br/> | <span data-ttu-id="4eb9d-122">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="4eb9d-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="4eb9d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4eb9d-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="4eb9d-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4eb9d-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb9d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4eb9d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb9d-126">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="4eb9d-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="4eb9d-127">**ClosedCaption 物件**</span><span class="sxs-lookup"><span data-stu-id="4eb9d-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="4eb9d-128">**ClosedCaption.SAMILang**</span><span class="sxs-lookup"><span data-stu-id="4eb9d-128">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





