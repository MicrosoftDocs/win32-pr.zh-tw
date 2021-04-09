---
description: 包含 IDirect3DAuthenticatedChannel9：： Query 方法的回應。
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: 'D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111820"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a><span data-ttu-id="2a64b-103">D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="2a64b-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT structure</span></span>

<span data-ttu-id="2a64b-104">包含 [**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) 方法的回應。</span><span class="sxs-lookup"><span data-stu-id="2a64b-104">Contains the response from the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a64b-105">語法</span><span class="sxs-lookup"><span data-stu-id="2a64b-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="2a64b-106">成員</span><span class="sxs-lookup"><span data-stu-id="2a64b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2a64b-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="2a64b-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="2a64b-108">[**D3D \_ OMAC**](d3d-omac.md)結構，其中包含資料的訊息驗證碼 (MAC) 。</span><span class="sxs-lookup"><span data-stu-id="2a64b-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="2a64b-109">驅動程式會使用 AES 型單鍵 CBC MAC (OMAC) 為此結構成員後面出現的資料區塊計算此值。</span><span class="sxs-lookup"><span data-stu-id="2a64b-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="2a64b-110">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="2a64b-110">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="2a64b-111">指定查詢的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2a64b-111">A GUID that specifies the query.</span></span> <span data-ttu-id="2a64b-112">如需值的清單，請參閱 [內容保護查詢](content-protection-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="2a64b-112">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a64b-113">**處理**</span><span class="sxs-lookup"><span data-stu-id="2a64b-113">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="2a64b-114">已驗證通道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2a64b-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="2a64b-115">**UINT**</span><span class="sxs-lookup"><span data-stu-id="2a64b-115">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="2a64b-116">查詢序號。</span><span class="sxs-lookup"><span data-stu-id="2a64b-116">The query sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="2a64b-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="2a64b-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="2a64b-118">查詢的結果碼。</span><span class="sxs-lookup"><span data-stu-id="2a64b-118">The result code for the query.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a64b-119">備註</span><span class="sxs-lookup"><span data-stu-id="2a64b-119">Remarks</span></span>

<span data-ttu-id="2a64b-120">針對 **QueryType**、 **hChannel** 和 **SequenceNumber** 成員，驅動程式會使用與應用程式在 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md) 結構中所提供的相同值。</span><span class="sxs-lookup"><span data-stu-id="2a64b-120">For the **QueryType**, **hChannel**, and **SequenceNumber** members, the driver uses in the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure.</span></span> <span data-ttu-id="2a64b-121">應用程式應該驗證這些值是否相符。</span><span class="sxs-lookup"><span data-stu-id="2a64b-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a64b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a64b-122">Requirements</span></span>



| <span data-ttu-id="2a64b-123">需求</span><span class="sxs-lookup"><span data-stu-id="2a64b-123">Requirement</span></span> | <span data-ttu-id="2a64b-124">值</span><span class="sxs-lookup"><span data-stu-id="2a64b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a64b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a64b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2a64b-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a64b-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2a64b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a64b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2a64b-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a64b-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2a64b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2a64b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a64b-130"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a64b-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a64b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a64b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a64b-132">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="2a64b-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="2a64b-133">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="2a64b-133">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




