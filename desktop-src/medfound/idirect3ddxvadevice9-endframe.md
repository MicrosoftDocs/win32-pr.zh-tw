---
description: 結束處理以建立解碼的圖片。
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'IDirect3DDXVADevice9：： EndFrame 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114228"
---
# <a name="idirect3ddxvadevice9endframe-method"></a><span data-ttu-id="0b3ce-103">IDirect3DDXVADevice9：： EndFrame 方法</span><span class="sxs-lookup"><span data-stu-id="0b3ce-103">IDirect3DDXVADevice9::EndFrame method</span></span>

<span data-ttu-id="0b3ce-104">結束處理以建立解碼的圖片。</span><span class="sxs-lookup"><span data-stu-id="0b3ce-104">Ends the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b3ce-105">語法</span><span class="sxs-lookup"><span data-stu-id="0b3ce-105">Syntax</span></span>


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a><span data-ttu-id="0b3ce-106">參數</span><span class="sxs-lookup"><span data-stu-id="0b3ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b3ce-107">*SizeMiscData*</span><span class="sxs-lookup"><span data-stu-id="0b3ce-107">*SizeMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3ce-108">*PMiscData* 所指定的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0b3ce-108">The size of the buffer specified by *pMiscData*, in bytes.</span></span> <span data-ttu-id="0b3ce-109">值必須是2。</span><span class="sxs-lookup"><span data-stu-id="0b3ce-109">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="0b3ce-110">*pMiscData*</span><span class="sxs-lookup"><span data-stu-id="0b3ce-110">*pMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="0b3ce-111">包含影片加速器資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="0b3ce-111">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="0b3ce-112">這個緩衝區必須包含在 *pInputData* 參數中傳遞給 [**IDirect3DDXVADevice9：： BeginFrame**](idirect3ddxvadevice9-beginframe.md)方法的相同框架索引。</span><span class="sxs-lookup"><span data-stu-id="0b3ce-112">This buffer must contain the same frame index that was passed to the [**IDirect3DDXVADevice9::BeginFrame**](idirect3ddxvadevice9-beginframe.md) method in the *pInputData* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b3ce-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b3ce-113">Return value</span></span>

<span data-ttu-id="0b3ce-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0b3ce-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0b3ce-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0b3ce-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b3ce-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b3ce-116">Requirements</span></span>



| <span data-ttu-id="0b3ce-117">需求</span><span class="sxs-lookup"><span data-stu-id="0b3ce-117">Requirement</span></span> | <span data-ttu-id="0b3ce-118">值</span><span class="sxs-lookup"><span data-stu-id="0b3ce-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0b3ce-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b3ce-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b3ce-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b3ce-120">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0b3ce-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b3ce-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b3ce-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0b3ce-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0b3ce-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0b3ce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b3ce-124"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="0b3ce-124"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b3ce-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b3ce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b3ce-126">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="0b3ce-126">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




