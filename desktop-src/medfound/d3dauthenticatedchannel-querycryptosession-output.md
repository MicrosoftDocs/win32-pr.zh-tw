---
description: 包含對 D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION 查詢的回應。
ms.assetid: df9d9b41-8188-4597-9e83-d14065eb7fc7
title: 'D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fb4e6ccad999f183e71f0f57d64544a70cef5534
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971983"
---
# <a name="d3dauthenticatedchannel_querycryptosession_output-structure"></a><span data-ttu-id="72d03-103">D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="72d03-103">D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT structure</span></span>

<span data-ttu-id="72d03-104">包含對 [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="72d03-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) query.</span></span>

<span data-ttu-id="72d03-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="72d03-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="72d03-106">語法</span><span class="sxs-lookup"><span data-stu-id="72d03-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DXVA2DecodeHandle;
  HANDLE                               CryptoSessionHandle;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="72d03-107">成員</span><span class="sxs-lookup"><span data-stu-id="72d03-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="72d03-108">**輸出**</span><span class="sxs-lookup"><span data-stu-id="72d03-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="72d03-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="72d03-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="72d03-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="72d03-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="72d03-111">DirectX Video 加速 2 (DXVA-2) 解碼器裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="72d03-111">A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="72d03-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="72d03-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="72d03-113">與解碼器裝置相關聯的密碼編譯會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="72d03-113">A handle to the cryptographic session that is associated with the decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="72d03-114">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="72d03-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="72d03-115">與解碼器裝置相關聯之 Direct3D 裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="72d03-115">A handle to the Direct3D device that is associated with the decoder device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72d03-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="72d03-116">Requirements</span></span>



| <span data-ttu-id="72d03-117">需求</span><span class="sxs-lookup"><span data-stu-id="72d03-117">Requirement</span></span> | <span data-ttu-id="72d03-118">值</span><span class="sxs-lookup"><span data-stu-id="72d03-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72d03-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72d03-119">Minimum supported client</span></span><br/> | <span data-ttu-id="72d03-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72d03-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72d03-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72d03-121">Minimum supported server</span></span><br/> | <span data-ttu-id="72d03-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72d03-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="72d03-123">標頭</span><span class="sxs-lookup"><span data-stu-id="72d03-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d03-124"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="72d03-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d03-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72d03-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d03-126">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="72d03-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="72d03-127">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="72d03-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




