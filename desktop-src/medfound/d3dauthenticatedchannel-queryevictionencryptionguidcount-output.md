---
description: 包含對 D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT 查詢的回應。
ms.assetid: 168f9455-8dc6-473a-ad2c-e51996b63650
title: 'D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 51668dccdfa15649ec2a062a1231eb0b16e68ff8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970943"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguidcount_output-structure"></a><span data-ttu-id="0ef69-103">D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="0ef69-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="0ef69-104">包含對 [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="0ef69-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) query.</span></span>

<span data-ttu-id="0ef69-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="0ef69-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef69-106">語法</span><span class="sxs-lookup"><span data-stu-id="0ef69-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  NumEncryptionGuids                   UINT;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="0ef69-107">成員</span><span class="sxs-lookup"><span data-stu-id="0ef69-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ef69-108">**輸出**</span><span class="sxs-lookup"><span data-stu-id="0ef69-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="0ef69-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="0ef69-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="0ef69-110">**UINT**</span><span class="sxs-lookup"><span data-stu-id="0ef69-110">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="0ef69-111">加密 Guid 的數目。</span><span class="sxs-lookup"><span data-stu-id="0ef69-111">The number of encryption GUIDs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ef69-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ef69-112">Requirements</span></span>



| <span data-ttu-id="0ef69-113">需求</span><span class="sxs-lookup"><span data-stu-id="0ef69-113">Requirement</span></span> | <span data-ttu-id="0ef69-114">值</span><span class="sxs-lookup"><span data-stu-id="0ef69-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef69-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ef69-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0ef69-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ef69-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0ef69-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ef69-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0ef69-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ef69-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0ef69-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0ef69-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ef69-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef69-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef69-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ef69-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef69-122">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="0ef69-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="0ef69-123">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="0ef69-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




