---
description: 包含對 D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE 查詢的回應。
ms.assetid: f2e0ae6c-dc97-46f7-933f-6c14d83adf18
title: 'D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b862523c54dc9f483e63cee525dc61c5f469602d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972356"
---
# <a name="d3dauthenticatedchannel_querydevicehandle_output-structure"></a><span data-ttu-id="4ef66-103">D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="4ef66-103">D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT structure</span></span>

<span data-ttu-id="4ef66-104">包含對 [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="4ef66-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) query.</span></span>

<span data-ttu-id="4ef66-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="4ef66-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ef66-106">語法</span><span class="sxs-lookup"><span data-stu-id="4ef66-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="4ef66-107">成員</span><span class="sxs-lookup"><span data-stu-id="4ef66-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ef66-108">**輸出**</span><span class="sxs-lookup"><span data-stu-id="4ef66-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="4ef66-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="4ef66-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="4ef66-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="4ef66-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="4ef66-111">裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4ef66-111">A handle to the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ef66-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ef66-112">Requirements</span></span>



| <span data-ttu-id="4ef66-113">需求</span><span class="sxs-lookup"><span data-stu-id="4ef66-113">Requirement</span></span> | <span data-ttu-id="4ef66-114">值</span><span class="sxs-lookup"><span data-stu-id="4ef66-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef66-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ef66-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4ef66-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ef66-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4ef66-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ef66-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4ef66-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ef66-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4ef66-119">標頭</span><span class="sxs-lookup"><span data-stu-id="4ef66-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ef66-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ef66-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ef66-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ef66-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ef66-122">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="4ef66-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="4ef66-123">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="4ef66-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




