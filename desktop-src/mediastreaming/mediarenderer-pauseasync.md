---
title: MediaRenderer. PauseAsync 方法
description: 指示 DMR 以非同步方式暫停播放目前的內容。 |MediaRenderer. PauseAsync 方法
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- PauseAsync 方法媒體串流 API
- PauseAsync 方法媒體串流 API，MediaRenderer 介面
- MediaRenderer 介面媒體串流 API，PauseAsync 方法
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974820"
---
# <a name="mediarendererpauseasync-method"></a><span data-ttu-id="9a7ac-107">MediaRenderer. PauseAsync 方法</span><span class="sxs-lookup"><span data-stu-id="9a7ac-107">MediaRenderer.PauseAsync method</span></span>

<span data-ttu-id="9a7ac-108">指示 DMR 以非同步方式暫停播放目前的內容。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7ac-109">語法</span><span class="sxs-lookup"><span data-stu-id="9a7ac-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="9a7ac-110">參數</span><span class="sxs-lookup"><span data-stu-id="9a7ac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a7ac-111">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9a7ac-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7ac-112">接收 [**PlaybackOperation**](playbackoperation.md) 物件的參考，這個物件是用來從非同步作業取得結果。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a7ac-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a7ac-113">Return value</span></span>

<span data-ttu-id="9a7ac-114">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9a7ac-115">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9a7ac-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9a7ac-116">Return code</span></span>                                                                          | <span data-ttu-id="9a7ac-117">Description</span><span class="sxs-lookup"><span data-stu-id="9a7ac-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9a7ac-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9a7ac-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9a7ac-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="9a7ac-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9a7ac-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a7ac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7ac-121">**MediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="9a7ac-121">**MediaRenderer**</span></span>](mediarenderer.md)
</dt> </dl>

 

 





