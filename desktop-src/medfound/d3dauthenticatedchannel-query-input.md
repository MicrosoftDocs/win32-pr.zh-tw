---
description: 包含 IDirect3DAuthenticatedChannel9：： Query 方法的輸入資料。
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: 'D3DAUTHENTICATEDCHANNEL_QUERY_INPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a0bec356b20569b5638848407eff27e930ef76b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191070"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a><span data-ttu-id="e31c1-103">D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入結構</span><span class="sxs-lookup"><span data-stu-id="e31c1-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT structure</span></span>

<span data-ttu-id="e31c1-104">包含 [**IDirect3DAuthenticatedChannel9：： Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) 方法的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="e31c1-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31c1-105">語法</span><span class="sxs-lookup"><span data-stu-id="e31c1-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a><span data-ttu-id="e31c1-106">成員</span><span class="sxs-lookup"><span data-stu-id="e31c1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e31c1-107">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="e31c1-107">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="e31c1-108">指定查詢的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e31c1-108">A GUID that specifies the query.</span></span> <span data-ttu-id="e31c1-109">如需值的清單，請參閱 [內容保護查詢](content-protection-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="e31c1-109">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="e31c1-110">**處理**</span><span class="sxs-lookup"><span data-stu-id="e31c1-110">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="e31c1-111">已驗證通道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e31c1-111">A handle to the authenticated channel.</span></span> <span data-ttu-id="e31c1-112">若要取得控制碼，請呼叫 [**IDirect3DDevice9Video：： CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)。</span><span class="sxs-lookup"><span data-stu-id="e31c1-112">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="e31c1-113">**UINT**</span><span class="sxs-lookup"><span data-stu-id="e31c1-113">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="e31c1-114">查詢序號。</span><span class="sxs-lookup"><span data-stu-id="e31c1-114">The query sequence number.</span></span> <span data-ttu-id="e31c1-115">在會話開始時，產生以密碼編譯的安全32位亂數字，作為起始序號使用。</span><span class="sxs-lookup"><span data-stu-id="e31c1-115">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="e31c1-116">針對每個查詢，將序號遞增1。</span><span class="sxs-lookup"><span data-stu-id="e31c1-116">For each query, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e31c1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e31c1-117">Requirements</span></span>



| <span data-ttu-id="e31c1-118">需求</span><span class="sxs-lookup"><span data-stu-id="e31c1-118">Requirement</span></span> | <span data-ttu-id="e31c1-119">值</span><span class="sxs-lookup"><span data-stu-id="e31c1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e31c1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e31c1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e31c1-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e31c1-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e31c1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e31c1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e31c1-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e31c1-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e31c1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e31c1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e31c1-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="e31c1-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e31c1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e31c1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31c1-127">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="e31c1-127">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="e31c1-128">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="e31c1-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




