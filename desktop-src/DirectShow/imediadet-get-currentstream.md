---
description: Get CurrentStream 方法會抓取媒體偵測器 \_ 目前使用的資料流程號碼。
ms.assetid: 0f590498-e639-4b6b-be1d-f1e4a36282cb
title: 'IMediaDet：： get_CurrentStream 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e664e88862a6bc124a88ac23cedf29e687d51e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995755"
---
# <a name="imediadetget_currentstream-method"></a><span data-ttu-id="2c240-103">IMediaDet：： get \_ CurrentStream 方法</span><span class="sxs-lookup"><span data-stu-id="2c240-103">IMediaDet::get\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="2c240-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="2c240-104">\[Deprecated.</span></span> <span data-ttu-id="2c240-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="2c240-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2c240-106">方法會抓取媒體偵測器 `get_CurrentStream` 目前使用的資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="2c240-106">The `get_CurrentStream` method retrieves the stream number currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c240-107">語法</span><span class="sxs-lookup"><span data-stu-id="2c240-107">Syntax</span></span>


```C++
HRESULT get_CurrentStream(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="2c240-108">參數</span><span class="sxs-lookup"><span data-stu-id="2c240-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c240-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="2c240-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2c240-110">接收目前的資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="2c240-110">Receives the current stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c240-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c240-111">Return value</span></span>

<span data-ttu-id="2c240-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2c240-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2c240-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c240-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c240-114">備註</span><span class="sxs-lookup"><span data-stu-id="2c240-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2c240-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="2c240-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2c240-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2c240-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2c240-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="2c240-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c240-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c240-118">Requirements</span></span>



| <span data-ttu-id="2c240-119">需求</span><span class="sxs-lookup"><span data-stu-id="2c240-119">Requirement</span></span> | <span data-ttu-id="2c240-120">值</span><span class="sxs-lookup"><span data-stu-id="2c240-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c240-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2c240-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2c240-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c240-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2c240-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="2c240-123">Library</span></span><br/> | <dl> <span data-ttu-id="2c240-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c240-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c240-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c240-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c240-126">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="2c240-126">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="2c240-127">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2c240-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




