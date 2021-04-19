---
description: 傳回與這個已驗證通道相關聯之裝置的控制碼。
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: 'D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973795"
---
# <a name="d3dauthenticatedquery_devicehandle"></a><span data-ttu-id="2e27e-103">D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE</span><span class="sxs-lookup"><span data-stu-id="2e27e-103">D3DAUTHENTICATEDQUERY\_DEVICEHANDLE</span></span>

<span data-ttu-id="2e27e-104">傳回與這個已驗證通道相關聯之裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2e27e-104">Returns a handle to the device that is associated with this authenticated channel.</span></span> <span data-ttu-id="2e27e-105">您可以使用此控制碼來確認兩個已驗證的通道是否與相同裝置通訊。</span><span class="sxs-lookup"><span data-stu-id="2e27e-105">You can use this handle to verify whether two authenticated channels are communicating with the same device.</span></span>



| <span data-ttu-id="2e27e-106">需求</span><span class="sxs-lookup"><span data-stu-id="2e27e-106">Requirement</span></span> | <span data-ttu-id="2e27e-107">值</span><span class="sxs-lookup"><span data-stu-id="2e27e-107">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e27e-108">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="2e27e-108">Query GUID</span></span>  | <span data-ttu-id="2e27e-109">**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="2e27e-109">**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**</span></span>                                                                        |
| <span data-ttu-id="2e27e-110">輸入資料</span><span class="sxs-lookup"><span data-stu-id="2e27e-110">Input data</span></span>  | [<span data-ttu-id="2e27e-111">**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="2e27e-111">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                           |
| <span data-ttu-id="2e27e-112">傳回資料</span><span class="sxs-lookup"><span data-stu-id="2e27e-112">Return data</span></span> | [<span data-ttu-id="2e27e-113">**D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="2e27e-113">**D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="2e27e-114">備註</span><span class="sxs-lookup"><span data-stu-id="2e27e-114">Remarks</span></span>

<span data-ttu-id="2e27e-115">此查詢對於所有通道類型都有效。</span><span class="sxs-lookup"><span data-stu-id="2e27e-115">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e27e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e27e-116">Requirements</span></span>



| <span data-ttu-id="2e27e-117">需求</span><span class="sxs-lookup"><span data-stu-id="2e27e-117">Requirement</span></span> | <span data-ttu-id="2e27e-118">值</span><span class="sxs-lookup"><span data-stu-id="2e27e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e27e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e27e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2e27e-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e27e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2e27e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e27e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2e27e-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e27e-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2e27e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="2e27e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e27e-124"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e27e-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e27e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e27e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e27e-126">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="2e27e-126">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="2e27e-127">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="2e27e-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="2e27e-128">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="2e27e-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




