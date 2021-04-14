---
description: 這個方法會傳回與影片資料相關聯的裝置。
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: IVideoFrameNative：： GetDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386153"
---
# <a name="ivideoframenativegetdevice-method"></a><span data-ttu-id="18ffe-103">IVideoFrameNative：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="18ffe-103">IVideoFrameNative::GetDevice method</span></span>

<span data-ttu-id="18ffe-104">這個方法會傳回與影片資料相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="18ffe-104">This method returns a device associated with the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ffe-105">語法</span><span class="sxs-lookup"><span data-stu-id="18ffe-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="18ffe-106">參數</span><span class="sxs-lookup"><span data-stu-id="18ffe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ffe-107">*riid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18ffe-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18ffe-108">要取出之裝置的 IID。</span><span class="sxs-lookup"><span data-stu-id="18ffe-108">The IID of the device to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="18ffe-109">*ppv* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="18ffe-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18ffe-110">當此方法成功傳回時，會包含在 *riid* 參數中要求的裝置指標。</span><span class="sxs-lookup"><span data-stu-id="18ffe-110">When this method returns successfully, contains the device pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ffe-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="18ffe-111">Return value</span></span>

<span data-ttu-id="18ffe-112">\_在成功完成時傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="18ffe-112">Returns S\_OK on successful completion.</span></span>

## <a name="see-also"></a><span data-ttu-id="18ffe-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18ffe-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ffe-114">**IVideoFrameNative**</span><span class="sxs-lookup"><span data-stu-id="18ffe-114">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



