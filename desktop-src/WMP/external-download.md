---
title: External. 下載方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 下載方法會啟動一組媒體專案的下載。
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- 下載方法 Windows Media Player
- 下載方法 Windows Media Player，外部類別
- 外部類別 Windows Media Player，下載方法
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995594"
---
# <a name="externaldownload-method"></a><span data-ttu-id="aa1dd-108">External. 下載方法</span><span class="sxs-lookup"><span data-stu-id="aa1dd-108">External.download method</span></span>

> [!Note]  
> <span data-ttu-id="aa1dd-109">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="aa1dd-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="aa1dd-111">**下載** 方法會啟動一組媒體專案的下載。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-111">The **download** method initiates the download of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa1dd-112">語法</span><span class="sxs-lookup"><span data-stu-id="aa1dd-112">Syntax</span></span>


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a><span data-ttu-id="aa1dd-113">參數</span><span class="sxs-lookup"><span data-stu-id="aa1dd-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa1dd-114">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa1dd-114">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa1dd-115">連結 [庫位置常數](library-location-constants.md) ，指定要下載的專案類型。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-115">A [library location constant](library-location-constants.md) that specifies the type of item to be downloaded.</span></span> <span data-ttu-id="aa1dd-116">例如，CPTrackID 指定要下載一或多個曲目。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-116">For example, CPTrackID specifies that one or more tracks are to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="aa1dd-117">*識別碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aa1dd-117">*IDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa1dd-118">**字串** ，包含要下載之媒體專案的識別碼（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-118">**String** containing the IDs, delimited by semicolons, of the media items to be downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa1dd-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa1dd-119">Return value</span></span>

<span data-ttu-id="aa1dd-120">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa1dd-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa1dd-121">Requirements</span></span>



| <span data-ttu-id="aa1dd-122">需求</span><span class="sxs-lookup"><span data-stu-id="aa1dd-122">Requirement</span></span> | <span data-ttu-id="aa1dd-123">值</span><span class="sxs-lookup"><span data-stu-id="aa1dd-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa1dd-124">版本</span><span class="sxs-lookup"><span data-stu-id="aa1dd-124">Version</span></span><br/> | <span data-ttu-id="aa1dd-125">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="aa1dd-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="aa1dd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="aa1dd-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="aa1dd-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa1dd-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa1dd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa1dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa1dd-129">**下載媒體內容**</span><span class="sxs-lookup"><span data-stu-id="aa1dd-129">**Downloading Media Content**</span></span>](downloading-media-content.md)
</dt> <dt>

[<span data-ttu-id="aa1dd-130">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="aa1dd-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="aa1dd-131">**External. 購買**</span><span class="sxs-lookup"><span data-stu-id="aa1dd-131">**External.buy**</span></span>](external-buy.md)
</dt> <dt>

[<span data-ttu-id="aa1dd-132">**IWMPContentPartner：:D 下載 o)**</span><span class="sxs-lookup"><span data-stu-id="aa1dd-132">**IWMPContentPartner::Download**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





