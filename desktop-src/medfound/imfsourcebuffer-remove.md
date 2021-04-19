---
description: 從 IMFSourceBuffer 中移除指定時間範圍所定義的媒體區段。
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: IMFSourceBuffer：： Remove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: d82660d08efe651b321672b6ccd0cb475875beee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980724"
---
# <a name="imfsourcebufferremove-method"></a><span data-ttu-id="07d93-103">IMFSourceBuffer：： Remove 方法</span><span class="sxs-lookup"><span data-stu-id="07d93-103">IMFSourceBuffer::Remove method</span></span>

<span data-ttu-id="07d93-104">從 [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)中移除指定時間範圍所定義的媒體區段。</span><span class="sxs-lookup"><span data-stu-id="07d93-104">Removes the media segments defined by the specified time range from the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="07d93-105">語法</span><span class="sxs-lookup"><span data-stu-id="07d93-105">Syntax</span></span>


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a><span data-ttu-id="07d93-106">參數</span><span class="sxs-lookup"><span data-stu-id="07d93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d93-107">*開始* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07d93-107">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d93-108">時間範圍的開始。</span><span class="sxs-lookup"><span data-stu-id="07d93-108">The start of the time range.</span></span>

</dd> <dt>

<span data-ttu-id="07d93-109">*結束* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07d93-109">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d93-110">時間範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="07d93-110">The end of the time range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d93-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="07d93-111">Return value</span></span>

<span data-ttu-id="07d93-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="07d93-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07d93-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="07d93-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d93-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="07d93-114">Requirements</span></span>



| <span data-ttu-id="07d93-115">需求</span><span class="sxs-lookup"><span data-stu-id="07d93-115">Requirement</span></span> | <span data-ttu-id="07d93-116">值</span><span class="sxs-lookup"><span data-stu-id="07d93-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d93-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07d93-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07d93-118">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07d93-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="07d93-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07d93-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07d93-120">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07d93-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="07d93-121">Idl</span><span class="sxs-lookup"><span data-stu-id="07d93-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="07d93-122"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="07d93-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d93-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07d93-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d93-124">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="07d93-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




