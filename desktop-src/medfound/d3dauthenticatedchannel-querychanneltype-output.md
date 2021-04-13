---
description: 包含對 D3DAUTHENTICATEDQUERY \_ CHANNELTYPE 查詢的回應。
ms.assetid: 547f7f26-2b9d-48b1-97cc-84a2202c3900
title: 'D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3120669da69f13359f49d8b8c38ed7d3e211a8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386040"
---
# <a name="d3dauthenticatedchannel_querychanneltype_output-structure"></a><span data-ttu-id="24d05-103">D3DAUTHENTICATEDCHANNEL \_ QUERYCHANNELTYPE \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="24d05-103">D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="24d05-104">包含對 [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="24d05-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) query.</span></span>

<span data-ttu-id="24d05-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="24d05-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="24d05-106">語法</span><span class="sxs-lookup"><span data-stu-id="24d05-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DAUTHENTICATEDCHANNELTYPE          ChannelType;
} D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="24d05-107">成員</span><span class="sxs-lookup"><span data-stu-id="24d05-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="24d05-108">**輸出**</span><span class="sxs-lookup"><span data-stu-id="24d05-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="24d05-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="24d05-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="24d05-110">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="24d05-110">**ChannelType**</span></span>
</dt> <dd>

<span data-ttu-id="24d05-111">指定通道類型的 [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) 值。</span><span class="sxs-lookup"><span data-stu-id="24d05-111">A [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) value that specifies the channel type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24d05-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="24d05-112">Requirements</span></span>



| <span data-ttu-id="24d05-113">需求</span><span class="sxs-lookup"><span data-stu-id="24d05-113">Requirement</span></span> | <span data-ttu-id="24d05-114">值</span><span class="sxs-lookup"><span data-stu-id="24d05-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24d05-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24d05-115">Minimum supported client</span></span><br/> | <span data-ttu-id="24d05-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24d05-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="24d05-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24d05-117">Minimum supported server</span></span><br/> | <span data-ttu-id="24d05-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24d05-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="24d05-119">標頭</span><span class="sxs-lookup"><span data-stu-id="24d05-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="24d05-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="24d05-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24d05-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24d05-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24d05-122">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="24d05-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="24d05-123">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="24d05-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




