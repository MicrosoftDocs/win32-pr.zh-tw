---
description: 包含對 D3DAUTHENTICATEDQUERY \_ OUTPUTID 查詢的回應。
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: 'D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 26686126fd2a5cb942c88ea485f753d2432499dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026045"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a><span data-ttu-id="cd1f9-103">D3DAUTHENTICATEDCHANNEL \_ QUERYROUTPUTID \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="cd1f9-103">D3DAUTHENTICATEDCHANNEL\_QUERYROUTPUTID\_OUTPUT structure</span></span>

<span data-ttu-id="cd1f9-104">包含對 [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="cd1f9-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="cd1f9-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="cd1f9-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd1f9-106">語法</span><span class="sxs-lookup"><span data-stu-id="cd1f9-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="cd1f9-107">成員</span><span class="sxs-lookup"><span data-stu-id="cd1f9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd1f9-108">**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="cd1f9-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="cd1f9-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="cd1f9-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="cd1f9-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="cd1f9-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="cd1f9-111">裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd1f9-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="cd1f9-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="cd1f9-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="cd1f9-113">密碼編譯會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cd1f9-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="cd1f9-114">**OutputIDIndex**</span><span class="sxs-lookup"><span data-stu-id="cd1f9-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="cd1f9-115">**OutputID** 成員中指定的輸出識別碼索引。</span><span class="sxs-lookup"><span data-stu-id="cd1f9-115">The index of the output ID given in the **OutputID** member.</span></span>

</dd> <dt>

<span data-ttu-id="cd1f9-116">**OutputID**</span><span class="sxs-lookup"><span data-stu-id="cd1f9-116">**OutputID**</span></span>
</dt> <dd>

<span data-ttu-id="cd1f9-117">與指定的裝置和密碼編譯會話相關聯的輸出識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd1f9-117">An output ID that is associated with the specified device and cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd1f9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd1f9-118">Requirements</span></span>



| <span data-ttu-id="cd1f9-119">需求</span><span class="sxs-lookup"><span data-stu-id="cd1f9-119">Requirement</span></span> | <span data-ttu-id="cd1f9-120">值</span><span class="sxs-lookup"><span data-stu-id="cd1f9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd1f9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd1f9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cd1f9-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd1f9-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cd1f9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd1f9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cd1f9-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd1f9-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cd1f9-125">標頭</span><span class="sxs-lookup"><span data-stu-id="cd1f9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd1f9-126"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd1f9-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd1f9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd1f9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd1f9-128">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="cd1f9-128">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="cd1f9-129">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="cd1f9-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




