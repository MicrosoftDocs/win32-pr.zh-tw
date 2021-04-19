---
description: Init 方法會初始化物件。
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: 'CSeekingPassThru.Init 方法 (Seekpt .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982506"
---
# <a name="cseekingpassthruinit-method"></a><span data-ttu-id="30b4f-103">CSeekingPassThru.Init 方法</span><span class="sxs-lookup"><span data-stu-id="30b4f-103">CSeekingPassThru.Init method</span></span>

<span data-ttu-id="30b4f-104">`Init`方法會初始化物件。</span><span class="sxs-lookup"><span data-stu-id="30b4f-104">The `Init` method initializes the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b4f-105">語法</span><span class="sxs-lookup"><span data-stu-id="30b4f-105">Syntax</span></span>


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="30b4f-106">參數</span><span class="sxs-lookup"><span data-stu-id="30b4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30b4f-107">*bSupportRendering* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30b4f-107">*bSupportRendering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b4f-108">指定篩選是否為轉譯器的布林值。</span><span class="sxs-lookup"><span data-stu-id="30b4f-108">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="30b4f-109">如果篩選器是轉譯器，請使用 **TRUE** 值，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="30b4f-109">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="30b4f-110">*pPin*</span><span class="sxs-lookup"><span data-stu-id="30b4f-110">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="30b4f-111">篩選器輸入釘選上 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="30b4f-111">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30b4f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="30b4f-112">Return value</span></span>

<span data-ttu-id="30b4f-113">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="30b4f-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="30b4f-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="30b4f-114">Return code</span></span>                                                                                   | <span data-ttu-id="30b4f-115">Description</span><span class="sxs-lookup"><span data-stu-id="30b4f-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="30b4f-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="30b4f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="30b4f-117">成功。</span><span class="sxs-lookup"><span data-stu-id="30b4f-117">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="30b4f-118"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="30b4f-118"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="30b4f-119">物件已初始化。</span><span class="sxs-lookup"><span data-stu-id="30b4f-119">Object was already initialized.</span></span><br/>         |
| <dl> <span data-ttu-id="30b4f-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="30b4f-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="30b4f-121">記憶體不足，無法建立物件。</span><span class="sxs-lookup"><span data-stu-id="30b4f-121">Not enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="30b4f-122">備註</span><span class="sxs-lookup"><span data-stu-id="30b4f-122">Remarks</span></span>

<span data-ttu-id="30b4f-123">如果 *bSupportRendering* 的值為 **TRUE**，這個方法會建立 [**CRendererPosPassThru**](crendererpospassthru.md) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="30b4f-123">If the value of *bSupportRendering* is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="30b4f-124">否則，它會建立 [**CPosPassThru**](cpospassthru.md) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="30b4f-124">Otherwise, it creates an instance of the [**CPosPassThru**](cpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="30b4f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="30b4f-125">Requirements</span></span>



| <span data-ttu-id="30b4f-126">需求</span><span class="sxs-lookup"><span data-stu-id="30b4f-126">Requirement</span></span> | <span data-ttu-id="30b4f-127">值</span><span class="sxs-lookup"><span data-stu-id="30b4f-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b4f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="30b4f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="30b4f-129"><dt>Seekpt (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="30b4f-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="30b4f-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="30b4f-130">Library</span></span><br/> | <dl> <span data-ttu-id="30b4f-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="30b4f-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b4f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30b4f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b4f-133">**CSeekingPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="30b4f-133">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




