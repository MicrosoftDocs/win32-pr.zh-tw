---
description: 包含對 D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT 查詢的回應。
ms.assetid: c283833d-e98c-4f01-b623-21027a6b90e8
title: 'D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fd30cff59d35f845903e7f4fdb08cdff61df3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979719"
---
# <a name="d3dauthenticatedchannel_queryunrestrictedprotectedsharedresourcecount_output-structure"></a><span data-ttu-id="af7c5-103">D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="af7c5-103">D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="af7c5-104">包含對 [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="af7c5-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) query.</span></span>

<span data-ttu-id="af7c5-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="af7c5-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="af7c5-106">語法</span><span class="sxs-lookup"><span data-stu-id="af7c5-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumUnrestrictedProtectedSharedResources;
} D3DAUTHENTICATEDCHANNEL_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="af7c5-107">成員</span><span class="sxs-lookup"><span data-stu-id="af7c5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="af7c5-108">**輸出**</span><span class="sxs-lookup"><span data-stu-id="af7c5-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="af7c5-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="af7c5-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="af7c5-110">**NumUnrestrictedProtectedSharedResources**</span><span class="sxs-lookup"><span data-stu-id="af7c5-110">**NumUnrestrictedProtectedSharedResources**</span></span>
</dt> <dd>

<span data-ttu-id="af7c5-111">受保護的共用資源數目，可由任何進程開啟而不受限制。</span><span class="sxs-lookup"><span data-stu-id="af7c5-111">The number of protected, shared resources that can be opened by any process without restrictions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af7c5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="af7c5-112">Requirements</span></span>



| <span data-ttu-id="af7c5-113">需求</span><span class="sxs-lookup"><span data-stu-id="af7c5-113">Requirement</span></span> | <span data-ttu-id="af7c5-114">值</span><span class="sxs-lookup"><span data-stu-id="af7c5-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af7c5-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af7c5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="af7c5-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af7c5-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="af7c5-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af7c5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="af7c5-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af7c5-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="af7c5-119">標頭</span><span class="sxs-lookup"><span data-stu-id="af7c5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="af7c5-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="af7c5-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af7c5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af7c5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af7c5-122">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="af7c5-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="af7c5-123">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="af7c5-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




