---
description: LINEOFFERINGMODE \_ 位旗標常數 (TAPI 1.4 版和更新版本，) 描述供應專案呼叫的不同 substates。
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: 'LINEOFFERINGMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996231"
---
# <a name="lineofferingmode_-constants"></a><span data-ttu-id="88679-103">LINEOFFERINGMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="88679-103">LINEOFFERINGMODE\_ Constants</span></span>

<span data-ttu-id="88679-104">**LINEOFFERINGMODE \_** 位旗標常數 (TAPI 1.4 版和更新版本，) 描述供應專案呼叫的不同 substates。</span><span class="sxs-lookup"><span data-stu-id="88679-104">The **LINEOFFERINGMODE\_** bit-flag constants (TAPI versions 1.4 and later) describe different substates of an offering call.</span></span> <span data-ttu-id="88679-105">在提供撥號狀態 trdansitions 之後，您可以使用模式作為應用程式的撥號狀態，而在 [**\_ CALLSTATE**](line-callstate.md) 訊息中指出呼叫是在 LINECALLSTATE 供應專案中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="88679-105">A mode is available as call status to the application after the call state trdansitions to offering, and within the [**LINE\_CALLSTATE**](line-callstate.md) message indicating the call is in LINECALLSTATE\_OFFERING.</span></span> <span data-ttu-id="88679-106">當呼叫位於與其他工作站 (橋接) 的共用位址時，就會使用這些值 (查看 [**LINEADDRESSSHARING \_ 常數**](lineaddresssharing--constants.md)) ，主要是電子關鍵系統。</span><span class="sxs-lookup"><span data-stu-id="88679-106">These values are used when the call is on an address that is shared (bridged) with other stations (see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span>

<dl> <dt>

<span data-ttu-id="88679-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ 使用中**</span><span class="sxs-lookup"><span data-stu-id="88679-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88679-108">表示在目前工作站上發出的呼叫 (會伴隨 LINEDEVSTATE \_ 響鈴訊息) ，而且如果有任何應用程式設定為自動回答，則可以這樣做。</span><span class="sxs-lookup"><span data-stu-id="88679-108">Indicates that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="88679-109">如果撥號狀態模式為零，則應用程式應該假設該值為使用中 (這會是非橋接位址) 上的情況。</span><span class="sxs-lookup"><span data-stu-id="88679-109">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="88679-110"> (TAPI 1.4 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="88679-110">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88679-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ 非使用中**</span><span class="sxs-lookup"><span data-stu-id="88679-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88679-112">指出會在多個工作站上提供呼叫，但目前的工作站不會發出警示 (例如，它可能是供應專案狀態為「諮詢」的一站，例如閃爍的燈) ;工作站上設定自動接聽的軟體應最好不要接聽電話，因為這應該是主要 (警示) 站的特權用，但 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) 可能用來連接電話。</span><span class="sxs-lookup"><span data-stu-id="88679-112">Indicates that the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) may be used to connect the call.</span></span> <span data-ttu-id="88679-113"> (TAPI 1.4 版和更新版本) </span><span class="sxs-lookup"><span data-stu-id="88679-113">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88679-114">備註</span><span class="sxs-lookup"><span data-stu-id="88679-114">Remarks</span></span>

<span data-ttu-id="88679-115">不可延伸。</span><span class="sxs-lookup"><span data-stu-id="88679-115">Not extensible.</span></span> <span data-ttu-id="88679-116">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="88679-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="88679-117">為了回溯相容性，服務提供者必須負責檢查該行上的已協商 API 版本，如果已協商的版本不支援，則不會使用這些 LINEOFFERINGMODE \_ 值。</span><span class="sxs-lookup"><span data-stu-id="88679-117">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEOFFERINGMODE\_ values if they are not supported on the negotiated version.</span></span> <span data-ttu-id="88679-118">未 cognizant LINEOFFERINGMODE 的應用程式 \_ 很有可能會假設 LINECALLSTATE 供應專案中的呼叫位於 \_ LINEOFFERINGMODE \_ ACTIVE 中。</span><span class="sxs-lookup"><span data-stu-id="88679-118">Applications that are not cognizant of LINEOFFERINGMODE\_ will most likely assume that a call that is in LINECALLSTATE\_OFFERING is in LINEOFFERINGMODE\_ACTIVE.</span></span>

<span data-ttu-id="88679-119">\_ \_ 當呼叫位於與其他工作站共用 (橋接的位址時，會使用 LINEOFFERINGMODE ACTIVE 和 LINEOFFERINGMODE 非使用中的值; 請參閱[LINEADDRESSSHARING \_ 常數](lineaddresssharing--constants.md)) ，主要是電子金鑰系統。</span><span class="sxs-lookup"><span data-stu-id="88679-119">The LINEOFFERINGMODE\_ACTIVE and LINEOFFERINGMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [LINEADDRESSSHARING\_ Constants](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="88679-120">如果供應專案通話狀態模式為「作用中」，這表示呼叫會在目前的工作站上發出警示 (將會伴隨 LINEDEVSTATE \_ 響鈴訊息) ，而且如果有任何應用程式設定為自動回答，則可以這樣做。</span><span class="sxs-lookup"><span data-stu-id="88679-120">If the offering call state mode is "active," it means that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="88679-121">如果通話狀態模式為「非使用中」，則會在一個以上的工作站上提供呼叫，但目前的工作站不會發出警示 (例如，它可能是供應專案狀態為「諮詢」的通知站，例如閃爍燈的) ;工作站上設定自動接聽的軟體應最好不要接聽電話，因為這應該是主要 (警示) 站上的特權用，但 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) 可以用來連線通話。</span><span class="sxs-lookup"><span data-stu-id="88679-121">If the call state mode is "inactive," the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) can be used to connect the call.</span></span> <span data-ttu-id="88679-122">如果撥號狀態模式為零，則應用程式應該假設該值為使用中 (這會是非橋接位址) 上的情況。</span><span class="sxs-lookup"><span data-stu-id="88679-122">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span>

## <a name="requirements"></a><span data-ttu-id="88679-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="88679-123">Requirements</span></span>



| <span data-ttu-id="88679-124">需求</span><span class="sxs-lookup"><span data-stu-id="88679-124">Requirement</span></span> | <span data-ttu-id="88679-125">值</span><span class="sxs-lookup"><span data-stu-id="88679-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="88679-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="88679-126">TAPI version</span></span><br/> | <span data-ttu-id="88679-127">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="88679-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="88679-128">標頭</span><span class="sxs-lookup"><span data-stu-id="88679-128">Header</span></span><br/>       | <dl> <span data-ttu-id="88679-129"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="88679-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




