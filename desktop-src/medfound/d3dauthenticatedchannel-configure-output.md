---
description: 包含對 IDirect3DAuthenticatedChannel9：： Configure 方法之呼叫的回應。
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: 'D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317991"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a><span data-ttu-id="88ae5-103">D3DAUTHENTICATEDCHANNEL \_ 設定 \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="88ae5-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_OUTPUT structure</span></span>

<span data-ttu-id="88ae5-104">包含對 [**IDirect3DAuthenticatedChannel9：： Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) 方法之呼叫的回應。</span><span class="sxs-lookup"><span data-stu-id="88ae5-104">Contains the response to a call to the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ae5-105">語法</span><span class="sxs-lookup"><span data-stu-id="88ae5-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="88ae5-106">成員</span><span class="sxs-lookup"><span data-stu-id="88ae5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="88ae5-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="88ae5-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="88ae5-108">[**D3D \_ OMAC**](d3d-omac.md)結構，其中包含資料的訊息驗證碼 (MAC) 。</span><span class="sxs-lookup"><span data-stu-id="88ae5-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="88ae5-109">驅動程式會使用 AES 型單鍵 CBC MAC (OMAC) 為此結構成員後面出現的資料區塊計算此值。</span><span class="sxs-lookup"><span data-stu-id="88ae5-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="88ae5-110">**ConfigureType**</span><span class="sxs-lookup"><span data-stu-id="88ae5-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="88ae5-111">指定命令的 GUID。</span><span class="sxs-lookup"><span data-stu-id="88ae5-111">A GUID that specifies the command.</span></span> <span data-ttu-id="88ae5-112">如需值的清單，請參閱 [內容保護命令](content-protection-commands.md)。</span><span class="sxs-lookup"><span data-stu-id="88ae5-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ae5-113">**hChannel**</span><span class="sxs-lookup"><span data-stu-id="88ae5-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="88ae5-114">已驗證通道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="88ae5-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="88ae5-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="88ae5-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="88ae5-116">命令的序號。</span><span class="sxs-lookup"><span data-stu-id="88ae5-116">The command sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="88ae5-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="88ae5-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="88ae5-118">命令的結果碼。</span><span class="sxs-lookup"><span data-stu-id="88ae5-118">The result code for the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88ae5-119">備註</span><span class="sxs-lookup"><span data-stu-id="88ae5-119">Remarks</span></span>

<span data-ttu-id="88ae5-120">針對 **ConfigureType**、 **hChannel** 和 **SequenceNumber** 成員，驅動程式會使用 [**D3DAUTHENTICATEDCHANNEL \_ 設定 \_ 輸入**](d3dauthenticatedchannel-configure-input.md) 結構中所提供的相同值。</span><span class="sxs-lookup"><span data-stu-id="88ae5-120">For the **ConfigureType**, **hChannel**, and **SequenceNumber** members, the driver uses the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure.</span></span> <span data-ttu-id="88ae5-121">應用程式應該驗證這些值是否相符。</span><span class="sxs-lookup"><span data-stu-id="88ae5-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ae5-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="88ae5-122">Requirements</span></span>



| <span data-ttu-id="88ae5-123">需求</span><span class="sxs-lookup"><span data-stu-id="88ae5-123">Requirement</span></span> | <span data-ttu-id="88ae5-124">值</span><span class="sxs-lookup"><span data-stu-id="88ae5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88ae5-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88ae5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="88ae5-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88ae5-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="88ae5-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88ae5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="88ae5-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88ae5-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="88ae5-129">標頭</span><span class="sxs-lookup"><span data-stu-id="88ae5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="88ae5-130"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="88ae5-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ae5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88ae5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ae5-132">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="88ae5-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="88ae5-133">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="88ae5-133">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




