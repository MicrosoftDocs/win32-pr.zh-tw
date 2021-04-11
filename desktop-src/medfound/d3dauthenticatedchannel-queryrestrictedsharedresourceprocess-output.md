---
description: 包含對 D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS 查詢的回應。
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: 'D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bd93e1cadb7da500a82218924044af79fbb1f493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111809"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a><span data-ttu-id="9d57c-103">D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ 輸出結構</span><span class="sxs-lookup"><span data-stu-id="9d57c-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT structure</span></span>

<span data-ttu-id="9d57c-104">包含對 [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) 查詢的回應。</span><span class="sxs-lookup"><span data-stu-id="9d57c-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="9d57c-105">若要傳送此查詢，請呼叫 [**IDirect3DAuthenticatedChannel9：： query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)。</span><span class="sxs-lookup"><span data-stu-id="9d57c-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d57c-106">語法</span><span class="sxs-lookup"><span data-stu-id="9d57c-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT          Output;
  UINT                                          ProcessIndex;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentifer;
  HANDLE                                        ProcessHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="9d57c-107">成員</span><span class="sxs-lookup"><span data-stu-id="9d57c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d57c-108">**輸出**</span><span class="sxs-lookup"><span data-stu-id="9d57c-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="9d57c-109">包含訊息驗證碼 (MAC) 和其他資料的 [**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸出**](d3dauthenticatedchannel-query-output.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="9d57c-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="9d57c-110">**ProcessIndex**</span><span class="sxs-lookup"><span data-stu-id="9d57c-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="9d57c-111">進程清單中進程的索引。</span><span class="sxs-lookup"><span data-stu-id="9d57c-111">The index of the process in the list of processes.</span></span>

</dd> <dt>

<span data-ttu-id="9d57c-112">**ProcessIdentifer**</span><span class="sxs-lookup"><span data-stu-id="9d57c-112">**ProcessIdentifer**</span></span>
</dt> <dd>

<span data-ttu-id="9d57c-113">指定進程類型的 [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) 值。</span><span class="sxs-lookup"><span data-stu-id="9d57c-113">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span>

</dd> <dt>

<span data-ttu-id="9d57c-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="9d57c-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="9d57c-115">進程控制碼。</span><span class="sxs-lookup"><span data-stu-id="9d57c-115">A process handle.</span></span> <span data-ttu-id="9d57c-116">如果 **ProcessIdentifier** 成員等於 **PROCESSIDTYPE \_ 控制碼**， **ProcessHandle** 成員就會包含有效的進程控制碼。</span><span class="sxs-lookup"><span data-stu-id="9d57c-116">If the **ProcessIdentifier** member equals **PROCESSIDTYPE\_HANDLE**, the **ProcessHandle** member contains a valid handle to a process.</span></span> <span data-ttu-id="9d57c-117">否則，會忽略這個成員。</span><span class="sxs-lookup"><span data-stu-id="9d57c-117">Otherwise, this member is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d57c-118">備註</span><span class="sxs-lookup"><span data-stu-id="9d57c-118">Remarks</span></span>

<span data-ttu-id="9d57c-119">桌面視窗管理員 (DWM) 進程是藉由設定等於 **PROCESSIDTYPE \_ Dwm** 的 **ProcessIdentifier** 來識別。</span><span class="sxs-lookup"><span data-stu-id="9d57c-119">The Desktop Window Manager (DWM) process is identified by setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="9d57c-120">其他進程的識別方式是在 **ProcessHandle** 中設定進程控制碼，並設定 **ProcessIdentifier** 等於 **PROCESSIDTYPE \_ 控制碼**。</span><span class="sxs-lookup"><span data-stu-id="9d57c-120">Other processes are identified by setting the process handle in **ProcessHandle** and setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_HANDLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d57c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d57c-121">Requirements</span></span>



| <span data-ttu-id="9d57c-122">需求</span><span class="sxs-lookup"><span data-stu-id="9d57c-122">Requirement</span></span> | <span data-ttu-id="9d57c-123">值</span><span class="sxs-lookup"><span data-stu-id="9d57c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d57c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d57c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9d57c-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d57c-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9d57c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d57c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9d57c-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d57c-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9d57c-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9d57c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d57c-129"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d57c-129"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d57c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d57c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d57c-131">Direct3D 影片結構</span><span class="sxs-lookup"><span data-stu-id="9d57c-131">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="9d57c-132">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="9d57c-132">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




