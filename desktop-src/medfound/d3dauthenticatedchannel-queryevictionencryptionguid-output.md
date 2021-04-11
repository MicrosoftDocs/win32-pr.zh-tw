---
description: 包含對 D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID 查詢的回應。
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: 'D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8fa46095c5075b0a36ed691978b73de1e7b8cade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847634"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a><span data-ttu-id="bfcf5-103">D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="bfcf5-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT structure</span></span>

<span data-ttu-id="bfcf5-104">包含對 [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="bfcf5-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="bfcf5-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="bfcf5-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfcf5-106">語法</span><span class="sxs-lookup"><span data-stu-id="bfcf5-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="bfcf5-107">成員</span><span class="sxs-lookup"><span data-stu-id="bfcf5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bfcf5-108">**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="bfcf5-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf5-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="bfcf5-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="bfcf5-110">**EncryptionGuidIndex**</span><span class="sxs-lookup"><span data-stu-id="bfcf5-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf5-111">加密 GUID 的索引。</span><span class="sxs-lookup"><span data-stu-id="bfcf5-111">The index of the encryption GUID.</span></span>

</dd> <dt>

<span data-ttu-id="bfcf5-112">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="bfcf5-112">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="bfcf5-113">指定支援之加密類型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="bfcf5-113">A GUID that specifies a supported encryption type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfcf5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfcf5-114">Requirements</span></span>



| <span data-ttu-id="bfcf5-115">需求</span><span class="sxs-lookup"><span data-stu-id="bfcf5-115">Requirement</span></span> | <span data-ttu-id="bfcf5-116">值</span><span class="sxs-lookup"><span data-stu-id="bfcf5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcf5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bfcf5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bfcf5-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfcf5-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bfcf5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bfcf5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bfcf5-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfcf5-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bfcf5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="bfcf5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfcf5-122"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="bfcf5-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfcf5-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfcf5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfcf5-124">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="bfcf5-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="bfcf5-125">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="bfcf5-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




