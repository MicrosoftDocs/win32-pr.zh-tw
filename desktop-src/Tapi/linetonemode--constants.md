---
description: LINETONEMODE \_ 常數描述產生換行時所使用的不同選項。
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: 'LINETONEMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995624"
---
# <a name="linetonemode_-constants"></a><span data-ttu-id="cb9d6-103">LINETONEMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="cb9d6-103">LINETONEMODE\_ Constants</span></span>

<span data-ttu-id="cb9d6-104">**LINETONEMODE \_ 常數** 描述產生換行時所使用的不同選項。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-104">The **LINETONEMODE\_ constants** describe different selections that are used when generating line tones.</span></span>

<dl> <dt>

<span data-ttu-id="cb9d6-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE \_ 嗶聲**</span><span class="sxs-lookup"><span data-stu-id="cb9d6-105"><span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**LINETONEMODE\_BEEP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cb9d6-106">色調是一種嗶聲，例如用來宣佈錄製開頭的聲提示。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-106">The tone is a beep, such as that used to announce the beginning of a recording.</span></span> <span data-ttu-id="cb9d6-107">確切定義是定義的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-107">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cb9d6-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**LINETONEMODE \_ 帳單**</span><span class="sxs-lookup"><span data-stu-id="cb9d6-108"><span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**LINETONEMODE\_BILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cb9d6-109">語氣是帳單資訊語氣，例如信用卡提示音。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-109">The tone is a billing information tone such as a credit card prompt tone.</span></span> <span data-ttu-id="cb9d6-110">確切定義是定義的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-110">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cb9d6-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="cb9d6-111"><span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cb9d6-112">色調是忙碌的聲音。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-112">The tone is a busy tone.</span></span> <span data-ttu-id="cb9d6-113">確切定義是定義的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-113">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cb9d6-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ 自訂**</span><span class="sxs-lookup"><span data-stu-id="cb9d6-114"><span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cb9d6-115">色調是由其元件頻率定義的自訂色調，其類型為 [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone)。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-115">The tone is a custom tone defined by its component frequencies, of type [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cb9d6-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE \_ 回電**</span><span class="sxs-lookup"><span data-stu-id="cb9d6-116"><span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cb9d6-117">語氣是回電語氣。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-117">The tone is ringback tone.</span></span> <span data-ttu-id="cb9d6-118">確切定義是定義的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-118">Exact definition is service-provider defined.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb9d6-119">備註</span><span class="sxs-lookup"><span data-stu-id="cb9d6-119">Remarks</span></span>

<span data-ttu-id="cb9d6-120">您可以為裝置專屬的延伸模組指派高序位16位。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-120">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="cb9d6-121">低序位16位是保留的。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-121">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="cb9d6-122">這些常數用來定義透過呼叫遠端方所產生的聲音 inband。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-122">These constants are used to define tones to be generated inband over a call to the remote party.</span></span> <span data-ttu-id="cb9d6-123">請注意，非自訂色調的色調偵測不會使用這些常數。</span><span class="sxs-lookup"><span data-stu-id="cb9d6-123">Note that tone detection of non-custom tones does not use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb9d6-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb9d6-124">Requirements</span></span>



| <span data-ttu-id="cb9d6-125">需求</span><span class="sxs-lookup"><span data-stu-id="cb9d6-125">Requirement</span></span> | <span data-ttu-id="cb9d6-126">值</span><span class="sxs-lookup"><span data-stu-id="cb9d6-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cb9d6-127">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="cb9d6-127">TAPI version</span></span><br/> | <span data-ttu-id="cb9d6-128">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="cb9d6-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cb9d6-129">標頭</span><span class="sxs-lookup"><span data-stu-id="cb9d6-129">Header</span></span><br/>       | <dl> <span data-ttu-id="cb9d6-130"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="cb9d6-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




