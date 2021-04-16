---
description: 中止目前媒體區段的處理。
ms.assetid: 31253d0d-c53f-47bd-823a-fc564cb63b78
title: IMFSourceBuffer：： Abort 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Abort
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 3a8b5115032fb918af66094bb87c7118eb503da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512448"
---
# <a name="imfsourcebufferabort-method"></a><span data-ttu-id="c403c-103">IMFSourceBuffer：： Abort 方法</span><span class="sxs-lookup"><span data-stu-id="c403c-103">IMFSourceBuffer::Abort method</span></span>

<span data-ttu-id="c403c-104">中止目前媒體區段的處理。</span><span class="sxs-lookup"><span data-stu-id="c403c-104">Aborts the processing of the current media segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="c403c-105">語法</span><span class="sxs-lookup"><span data-stu-id="c403c-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="c403c-106">參數</span><span class="sxs-lookup"><span data-stu-id="c403c-106">Parameters</span></span>

<span data-ttu-id="c403c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c403c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c403c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c403c-108">Return value</span></span>

<span data-ttu-id="c403c-109">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c403c-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c403c-110">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c403c-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c403c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c403c-111">Requirements</span></span>



| <span data-ttu-id="c403c-112">需求</span><span class="sxs-lookup"><span data-stu-id="c403c-112">Requirement</span></span> | <span data-ttu-id="c403c-113">值</span><span class="sxs-lookup"><span data-stu-id="c403c-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c403c-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c403c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c403c-115">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c403c-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c403c-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c403c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c403c-117">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c403c-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c403c-118">Idl</span><span class="sxs-lookup"><span data-stu-id="c403c-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c403c-119"><dt>Mfmediaengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c403c-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c403c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c403c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c403c-121">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="c403c-121">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




