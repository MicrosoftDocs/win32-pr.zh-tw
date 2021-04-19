---
title: ShowPopup 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |ShowPopup 方法
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- showPopup 方法 Windows Media Player
- showPopup 方法 Windows Media Player、External 類別
- External class Windows Media Player，showPopup 方法
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976004"
---
# <a name="externalshowpopup-method"></a><span data-ttu-id="adf1d-107">ShowPopup 方法</span><span class="sxs-lookup"><span data-stu-id="adf1d-107">External.showPopup method</span></span>

> [!Note]  
> <span data-ttu-id="adf1d-108">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="adf1d-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="adf1d-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="adf1d-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="adf1d-110">**ShowPopup** 方法會指示 Windows Media Player 顯示快捷方式網頁;也就是在另一個視窗中出現的網頁。</span><span class="sxs-lookup"><span data-stu-id="adf1d-110">The **showPopup** method instructs Windows Media Player to display a pop-up webpage; that is, a webpage that appears in a separate window.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf1d-111">語法</span><span class="sxs-lookup"><span data-stu-id="adf1d-111">Syntax</span></span>


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a><span data-ttu-id="adf1d-112">參數</span><span class="sxs-lookup"><span data-stu-id="adf1d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf1d-113">*PopupIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adf1d-113">*PopupIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf1d-114">指定快顯網頁索引的 (**long**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="adf1d-114">**Number** (**long**) that specifies the index of the pop-up webpage.</span></span>

</dd> <dt>

<span data-ttu-id="adf1d-115">*參數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adf1d-115">*Parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf1d-116">Windows Media Player 附加至網頁 URL 的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="adf1d-116">**String** that Windows Media Player appends to the URL of the webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf1d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="adf1d-117">Return value</span></span>

<span data-ttu-id="adf1d-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="adf1d-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="adf1d-119">備註</span><span class="sxs-lookup"><span data-stu-id="adf1d-119">Remarks</span></span>

<span data-ttu-id="adf1d-120">Windows Media Player 不會解讀快顯索引。</span><span class="sxs-lookup"><span data-stu-id="adf1d-120">The pop-up index is not interpreted by Windows Media Player.</span></span> <span data-ttu-id="adf1d-121">識別快顯視窗的索引是由線上商店所建立，而且只有線上商店才有意義。</span><span class="sxs-lookup"><span data-stu-id="adf1d-121">Indexes that identify pop-up webpages are created by the online store, and have meaning only to the online store.</span></span>

<span data-ttu-id="adf1d-122">下列步驟顯示 Windows Media Player 如何使用 **showPopup** 方法的參數來建立快顯視窗的 URL。</span><span class="sxs-lookup"><span data-stu-id="adf1d-122">The following steps show how Windows Media Player uses the parameters of the **showPopup** method to create a URL for the popup window.</span></span>

1.  <span data-ttu-id="adf1d-123">探索頁面上的腳本會呼叫 **showPopup**，並傳遞 *PopupIndex* 中的整數和 *參數* 中的字串。</span><span class="sxs-lookup"><span data-stu-id="adf1d-123">Script on a discovery page calls **showPopup**, passing an integer in *PopupIndex* and a string in *Parameters*.</span></span>

2.  <span data-ttu-id="adf1d-124">Windows Media Player 將索引傳遞給 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) ，以抓取要顯示之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="adf1d-124">Windows Media Player passes the index to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to retrieve the URL of the webpage to be displayed.</span></span>

3.  <span data-ttu-id="adf1d-125">Windows Media Player 會將 *參數* 以查詢字串的形式附加至 URL。</span><span class="sxs-lookup"><span data-stu-id="adf1d-125">Windows Media Player appends *Parameters* to the URL as a query string.</span></span> <span data-ttu-id="adf1d-126">例如，如果 **GetItemInfo** 傳回 " https://www.Proseware.com/Pages/Popup1.htm "，且 *參數* 等於 "DlgX = 800&DlgY = 400&問候語 = Hi"，Windows Media Player 會建立下列 URL：</span><span class="sxs-lookup"><span data-stu-id="adf1d-126">For example, if **GetItemInfo** returns "https://www.Proseware.com/Pages/Popup1.htm" and *Parameters* is equal to "DlgX=800&DlgY=400&Greeting=Hi", Windows Media Player creates the following URL:</span></span>

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

<span data-ttu-id="adf1d-127">您可以使用 *參數* 來指定快顯視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="adf1d-127">You can use *Parameters* to specify the size of the pop-up window.</span></span> <span data-ttu-id="adf1d-128">例如，如果您將 *參數* 設定為 "DlgX = 800&DlgY = 400"，快顯視窗的大小會是800圖元乘以400圖元。</span><span class="sxs-lookup"><span data-stu-id="adf1d-128">For example, if you set *Parameters* to "DlgX=800&DlgY=400", the pop-up window will have a size of 800 pixels by 400 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="adf1d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="adf1d-129">Requirements</span></span>



| <span data-ttu-id="adf1d-130">需求</span><span class="sxs-lookup"><span data-stu-id="adf1d-130">Requirement</span></span> | <span data-ttu-id="adf1d-131">值</span><span class="sxs-lookup"><span data-stu-id="adf1d-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="adf1d-132">版本</span><span class="sxs-lookup"><span data-stu-id="adf1d-132">Version</span></span><br/> | <span data-ttu-id="adf1d-133">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="adf1d-133">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="adf1d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="adf1d-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="adf1d-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adf1d-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adf1d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adf1d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf1d-137">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="adf1d-137">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





