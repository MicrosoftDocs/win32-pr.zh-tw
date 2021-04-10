---
description: 定義媒體來源延伸模組的不同就緒狀態。
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: MF_MSE_READY 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849524"
---
# <a name="mf_mse_ready-enumeration"></a><span data-ttu-id="b0847-103">MF \_ MSE \_ 就緒列舉</span><span class="sxs-lookup"><span data-stu-id="b0847-103">MF\_MSE\_READY enumeration</span></span>

<span data-ttu-id="b0847-104">定義媒體來源延伸模組的不同就緒狀態。</span><span class="sxs-lookup"><span data-stu-id="b0847-104">Defines the different ready states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0847-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0847-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a><span data-ttu-id="b0847-106">常數</span><span class="sxs-lookup"><span data-stu-id="b0847-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b0847-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF \_ MSE \_ 就緒 \_ 已關閉**</span><span class="sxs-lookup"><span data-stu-id="b0847-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF\_MSE\_READY\_CLOSED**</span></span>
</dt> <dd>

<span data-ttu-id="b0847-108">媒體來源已關閉。</span><span class="sxs-lookup"><span data-stu-id="b0847-108">The media source is closed.</span></span>

</dd> <dt>

<span data-ttu-id="b0847-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF \_ MSE 已 \_ 就緒 \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="b0847-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF\_MSE\_READY\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="b0847-110">媒體來源已開啟。</span><span class="sxs-lookup"><span data-stu-id="b0847-110">The media source is open.</span></span>

</dd> <dt>

<span data-ttu-id="b0847-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF \_ MSE \_ 就緒已 \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="b0847-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF\_MSE\_READY\_ENDED**</span></span>
</dt> <dd>

<span data-ttu-id="b0847-112">媒體來源已結束。</span><span class="sxs-lookup"><span data-stu-id="b0847-112">The media source is ended.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0847-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0847-113">Requirements</span></span>



| <span data-ttu-id="b0847-114">需求</span><span class="sxs-lookup"><span data-stu-id="b0847-114">Requirement</span></span> | <span data-ttu-id="b0847-115">值</span><span class="sxs-lookup"><span data-stu-id="b0847-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0847-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0847-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b0847-117">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0847-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b0847-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0847-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b0847-119">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0847-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b0847-120">Idl</span><span class="sxs-lookup"><span data-stu-id="b0847-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0847-121"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0847-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0847-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0847-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0847-123">媒體基礎列舉</span><span class="sxs-lookup"><span data-stu-id="b0847-123">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




