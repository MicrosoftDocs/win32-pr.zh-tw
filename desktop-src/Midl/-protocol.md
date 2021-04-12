---
title: /protocol 參數
description: /Protocol 參數會指定產生的存根所支援的網路通訊協定。
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- /protocol 參數 MIDL
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313023"
---
# <a name="protocol-switch"></a><span data-ttu-id="720b1-104">/protocol 參數</span><span class="sxs-lookup"><span data-stu-id="720b1-104">/protocol switch</span></span>

<span data-ttu-id="720b1-105">**/Protocol** 參數會指定產生的存根所支援的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="720b1-105">The **/protocol** switch specifies which wire protocol is supported by the generated stub.</span></span>

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a><span data-ttu-id="720b1-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="720b1-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span data-ttu-id="720b1-107"><span id="dce"></span><span id="DCE"></span>dce \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="720b1-107"><span id="dce"></span><span id="DCE"></span>\*\*\*\*dce\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="720b1-108">產生的存根僅支援 DCE 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="720b1-108">The generated stub supports DCE protocol only.</span></span>

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span data-ttu-id="720b1-109"><span id="ndr64"></span><span id="NDR64"></span>ndr64\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="720b1-109"><span id="ndr64"></span><span id="NDR64"></span>\*\*\*\*ndr64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="720b1-110">產生的存根僅支援 Microsoft NDR64 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="720b1-110">The generated stub supports Microsoft NDR64 protocol only.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="720b1-111"><span id="all"></span><span id="ALL"></span>全部 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="720b1-111"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="720b1-112">產生的存根支援指定環境的所有可用通訊協定。</span><span class="sxs-lookup"><span data-stu-id="720b1-112">The generated stub supports all available protocols for a given environment.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="720b1-113">備註</span><span class="sxs-lookup"><span data-stu-id="720b1-113">Remarks</span></span>

<span data-ttu-id="720b1-114">RPC 會根據嚴格的線路通訊協定（也稱為傳輸語法）來封送處理和拆收資料，以定義資料線路的標記法，例如封送處理資料成員的順序、網路上的資料對齊方式、資料隨附的額外資訊，還有其他資訊。</span><span class="sxs-lookup"><span data-stu-id="720b1-114">RPC marshals and unmarshals data according to a strict wire protocol, also called transfer syntax, that defines data wire representation such as the order in which data members are marshaled, the alignment of data on the wire, additional information included with the data, among others.</span></span> <span data-ttu-id="720b1-115">Microsoft RPC 與憑證 DCE 的 NDR (網路資料表示) 通訊協定相容。</span><span class="sxs-lookup"><span data-stu-id="720b1-115">Microsoft RPC is compatible with OSF DCE's NDR (network data representation) protocol.</span></span> <span data-ttu-id="720b1-116">在 Windows XP 的64位版本中，Microsoft 引進了針對傳輸64位資料優化的實驗性通訊協定 NDR64。</span><span class="sxs-lookup"><span data-stu-id="720b1-116">In the 64-bit release of Windows XP, Microsoft introduces an experimental protocol NDR64 that is optimized for transferring 64-bit data.</span></span> <span data-ttu-id="720b1-117">NDR64 與 DCE 通訊協定沒有回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="720b1-117">NDR64 is not backward compatible with the DCE protocol.</span></span>

<span data-ttu-id="720b1-118">**Dce** 通訊協定與憑證 DCE 的 NDR 傳輸語法相容。</span><span class="sxs-lookup"><span data-stu-id="720b1-118">The **dce** protocol is compatible with OSF DCE's NDR transfer syntax.</span></span> <span data-ttu-id="720b1-119">此通訊協定已針對傳輸32位資料進行優化。</span><span class="sxs-lookup"><span data-stu-id="720b1-119">This protocol is optimized for transferring 32-bit data.</span></span>

<span data-ttu-id="720b1-120">目前只有在搭配 [**/win64**](-win64.md)參數使用時，才支援 **ndr64** 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="720b1-120">The **ndr64** protocol is currently supported only when used in conjunction with the [**/win64**](-win64.md) switch.</span></span> <span data-ttu-id="720b1-121">如果僅 ndr64 用戶端嘗試連線到僅限 dce 的伺服器，反之亦然，則會使用 RPC \_ S \_ 不支援的非 \_ 交易 \_ SYN 來拒絕呼叫。</span><span class="sxs-lookup"><span data-stu-id="720b1-121">If a ndr64 only client tries to connect to a dce-only server, or vice versa, the call is rejected with RPC\_S\_UNSUPPORTED\_TRANS\_SYN.</span></span>

<span data-ttu-id="720b1-122">**All** 選項會建立可使用任何可用通訊協定的存根。</span><span class="sxs-lookup"><span data-stu-id="720b1-122">The **all** option creates a stub that may use any available protocol.</span></span> <span data-ttu-id="720b1-123">若為32位的存根，目前唯一可用的通訊協定為 DCE。</span><span class="sxs-lookup"><span data-stu-id="720b1-123">For 32-bit stubs, the only protocol currently available is DCE.</span></span> <span data-ttu-id="720b1-124">針對使用 [**/win64**](-win64.md) 參數建立的64位存根，可使用 DCE 和 NDR64。</span><span class="sxs-lookup"><span data-stu-id="720b1-124">For 64-bit stubs, created using the [**/win64**](-win64.md) switch, both DCE and NDR64 are available.</span></span>

## <a name="examples"></a><span data-ttu-id="720b1-125">範例</span><span class="sxs-lookup"><span data-stu-id="720b1-125">Examples</span></span>

<span data-ttu-id="720b1-126">**midl/protocol 所有/win64 的檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="720b1-126">**midl /protocol all /win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="720b1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="720b1-127">See also</span></span>

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 




