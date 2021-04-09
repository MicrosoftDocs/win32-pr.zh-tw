---
description: 包含對 D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE 查詢的回應。
ms.assetid: 66735ce3-c16b-4eca-9283-5d3bc37d73d3
title: 'D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cfc0075678163b273acad72fa1724cbca8a29cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111808"
---
# <a name="d3dauthenticatedchannel_queryuncompressedencryptionlevel_output-structure"></a><span data-ttu-id="cb3ff-103">D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="cb3ff-103">D3DAUTHENTICATEDCHANNEL\_QUERYUNCOMPRESSEDENCRYPTIONLEVEL\_OUTPUT structure</span></span>

<span data-ttu-id="cb3ff-104">包含對 [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="cb3ff-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) query.</span></span>

<span data-ttu-id="cb3ff-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="cb3ff-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3ff-106">語法</span><span class="sxs-lookup"><span data-stu-id="cb3ff-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  GUID                                 EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYUNCOMPRESSEDENCRYPTIONLEVEL_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="cb3ff-107">成員</span><span class="sxs-lookup"><span data-stu-id="cb3ff-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cb3ff-108">**輸出**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="cb3ff-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="cb3ff-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="cb3ff-110">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-110">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="cb3ff-111">指定目前加密類型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="cb3ff-111">A GUID that specifies the current encryption type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb3ff-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb3ff-112">Requirements</span></span>



| <span data-ttu-id="cb3ff-113">需求</span><span class="sxs-lookup"><span data-stu-id="cb3ff-113">Requirement</span></span> | <span data-ttu-id="cb3ff-114">值</span><span class="sxs-lookup"><span data-stu-id="cb3ff-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3ff-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb3ff-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cb3ff-116">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb3ff-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cb3ff-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb3ff-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cb3ff-118">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb3ff-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cb3ff-119">標頭</span><span class="sxs-lookup"><span data-stu-id="cb3ff-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb3ff-120"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb3ff-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb3ff-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb3ff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3ff-122">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="cb3ff-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="cb3ff-123">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="cb3ff-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




