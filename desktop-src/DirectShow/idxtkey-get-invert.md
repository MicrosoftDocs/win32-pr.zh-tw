---
description: Get \_ 倒轉方法會抓取布林值，指出金鑰作業是否反轉。 這個屬性會套用至 DXTKEY ALPHA 以外的所有索引鍵類型 \_ 。
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'IDxtKey：： get_Invert 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977670"
---
# <a name="idxtkeyget_invert-method"></a><span data-ttu-id="18ffa-104">IDxtKey：：取得 \_ 反轉方法</span><span class="sxs-lookup"><span data-stu-id="18ffa-104">IDxtKey::get\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="18ffa-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="18ffa-105">\[Deprecated.</span></span> <span data-ttu-id="18ffa-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="18ffa-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="18ffa-107">`get_Invert`方法會抓取布林值，指出金鑰作業是否反轉。</span><span class="sxs-lookup"><span data-stu-id="18ffa-107">The `get_Invert` method retrieves a Boolean value indicating whether the key operation is inverted.</span></span> <span data-ttu-id="18ffa-108">這個屬性會套用至 DXTKEY ALPHA 以外的所有索引鍵類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="18ffa-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ffa-109">語法</span><span class="sxs-lookup"><span data-stu-id="18ffa-109">Syntax</span></span>


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="18ffa-110">參數</span><span class="sxs-lookup"><span data-stu-id="18ffa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ffa-111">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="18ffa-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="18ffa-112">接收下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="18ffa-112">Receives one of the following values.</span></span>



| <span data-ttu-id="18ffa-113">值</span><span class="sxs-lookup"><span data-stu-id="18ffa-113">Value</span></span>     | <span data-ttu-id="18ffa-114">描述</span><span class="sxs-lookup"><span data-stu-id="18ffa-114">Description</span></span>                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="18ffa-115">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="18ffa-115">**TRUE**</span></span>  | <span data-ttu-id="18ffa-116">相對於預設作業，會反轉過量影像中的圖元。</span><span class="sxs-lookup"><span data-stu-id="18ffa-116">Pixels in the overlying image are inverted with respect to the default operation.</span></span> |
| <span data-ttu-id="18ffa-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="18ffa-117">**FALSE**</span></span> | <span data-ttu-id="18ffa-118">在上層影像中的圖元會以預設的方式變成透明的。</span><span class="sxs-lookup"><span data-stu-id="18ffa-118">Pixels in the overlying image are made transparent in the default manner.</span></span>         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ffa-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="18ffa-119">Return value</span></span>

<span data-ttu-id="18ffa-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="18ffa-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18ffa-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="18ffa-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18ffa-122">備註</span><span class="sxs-lookup"><span data-stu-id="18ffa-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="18ffa-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="18ffa-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="18ffa-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="18ffa-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="18ffa-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="18ffa-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18ffa-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="18ffa-126">Requirements</span></span>



| <span data-ttu-id="18ffa-127">需求</span><span class="sxs-lookup"><span data-stu-id="18ffa-127">Requirement</span></span> | <span data-ttu-id="18ffa-128">值</span><span class="sxs-lookup"><span data-stu-id="18ffa-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18ffa-129">標頭</span><span class="sxs-lookup"><span data-stu-id="18ffa-129">Header</span></span><br/>  | <dl> <span data-ttu-id="18ffa-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="18ffa-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="18ffa-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="18ffa-131">Library</span></span><br/> | <dl> <span data-ttu-id="18ffa-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="18ffa-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ffa-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18ffa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ffa-134">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="18ffa-134">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="18ffa-135">**IDxtKey：：取得 \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="18ffa-135">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




