---
description: IRenderEngine：： SetSourceConnectCallback 方法-不支援。
ms.assetid: 7da88bab-abba-417c-9e33-c4fc4950536f
title: IRenderEngine：： SetSourceConnectCallback 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceConnectCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: e8fc7dca58f2c1406f575f99d8119edd9bd750d9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084426"
---
# <a name="irenderenginesetsourceconnectcallback-method"></a><span data-ttu-id="aabb0-103">IRenderEngine：： SetSourceConnectCallback 方法</span><span class="sxs-lookup"><span data-stu-id="aabb0-103">IRenderEngine::SetSourceConnectCallback method</span></span>

> [!Note]  
> <span data-ttu-id="aabb0-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="aabb0-104">\[Deprecated.</span></span> <span data-ttu-id="aabb0-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="aabb0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aabb0-106">不支援。</span><span class="sxs-lookup"><span data-stu-id="aabb0-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="aabb0-107">語法</span><span class="sxs-lookup"><span data-stu-id="aabb0-107">Syntax</span></span>


```C++
HRESULT SetSourceConnectCallback(
   IGrfCache *pCallback
);
```



## <a name="parameters"></a><span data-ttu-id="aabb0-108">參數</span><span class="sxs-lookup"><span data-stu-id="aabb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aabb0-109">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="aabb0-109">*pCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="aabb0-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="aabb0-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aabb0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="aabb0-111">Return value</span></span>

<span data-ttu-id="aabb0-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="aabb0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aabb0-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aabb0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aabb0-114">備註</span><span class="sxs-lookup"><span data-stu-id="aabb0-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aabb0-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="aabb0-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aabb0-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="aabb0-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aabb0-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="aabb0-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="aabb0-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aabb0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aabb0-119">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="aabb0-119">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> </dl>

 

 



