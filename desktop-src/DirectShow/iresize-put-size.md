---
description: Put \_ size 方法會設定輸出大小和延展模式。
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: 'IResize：:p ut_Size 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000763"
---
# <a name="iresizeput_size-method"></a><span data-ttu-id="2d680-103">IResize：:p 的內容 \_ 大小方法</span><span class="sxs-lookup"><span data-stu-id="2d680-103">IResize::put\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="2d680-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="2d680-104">\[Deprecated.</span></span> <span data-ttu-id="2d680-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="2d680-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2d680-106">`put_Size`方法會設定輸出大小和延展模式。</span><span class="sxs-lookup"><span data-stu-id="2d680-106">The `put_Size` method sets the output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d680-107">語法</span><span class="sxs-lookup"><span data-stu-id="2d680-107">Syntax</span></span>


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a><span data-ttu-id="2d680-108">參數</span><span class="sxs-lookup"><span data-stu-id="2d680-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d680-109">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d680-109">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d680-110">影片高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2d680-110">The video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2d680-111">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d680-111">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d680-112">影片寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2d680-112">The video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2d680-113">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="2d680-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d680-114">延展模式。</span><span class="sxs-lookup"><span data-stu-id="2d680-114">The stretch mode.</span></span> <span data-ttu-id="2d680-115">請參閱重 [**設大小旗標**](resize-flags.md) 的可能值。</span><span class="sxs-lookup"><span data-stu-id="2d680-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d680-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d680-116">Return value</span></span>

<span data-ttu-id="2d680-117">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2d680-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d680-118">備註</span><span class="sxs-lookup"><span data-stu-id="2d680-118">Remarks</span></span>

<span data-ttu-id="2d680-119">DES 可能會在呼叫 **put \_ 媒體** 之前或之後呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2d680-119">DES may call this method before or after calling **put\_MediaType**.</span></span> <span data-ttu-id="2d680-120">如果 DES 在呼叫 **put \_ 媒體** 之前呼叫這個方法，則篩選應選取位深度的預設值，並使用大小值來建立輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="2d680-120">If DES calls this method before calling **put\_MediaType**, the filter should select a default value for the bit depth and use the size values to construct an output media type.</span></span> <span data-ttu-id="2d680-121">如果 DES 在呼叫 **put \_ 媒體** 之後呼叫這個方法，則篩選器應該使用新的大小來修改其目前的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="2d680-121">If DES calls this method after calling **put\_MediaType**, the filter should modify its current output type with the new sizes.</span></span>

<span data-ttu-id="2d680-122">DES 也可以在輸出連接之後，呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2d680-122">DES may also call this method after the output pin is connected.</span></span> <span data-ttu-id="2d680-123">在這種情況下，請修改輸出類型，然後以新的類型重新連接輸出的 pin。</span><span class="sxs-lookup"><span data-stu-id="2d680-123">In that case, modify the output type and reconnect the output pin with the new type.</span></span> <span data-ttu-id="2d680-124">如需詳細資訊，請參閱重新 [連接 pin](reconnecting-pins.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d680-124">See [Reconnecting Pins](reconnecting-pins.md) for more information.</span></span>

<span data-ttu-id="2d680-125">*Flags* 參數會指定篩選應如何執行調整大小作業。</span><span class="sxs-lookup"><span data-stu-id="2d680-125">The *Flags* parameter specifies how the filter should perform the resizing operation.</span></span>

> [!Note]  
> <span data-ttu-id="2d680-126">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="2d680-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2d680-127">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2d680-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2d680-128">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="2d680-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d680-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d680-129">Requirements</span></span>



| <span data-ttu-id="2d680-130">需求</span><span class="sxs-lookup"><span data-stu-id="2d680-130">Requirement</span></span> | <span data-ttu-id="2d680-131">值</span><span class="sxs-lookup"><span data-stu-id="2d680-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d680-132">版本</span><span class="sxs-lookup"><span data-stu-id="2d680-132">Version</span></span><br/> | <span data-ttu-id="2d680-133">DirectX 9.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2d680-133">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="2d680-134">標頭</span><span class="sxs-lookup"><span data-stu-id="2d680-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2d680-135"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d680-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2d680-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="2d680-136">Library</span></span><br/> | <dl> <span data-ttu-id="2d680-137"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d680-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d680-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d680-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d680-139">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2d680-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="2d680-140">**IResize 介面**</span><span class="sxs-lookup"><span data-stu-id="2d680-140">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




