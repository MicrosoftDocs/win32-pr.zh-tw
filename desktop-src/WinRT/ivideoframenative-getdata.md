---
description: 這個方法會傳回提供影片資料存取權的介面。
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: IVideoFrameNative：：：：的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943429"
---
# <a name="ivideoframenativegetdata-method"></a><span data-ttu-id="8068b-103">IVideoFrameNative：：：：的方法</span><span class="sxs-lookup"><span data-stu-id="8068b-103">IVideoFrameNative::GetData method</span></span>

<span data-ttu-id="8068b-104">這個方法會傳回提供影片資料存取權的介面。</span><span class="sxs-lookup"><span data-stu-id="8068b-104">This method returns an interface that provides access to the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8068b-105">語法</span><span class="sxs-lookup"><span data-stu-id="8068b-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="8068b-106">參數</span><span class="sxs-lookup"><span data-stu-id="8068b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8068b-107">*riid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8068b-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8068b-108">要取出之介面的 IID。</span><span class="sxs-lookup"><span data-stu-id="8068b-108">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="8068b-109">*ppv* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8068b-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8068b-110">當這個方法成功傳回時，會包含在 *riid* 參數中要求的介面指標。</span><span class="sxs-lookup"><span data-stu-id="8068b-110">When this method returns successfully, contains the interface pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8068b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8068b-111">Return value</span></span>

<span data-ttu-id="8068b-112">\_在成功完成時傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="8068b-112">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="8068b-113">\_如果找不到要求的介面，則傳回 E NOINTERFACE。</span><span class="sxs-lookup"><span data-stu-id="8068b-113">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="8068b-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8068b-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8068b-115">**IVideoFrameNative**</span><span class="sxs-lookup"><span data-stu-id="8068b-115">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



