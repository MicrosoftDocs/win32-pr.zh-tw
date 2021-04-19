---
description: LINEADDRESSMODE \_ 位旗標常數描述線上路裝置上識別位址的各種方式。
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: 'LINEADDRESSMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977532"
---
# <a name="lineaddressmode_-constants"></a><span data-ttu-id="55358-103">LINEADDRESSMODE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="55358-103">LINEADDRESSMODE\_ Constants</span></span>

<span data-ttu-id="55358-104">**LINEADDRESSMODE \_** 位旗標常數描述線上路裝置上識別位址的各種方式。</span><span class="sxs-lookup"><span data-stu-id="55358-104">The **LINEADDRESSMODE\_** bit-flag constants describe various ways of identifying an address on a line device.</span></span>

<dl> <dt>

<span data-ttu-id="55358-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ ADDRESSID**</span><span class="sxs-lookup"><span data-stu-id="55358-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE\_ADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55358-106">使用範圍0至 *dwNumAddresses* 減去1的小整數來指定位址，其中 *dwNumAddresses* 是行裝置功能的值。</span><span class="sxs-lookup"><span data-stu-id="55358-106">The address is specified with a small integer in the range 0 to *dwNumAddresses* minus one, where *dwNumAddresses* is the value in the line's device capabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55358-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**</span><span class="sxs-lookup"><span data-stu-id="55358-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE\_DIALABLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="55358-108">位址是透過其電話號碼來指定。</span><span class="sxs-lookup"><span data-stu-id="55358-108">The address is specified through its phone number.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55358-109">備註</span><span class="sxs-lookup"><span data-stu-id="55358-109">Remarks</span></span>

<span data-ttu-id="55358-110">您可以為裝置專屬的延伸模組指派高序位16位。</span><span class="sxs-lookup"><span data-stu-id="55358-110">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="55358-111">低序位16位是保留的。</span><span class="sxs-lookup"><span data-stu-id="55358-111">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="55358-112">這個常數用來選取要在其上產生呼叫的行位址。</span><span class="sxs-lookup"><span data-stu-id="55358-112">This constant is used to select an address on a line on which to originate a call.</span></span> <span data-ttu-id="55358-113">一般模型會透過其位址識別碼來選取位址。</span><span class="sxs-lookup"><span data-stu-id="55358-113">The usual model would select the address by means of its address identifier.</span></span> <span data-ttu-id="55358-114">位址識別碼是用來在整個 TAPI 中識別位址的機制。</span><span class="sxs-lookup"><span data-stu-id="55358-114">Address identifiers are the mechanism used to identify addresses throughout TAPI.</span></span> <span data-ttu-id="55358-115">不過，在某些環境下進行呼叫時，使用電話號碼（而不是依位址識別碼）來識別來電的起始位址通常會更實用。</span><span class="sxs-lookup"><span data-stu-id="55358-115">However, in some environments, when making a call, it is often more practical to identify a call's originating address by phone number rather than by address identifier.</span></span> <span data-ttu-id="55358-116">其中一個範例是透過一個具有許多位址的線路裝置，在交換器上將大量電臺 (協力廠商) 的可能模型化。</span><span class="sxs-lookup"><span data-stu-id="55358-116">One example is in the possible modeling of large numbers of stations (third party) on the switch by means of one line device with many addresses.</span></span> <span data-ttu-id="55358-117">這一行代表所有工作站的集合，而且每個工作站都會對應到具有自己的主要電話號碼和位址識別碼的位址。</span><span class="sxs-lookup"><span data-stu-id="55358-117">The line represents the set of all stations, and each station is mapped to an address with its own primary phone number and address identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="55358-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="55358-118">Requirements</span></span>



| <span data-ttu-id="55358-119">需求</span><span class="sxs-lookup"><span data-stu-id="55358-119">Requirement</span></span> | <span data-ttu-id="55358-120">值</span><span class="sxs-lookup"><span data-stu-id="55358-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="55358-121">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="55358-121">TAPI version</span></span><br/> | <span data-ttu-id="55358-122">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="55358-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="55358-123">標頭</span><span class="sxs-lookup"><span data-stu-id="55358-123">Header</span></span><br/>       | <dl> <span data-ttu-id="55358-124"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="55358-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




