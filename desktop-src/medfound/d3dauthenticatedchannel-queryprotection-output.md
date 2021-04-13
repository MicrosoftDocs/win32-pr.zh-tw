---
description: 包含對 D3DAUTHENTICATEDQUERY \_ PROTECTION 查詢的回應。
ms.assetid: eb99089a-5e8e-4970-9c40-7f6a9662b5ec
title: 'D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: d68cafdf545d93a290e90c54be134977e51de4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510812"
---
# <a name="d3dauthenticatedchannel_queryprotection_output-structure"></a><span data-ttu-id="2da36-103">D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="2da36-103">D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT structure</span></span>

<span data-ttu-id="2da36-104">包含對 [**D3DAUTHENTICATEDQUERY \_ PROTECTION**](d3dauthenticatedquery-protection.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="2da36-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_PROTECTION**](d3dauthenticatedquery-protection.md) query.</span></span>

<span data-ttu-id="2da36-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="2da36-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="2da36-106">語法</span><span class="sxs-lookup"><span data-stu-id="2da36-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT     Output;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS ProtectionFlags;
} D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="2da36-107">成員</span><span class="sxs-lookup"><span data-stu-id="2da36-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2da36-108">**輸出**</span><span class="sxs-lookup"><span data-stu-id="2da36-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="2da36-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="2da36-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="2da36-110">**ProtectionFlags**</span><span class="sxs-lookup"><span data-stu-id="2da36-110">**ProtectionFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2da36-111">[**D3DAUTHENTICATEDCHANNEL \_ 保護 \_ 旗標**](d3dauthenticatedchannel-protection-flags.md)結構，可指定保護層級。</span><span class="sxs-lookup"><span data-stu-id="2da36-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2da36-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2da36-112">Requirements</span></span>



| <span data-ttu-id="2da36-113">需求</span><span class="sxs-lookup"><span data-stu-id="2da36-113">Requirement</span></span> | <span data-ttu-id="2da36-114">值</span><span class="sxs-lookup"><span data-stu-id="2da36-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2da36-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2da36-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2da36-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2da36-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2da36-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2da36-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2da36-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2da36-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2da36-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2da36-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2da36-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="2da36-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da36-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2da36-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da36-122">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="2da36-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="2da36-123">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="2da36-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




