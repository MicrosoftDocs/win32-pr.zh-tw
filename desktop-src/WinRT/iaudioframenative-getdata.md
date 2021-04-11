---
description: 這個方法會傳回提供音訊資料存取權的介面。
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: IAudioFrameNative：：：：的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113121"
---
# <a name="iaudioframenativegetdata-method"></a><span data-ttu-id="c2733-103">IAudioFrameNative：：：：的方法</span><span class="sxs-lookup"><span data-stu-id="c2733-103">IAudioFrameNative::GetData method</span></span>

<span data-ttu-id="c2733-104">這個方法會傳回提供音訊資料存取權的介面。</span><span class="sxs-lookup"><span data-stu-id="c2733-104">This method returns an interface that provides access to the audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2733-105">語法</span><span class="sxs-lookup"><span data-stu-id="c2733-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="c2733-106">參數</span><span class="sxs-lookup"><span data-stu-id="c2733-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2733-107">*riid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2733-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2733-108">類型： **REFIID**</span><span class="sxs-lookup"><span data-stu-id="c2733-108">Type: **REFIID**</span></span>

<span data-ttu-id="c2733-109">要取出之介面的 IID。</span><span class="sxs-lookup"><span data-stu-id="c2733-109">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c2733-110">*ppv* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c2733-110">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2733-111">類型： \**LPVOID \** _</span><span class="sxs-lookup"><span data-stu-id="c2733-111">Type: \**LPVOID\** _</span></span>

<span data-ttu-id="c2733-112">當這個方法成功傳回時，會包含 _riid \* 參數中要求的介面指標。</span><span class="sxs-lookup"><span data-stu-id="c2733-112">When this method returns successfully, contains the interface pointer requested in _riid\* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2733-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2733-113">Return value</span></span>

<span data-ttu-id="c2733-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c2733-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c2733-115">\_在成功完成時傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="c2733-115">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="c2733-116">\_如果找不到要求的介面，則傳回 E NOINTERFACE。</span><span class="sxs-lookup"><span data-stu-id="c2733-116">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2733-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2733-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2733-118">**IAudioFrameNative**</span><span class="sxs-lookup"><span data-stu-id="c2733-118">**IAudioFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



