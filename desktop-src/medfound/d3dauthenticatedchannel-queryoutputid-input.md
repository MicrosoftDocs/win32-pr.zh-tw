---
description: 包含 D3DAUTHENTICATEDQUERY OUTPUTID 查詢的輸入資料 \_ 。
ms.assetid: 8864c298-be9a-4ff4-a9c5-996b62937c18
title: 'D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7c64d43261ccc849772372110ad73169c698cd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984158"
---
# <a name="d3dauthenticatedchannel_queryoutputid_input-structure"></a><span data-ttu-id="029a0-103">D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ 輸入結構</span><span class="sxs-lookup"><span data-stu-id="029a0-103">D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT structure</span></span>

<span data-ttu-id="029a0-104">包含 [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) 查詢的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="029a0-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_OUTPUTID**](d3dauthenticatedquery-outputid.md) query.</span></span>

<span data-ttu-id="029a0-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="029a0-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="029a0-106">語法</span><span class="sxs-lookup"><span data-stu-id="029a0-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
  UINT                                OutputIDIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT;
```



## <a name="members"></a><span data-ttu-id="029a0-107">成員</span><span class="sxs-lookup"><span data-stu-id="029a0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="029a0-108">**輸入**</span><span class="sxs-lookup"><span data-stu-id="029a0-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="029a0-109">[**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**](d3dauthenticatedchannel-query-input.md)結構，其中包含查詢和其他資料的 GUID。</span><span class="sxs-lookup"><span data-stu-id="029a0-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="029a0-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="029a0-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="029a0-111">裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="029a0-111">A handle to the device.</span></span>

</dd> <dt>

<span data-ttu-id="029a0-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="029a0-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="029a0-113">密碼編譯會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="029a0-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="029a0-114">**OutputIDIndex**</span><span class="sxs-lookup"><span data-stu-id="029a0-114">**OutputIDIndex**</span></span>
</dt> <dd>

<span data-ttu-id="029a0-115">輸出識別碼的索引。</span><span class="sxs-lookup"><span data-stu-id="029a0-115">The index of the output ID.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="029a0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="029a0-116">Requirements</span></span>



| <span data-ttu-id="029a0-117">需求</span><span class="sxs-lookup"><span data-stu-id="029a0-117">Requirement</span></span> | <span data-ttu-id="029a0-118">值</span><span class="sxs-lookup"><span data-stu-id="029a0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="029a0-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="029a0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="029a0-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="029a0-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="029a0-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="029a0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="029a0-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="029a0-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="029a0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="029a0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="029a0-124"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="029a0-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="029a0-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="029a0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029a0-126">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="029a0-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="029a0-127">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="029a0-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




