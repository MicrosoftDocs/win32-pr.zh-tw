---
description: 包含 D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESS 查詢的輸入資料 \_ 。
ms.assetid: a1ceb394-7af9-4f05-9f58-a3103bf0150e
title: 'D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 06c4421f048af80186077da022fdecfaea79dca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973988"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_input-structure"></a><span data-ttu-id="3aeb7-103">D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ 輸入結構</span><span class="sxs-lookup"><span data-stu-id="3aeb7-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT structure</span></span>

<span data-ttu-id="3aeb7-104">包含 [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) 查詢的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="3aeb7-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="3aeb7-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="3aeb7-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="3aeb7-106">語法</span><span class="sxs-lookup"><span data-stu-id="3aeb7-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                ProcessIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT;
```



## <a name="members"></a><span data-ttu-id="3aeb7-107">成員</span><span class="sxs-lookup"><span data-stu-id="3aeb7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3aeb7-108">**輸入**</span><span class="sxs-lookup"><span data-stu-id="3aeb7-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="3aeb7-109">[**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)結構，其中包含查詢和其他資料的 GUID。</span><span class="sxs-lookup"><span data-stu-id="3aeb7-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="3aeb7-110">**ProcessIndex**</span><span class="sxs-lookup"><span data-stu-id="3aeb7-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="3aeb7-111">處理序的索引。</span><span class="sxs-lookup"><span data-stu-id="3aeb7-111">The index of the process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3aeb7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3aeb7-112">Requirements</span></span>



| <span data-ttu-id="3aeb7-113">需求</span><span class="sxs-lookup"><span data-stu-id="3aeb7-113">Requirement</span></span> | <span data-ttu-id="3aeb7-114">值</span><span class="sxs-lookup"><span data-stu-id="3aeb7-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aeb7-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3aeb7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3aeb7-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3aeb7-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3aeb7-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3aeb7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3aeb7-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3aeb7-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3aeb7-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3aeb7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aeb7-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="3aeb7-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aeb7-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3aeb7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aeb7-122">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="3aeb7-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="3aeb7-123">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="3aeb7-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




