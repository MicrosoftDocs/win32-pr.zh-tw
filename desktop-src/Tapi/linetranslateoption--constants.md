---
description: LINETRANSLATEOPTION \_ 位旗標常數描述位址轉譯使用的選項。
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: 'LINETRANSLATEOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000790"
---
# <a name="linetranslateoption_-constants"></a><span data-ttu-id="f0abe-103">LINETRANSLATEOPTION \_ 常數</span><span class="sxs-lookup"><span data-stu-id="f0abe-103">LINETRANSLATEOPTION\_ Constants</span></span>

<span data-ttu-id="f0abe-104">**LINETRANSLATEOPTION \_** 位旗標常數描述位址轉譯使用的選項。</span><span class="sxs-lookup"><span data-stu-id="f0abe-104">The **LINETRANSLATEOPTION\_** bit-flag constant describes an option used by address translation.</span></span>

<dl> <dt>

<span data-ttu-id="f0abe-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION \_ CANCELCALLWAITING**</span><span class="sxs-lookup"><span data-stu-id="f0abe-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION\_CANCELCALLWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f0abe-106">如果為位置定義了取消呼叫等候字串，則設定此位將會導致該字串插入可撥出的字串開頭。</span><span class="sxs-lookup"><span data-stu-id="f0abe-106">If a Cancel Call Waiting string is defined for the location, setting this bit will cause that string to be inserted at the beginning of the dialable string.</span></span> <span data-ttu-id="f0abe-107">這通常是由資料數據機和傳真應用程式所使用，以防止呼叫等候嗶聲的電話中斷。</span><span class="sxs-lookup"><span data-stu-id="f0abe-107">This is commonly used by data modem and fax applications to prevent interruption of calls by call waiting beeps.</span></span> <span data-ttu-id="f0abe-108">如果沒有為位置定義取消呼叫等候字串，這個位就不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="f0abe-108">If no Cancel Call Waiting string is defined for the location, this bit has no affect.</span></span> <span data-ttu-id="f0abe-109">請注意，使用此位的應用程式也會 \_ 在 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)結構的 **dwCallParamFlags** 成員中，透過 *lpCallParams* 參數 [**來設定**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)LINECALLPARAMFLAGS 安全位，如此一來，如果線路裝置使用可撥數位以外的機制來隱藏呼叫中斷，則會叫用該機制。</span><span class="sxs-lookup"><span data-stu-id="f0abe-109">Note that applications using this bit are advised to also set the LINECALLPARAMFLAGS\_SECURE bit in the **dwCallParamFlags** member of the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in to [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) through the *lpCallParams* parameter, so that if the line device uses a mechanism other than dialable digits to suppress call interrupts then that mechanism will be invoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0abe-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION \_ CARDOVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="f0abe-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION\_CARDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f0abe-111">預設的電話卡會以指定的電話卡覆寫。</span><span class="sxs-lookup"><span data-stu-id="f0abe-111">The default calling card is to be overridden with a specified one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0abe-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION \_ FORCELD**</span><span class="sxs-lookup"><span data-stu-id="f0abe-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION\_FORCELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f0abe-113">此選項會強制將位址 () 轉譯為長距離。</span><span class="sxs-lookup"><span data-stu-id="f0abe-113">This option forces the address (number) to be translated as long distance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f0abe-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION \_ FORCELOCAL**</span><span class="sxs-lookup"><span data-stu-id="f0abe-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION\_FORCELOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f0abe-115">此選項會強制將 (位址) 的數目轉譯為本機。</span><span class="sxs-lookup"><span data-stu-id="f0abe-115">This option forces the number (address) to be translated as local.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0abe-116">備註</span><span class="sxs-lookup"><span data-stu-id="f0abe-116">Remarks</span></span>

<span data-ttu-id="f0abe-117">無延伸。</span><span class="sxs-lookup"><span data-stu-id="f0abe-117">No extensibility.</span></span> <span data-ttu-id="f0abe-118">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="f0abe-118">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0abe-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0abe-119">Requirements</span></span>



| <span data-ttu-id="f0abe-120">需求</span><span class="sxs-lookup"><span data-stu-id="f0abe-120">Requirement</span></span> | <span data-ttu-id="f0abe-121">值</span><span class="sxs-lookup"><span data-stu-id="f0abe-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f0abe-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f0abe-122">TAPI version</span></span><br/> | <span data-ttu-id="f0abe-123">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f0abe-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f0abe-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f0abe-124">Header</span></span><br/>       | <dl> <span data-ttu-id="f0abe-125"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="f0abe-125"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0abe-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0abe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0abe-127">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="f0abe-127">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="f0abe-128">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="f0abe-128">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="f0abe-129">**LINETRANSLATEOUTPUT**</span><span class="sxs-lookup"><span data-stu-id="f0abe-129">**LINETRANSLATEOUTPUT**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




