---
description: 包含對 D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES 查詢的回應。
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: 'D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 853488c98687825ab55d642b2e01e569f0d435c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970743"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a><span data-ttu-id="5477f-103">D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="5477f-103">D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="5477f-104">包含對 [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="5477f-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) query.</span></span>

<span data-ttu-id="5477f-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="5477f-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="5477f-106">語法</span><span class="sxs-lookup"><span data-stu-id="5477f-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="5477f-107">成員</span><span class="sxs-lookup"><span data-stu-id="5477f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5477f-108">**輸出**</span><span class="sxs-lookup"><span data-stu-id="5477f-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="5477f-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="5477f-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="5477f-110">**BusType**</span><span class="sxs-lookup"><span data-stu-id="5477f-110">**BusType**</span></span>
</dt> <dd>

<span data-ttu-id="5477f-111">來自 [**D3DBUSTYPE**](d3dbustype.md)列舉之旗標的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="5477f-111">A bitwise **OR** of flags from the [**D3DBUSTYPE**](d3dbustype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="5477f-112">**bAccessibleInContiguousBlocks**</span><span class="sxs-lookup"><span data-stu-id="5477f-112">**bAccessibleInContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="5477f-113">若 **為 TRUE**，則 CPU 或匯流排可以存取影片記憶體的連續區塊。</span><span class="sxs-lookup"><span data-stu-id="5477f-113">If **TRUE**, contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> <dt>

<span data-ttu-id="5477f-114">**bAccessibleInNonContiguousBlocks**</span><span class="sxs-lookup"><span data-stu-id="5477f-114">**bAccessibleInNonContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="5477f-115">若 **為 TRUE**，則 CPU 或匯流排可以存取非連續的影片記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="5477f-115">If **TRUE**, non-contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5477f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5477f-116">Requirements</span></span>



| <span data-ttu-id="5477f-117">需求</span><span class="sxs-lookup"><span data-stu-id="5477f-117">Requirement</span></span> | <span data-ttu-id="5477f-118">值</span><span class="sxs-lookup"><span data-stu-id="5477f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5477f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5477f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5477f-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5477f-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5477f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5477f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5477f-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5477f-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5477f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5477f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5477f-124"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="5477f-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5477f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5477f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5477f-126">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="5477f-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="5477f-127">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="5477f-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




