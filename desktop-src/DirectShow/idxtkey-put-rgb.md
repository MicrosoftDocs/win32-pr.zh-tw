---
description: Put \_ RGB 方法會指定要做為索引鍵的 rgb 色彩。 只有當索引鍵類型是 DXTKEY RGB 時，才會套用此屬性 \_ 。
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: 'IDxtKey：:p ut_RGB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0b7d282ceb4a693d5a390b8df9b935f0e415d150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977578"
---
# <a name="idxtkeyput_rgb-method"></a><span data-ttu-id="a1fbc-104">IDxtKey：:p ui \_ RGB 方法</span><span class="sxs-lookup"><span data-stu-id="a1fbc-104">IDxtKey::put\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="a1fbc-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="a1fbc-105">\[Deprecated.</span></span> <span data-ttu-id="a1fbc-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="a1fbc-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a1fbc-107">`put_RGB`方法會指定要做為索引鍵的 RGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="a1fbc-107">The `put_RGB` method specifies the RGB color on which to key.</span></span> <span data-ttu-id="a1fbc-108">只有當索引鍵類型是 DXTKEY RGB 時，才會套用此屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a1fbc-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1fbc-109">語法</span><span class="sxs-lookup"><span data-stu-id="a1fbc-109">Syntax</span></span>


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a><span data-ttu-id="a1fbc-110">參數</span><span class="sxs-lookup"><span data-stu-id="a1fbc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1fbc-111">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1fbc-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1fbc-112">使用0xRRGGBB 格式將色彩指定為十六進位數位，其中 RR 是紅色值、GG 為綠色值，而 BB 為藍色值。</span><span class="sxs-lookup"><span data-stu-id="a1fbc-112">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1fbc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1fbc-113">Return value</span></span>

<span data-ttu-id="a1fbc-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a1fbc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a1fbc-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a1fbc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1fbc-116">備註</span><span class="sxs-lookup"><span data-stu-id="a1fbc-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a1fbc-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="a1fbc-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a1fbc-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a1fbc-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a1fbc-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="a1fbc-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1fbc-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1fbc-120">Requirements</span></span>



| <span data-ttu-id="a1fbc-121">需求</span><span class="sxs-lookup"><span data-stu-id="a1fbc-121">Requirement</span></span> | <span data-ttu-id="a1fbc-122">值</span><span class="sxs-lookup"><span data-stu-id="a1fbc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1fbc-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a1fbc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a1fbc-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1fbc-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a1fbc-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1fbc-125">Library</span></span><br/> | <dl> <span data-ttu-id="a1fbc-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1fbc-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1fbc-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1fbc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1fbc-128">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="a1fbc-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="a1fbc-129">**IDxtKey：:p 的 ui \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="a1fbc-129">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




