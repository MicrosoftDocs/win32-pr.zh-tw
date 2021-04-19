---
title: GetLanguageName 方法
description: GetLanguageName 方法會使用指定的地區設定識別碼 (LCID) 來抓取音訊語言的名稱。
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- getLanguageName 方法 Windows Media Player
- getLanguageName 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，getLanguageName 方法
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983151"
---
# <a name="controlsgetlanguagename-method"></a><span data-ttu-id="6b9df-106">GetLanguageName 方法</span><span class="sxs-lookup"><span data-stu-id="6b9df-106">Controls.getLanguageName method</span></span>

<span data-ttu-id="6b9df-107">**GetLanguageName** 方法會使用指定的地區設定識別碼 (LCID) 來抓取音訊語言的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b9df-107">The **getLanguageName** method retrieves the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b9df-108">語法</span><span class="sxs-lookup"><span data-stu-id="6b9df-108">Syntax</span></span>


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a><span data-ttu-id="6b9df-109">參數</span><span class="sxs-lookup"><span data-stu-id="6b9df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b9df-110"> \[ 中的 LCID\]</span><span class="sxs-lookup"><span data-stu-id="6b9df-110">*LCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b9df-111">指定 LCID (**long**) 的 **數目**。</span><span class="sxs-lookup"><span data-stu-id="6b9df-111">**Number** (**long**) specifying the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b9df-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b9df-112">Return value</span></span>

<span data-ttu-id="6b9df-113">這個方法會傳回 **字串**。</span><span class="sxs-lookup"><span data-stu-id="6b9df-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b9df-114">備註</span><span class="sxs-lookup"><span data-stu-id="6b9df-114">Remarks</span></span>

<span data-ttu-id="6b9df-115">LCID 可唯一識別特定語言方言，稱為地區設定。</span><span class="sxs-lookup"><span data-stu-id="6b9df-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="6b9df-116">針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="6b9df-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b9df-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b9df-117">Requirements</span></span>



| <span data-ttu-id="6b9df-118">需求</span><span class="sxs-lookup"><span data-stu-id="6b9df-118">Requirement</span></span> | <span data-ttu-id="6b9df-119">值</span><span class="sxs-lookup"><span data-stu-id="6b9df-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b9df-120">版本</span><span class="sxs-lookup"><span data-stu-id="6b9df-120">Version</span></span><br/> | <span data-ttu-id="6b9df-121">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="6b9df-121">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="6b9df-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6b9df-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b9df-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b9df-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b9df-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b9df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b9df-125">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="6b9df-125">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="6b9df-126">**AudioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="6b9df-126">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="6b9df-127">**CurrentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="6b9df-127">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="6b9df-128">**CurrentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="6b9df-128">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="6b9df-129">**GetAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="6b9df-129">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="6b9df-130">**GetAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="6b9df-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





