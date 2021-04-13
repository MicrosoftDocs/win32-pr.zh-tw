---
description: 包含 D3DAUTHENTICATEDQUERY ENCRYPTIONWHENACCESSIBLEGUID 查詢的輸入資料 \_ 。
ms.assetid: 0e24e393-3f63-4c6f-aca1-f73ced3490ba
title: 'D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1c4500d27577883f46d00580dcc7e306b4008cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386038"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_input-structure"></a><span data-ttu-id="87e0b-103">D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ 輸入結構</span><span class="sxs-lookup"><span data-stu-id="87e0b-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT structure</span></span>

<span data-ttu-id="87e0b-104">包含 [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) 查詢的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="87e0b-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="87e0b-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="87e0b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="87e0b-106">語法</span><span class="sxs-lookup"><span data-stu-id="87e0b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                EncryptionGuidIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_INPUT;
```



## <a name="members"></a><span data-ttu-id="87e0b-107">成員</span><span class="sxs-lookup"><span data-stu-id="87e0b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="87e0b-108">**輸入**</span><span class="sxs-lookup"><span data-stu-id="87e0b-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="87e0b-109">[**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)結構，其中包含查詢和其他資料的 GUID。</span><span class="sxs-lookup"><span data-stu-id="87e0b-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="87e0b-110">**EncryptionGuidIndex**</span><span class="sxs-lookup"><span data-stu-id="87e0b-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="87e0b-111">加密 GUID 的索引。</span><span class="sxs-lookup"><span data-stu-id="87e0b-111">The index of the encryption GUID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87e0b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="87e0b-112">Requirements</span></span>



| <span data-ttu-id="87e0b-113">需求</span><span class="sxs-lookup"><span data-stu-id="87e0b-113">Requirement</span></span> | <span data-ttu-id="87e0b-114">值</span><span class="sxs-lookup"><span data-stu-id="87e0b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87e0b-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87e0b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="87e0b-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87e0b-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="87e0b-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87e0b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="87e0b-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87e0b-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="87e0b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="87e0b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="87e0b-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="87e0b-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87e0b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87e0b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e0b-122">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="87e0b-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="87e0b-123">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="87e0b-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




