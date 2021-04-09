---
description: 包含 D3DAUTHENTICATEDQUERY OUTPUTIDCOUNT 查詢的輸入資料 \_ 。
ms.assetid: cc68b39f-4645-46a6-a752-549b070cf23b
title: 'D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 93f58bcd05efb8c173986186d631c713195d8363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111816"
---
# <a name="d3dauthenticatedchannel_queryoutputidcount_input-structure"></a><span data-ttu-id="e07ac-103">D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ 輸入結構</span><span class="sxs-lookup"><span data-stu-id="e07ac-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT structure</span></span>

<span data-ttu-id="e07ac-104">包含 [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) 查詢的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="e07ac-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) query.</span></span>

<span data-ttu-id="e07ac-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="e07ac-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="e07ac-106">語法</span><span class="sxs-lookup"><span data-stu-id="e07ac-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTIDCOUNT_INPUT;
```



## <a name="members"></a><span data-ttu-id="e07ac-107">成員</span><span class="sxs-lookup"><span data-stu-id="e07ac-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e07ac-108">**輸入**</span><span class="sxs-lookup"><span data-stu-id="e07ac-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="e07ac-109">[**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)結構，其中包含查詢和其他資料的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e07ac-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="e07ac-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="e07ac-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="e07ac-111">裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e07ac-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="e07ac-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="e07ac-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="e07ac-113">密碼編譯會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e07ac-113">A handle to the cryptographic session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e07ac-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e07ac-114">Requirements</span></span>



| <span data-ttu-id="e07ac-115">需求</span><span class="sxs-lookup"><span data-stu-id="e07ac-115">Requirement</span></span> | <span data-ttu-id="e07ac-116">值</span><span class="sxs-lookup"><span data-stu-id="e07ac-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e07ac-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e07ac-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e07ac-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e07ac-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e07ac-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e07ac-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e07ac-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e07ac-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e07ac-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e07ac-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e07ac-122"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="e07ac-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e07ac-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e07ac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07ac-124">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="e07ac-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="e07ac-125">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="e07ac-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




