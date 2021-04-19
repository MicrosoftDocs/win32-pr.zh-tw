---
description: 取得 \_ rgb 方法會抓取用來作為索引鍵的 rgb 色彩。 只有當索引鍵類型是 DXTKEY RGB 時，才會套用此屬性 \_ 。
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'IDxtKey：： get_RGB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ef521b28c232f8247ef38858931ae56be6bf2d25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989769"
---
# <a name="idxtkeyget_rgb-method"></a><span data-ttu-id="86864-104">IDxtKey：： get \_ RGB 方法</span><span class="sxs-lookup"><span data-stu-id="86864-104">IDxtKey::get\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="86864-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="86864-105">\[Deprecated.</span></span> <span data-ttu-id="86864-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="86864-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="86864-107">方法會抓取 `get_RGB` 要作為索引鍵的 RGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="86864-107">The `get_RGB` method retrieves the RGB color on which to key.</span></span> <span data-ttu-id="86864-108">只有當索引鍵類型是 DXTKEY RGB 時，才會套用此屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="86864-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="86864-109">語法</span><span class="sxs-lookup"><span data-stu-id="86864-109">Syntax</span></span>


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="86864-110">參數</span><span class="sxs-lookup"><span data-stu-id="86864-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86864-111">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="86864-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="86864-112">接收色彩。</span><span class="sxs-lookup"><span data-stu-id="86864-112">Receives the color.</span></span> <span data-ttu-id="86864-113">傳回的值是0xRRGGBB 格式的十六進位數位，其中 RR 是紅色值，GG 是綠色值，而 BB 是藍色值。</span><span class="sxs-lookup"><span data-stu-id="86864-113">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86864-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="86864-114">Return value</span></span>

<span data-ttu-id="86864-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="86864-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="86864-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="86864-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="86864-117">備註</span><span class="sxs-lookup"><span data-stu-id="86864-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="86864-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="86864-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="86864-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="86864-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="86864-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="86864-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86864-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="86864-121">Requirements</span></span>



| <span data-ttu-id="86864-122">需求</span><span class="sxs-lookup"><span data-stu-id="86864-122">Requirement</span></span> | <span data-ttu-id="86864-123">值</span><span class="sxs-lookup"><span data-stu-id="86864-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86864-124">標頭</span><span class="sxs-lookup"><span data-stu-id="86864-124">Header</span></span><br/>  | <dl> <span data-ttu-id="86864-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="86864-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="86864-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="86864-126">Library</span></span><br/> | <dl> <span data-ttu-id="86864-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="86864-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86864-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86864-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86864-129">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="86864-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="86864-130">**IDxtKey：：取得 \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="86864-130">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




