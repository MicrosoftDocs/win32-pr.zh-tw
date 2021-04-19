---
description: 取得 \_ 亮度方法會抓取要作為索引鍵的亮度值。 這個屬性只適用于金鑰類型為 DXTKEY \_ 亮度時。
ms.assetid: 92113331-a7b7-4618-81b2-ea02e7bcc923
title: 'IDxtKey：： get_Luminance 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85dcba3720e007d0f3de890c085b0b223e3df350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994245"
---
# <a name="idxtkeyget_luminance-method"></a><span data-ttu-id="65c15-104">IDxtKey：：取得 \_ 亮度方法</span><span class="sxs-lookup"><span data-stu-id="65c15-104">IDxtKey::get\_Luminance method</span></span>

> [!Note]  
> <span data-ttu-id="65c15-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="65c15-105">\[Deprecated.</span></span> <span data-ttu-id="65c15-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="65c15-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="65c15-107">方法會抓取 `get_Luminance` 要做為索引鍵的亮度值。</span><span class="sxs-lookup"><span data-stu-id="65c15-107">The `get_Luminance` method retrieves the luminance value on which to key.</span></span> <span data-ttu-id="65c15-108">這個屬性只適用于金鑰類型為 DXTKEY \_ 亮度時。</span><span class="sxs-lookup"><span data-stu-id="65c15-108">This property applies only when the key type is DXTKEY\_LUMINANCE.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c15-109">語法</span><span class="sxs-lookup"><span data-stu-id="65c15-109">Syntax</span></span>


```C++
HRESULT get_Luminance(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="65c15-110">參數</span><span class="sxs-lookup"><span data-stu-id="65c15-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c15-111">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="65c15-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="65c15-112">接收到索引鍵上的亮度值。</span><span class="sxs-lookup"><span data-stu-id="65c15-112">Receives the luminance value on which to key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c15-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="65c15-113">Return value</span></span>

<span data-ttu-id="65c15-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="65c15-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65c15-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="65c15-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65c15-116">備註</span><span class="sxs-lookup"><span data-stu-id="65c15-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65c15-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="65c15-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="65c15-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="65c15-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="65c15-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="65c15-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65c15-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="65c15-120">Requirements</span></span>



| <span data-ttu-id="65c15-121">需求</span><span class="sxs-lookup"><span data-stu-id="65c15-121">Requirement</span></span> | <span data-ttu-id="65c15-122">值</span><span class="sxs-lookup"><span data-stu-id="65c15-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65c15-123">標頭</span><span class="sxs-lookup"><span data-stu-id="65c15-123">Header</span></span><br/>  | <dl> <span data-ttu-id="65c15-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="65c15-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="65c15-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="65c15-125">Library</span></span><br/> | <dl> <span data-ttu-id="65c15-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="65c15-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65c15-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65c15-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c15-128">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="65c15-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="65c15-129">**IDxtKey：：取得 \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="65c15-129">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




