---
description: 包含對 D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT 查詢的回應。
ms.assetid: dd6286d8-dfb5-413a-ba38-8b99dc8fe305
title: 'D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 60568e7056ab9df7aafcec1cac7864685c7c6100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689335"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocesscount_output-structure"></a><span data-ttu-id="8798f-103">D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="8798f-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="8798f-104">包含對 [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="8798f-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) query.</span></span>

<span data-ttu-id="8798f-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="8798f-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="8798f-106">語法</span><span class="sxs-lookup"><span data-stu-id="8798f-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumRestrictedSharedResourceProcesses;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="8798f-107">成員</span><span class="sxs-lookup"><span data-stu-id="8798f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8798f-108">**輸出**</span><span class="sxs-lookup"><span data-stu-id="8798f-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="8798f-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="8798f-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="8798f-110">**NumRestrictedSharedResourceProcesses**</span><span class="sxs-lookup"><span data-stu-id="8798f-110">**NumRestrictedSharedResourceProcesses**</span></span>
</dt> <dd>

<span data-ttu-id="8798f-111">允許開啟具有限制存取之共用資源的進程數目。</span><span class="sxs-lookup"><span data-stu-id="8798f-111">The number of processes allowed to open shared resources that have restricted access.</span></span> <span data-ttu-id="8798f-112">除非已授與進程存取權，否則進程無法開啟這類資源。</span><span class="sxs-lookup"><span data-stu-id="8798f-112">A process cannot open such a resource unless the process has been granted access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8798f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8798f-113">Requirements</span></span>



| <span data-ttu-id="8798f-114">需求</span><span class="sxs-lookup"><span data-stu-id="8798f-114">Requirement</span></span> | <span data-ttu-id="8798f-115">值</span><span class="sxs-lookup"><span data-stu-id="8798f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8798f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8798f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8798f-117">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8798f-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8798f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8798f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8798f-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8798f-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8798f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="8798f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8798f-121"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="8798f-121"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8798f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8798f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8798f-123">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="8798f-123">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="8798f-124">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="8798f-124">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




