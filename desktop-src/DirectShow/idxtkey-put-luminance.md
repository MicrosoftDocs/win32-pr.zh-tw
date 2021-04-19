---
description: Put \_ 亮度方法會指定要做為索引鍵的亮度值。 這個屬性只適用于金鑰類型為 DXTKEY \_ 亮度時。
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: 'IDxtKey：:p ut_Luminance 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 100f2352b88e9aae2f31ce969302f4bee0905f27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993561"
---
# <a name="idxtkeyput_luminance-method"></a><span data-ttu-id="e9140-104">IDxtKey：:p 的 ui \_ 亮度方法</span><span class="sxs-lookup"><span data-stu-id="e9140-104">IDxtKey::put\_Luminance method</span></span>

> [!Note]  
> <span data-ttu-id="e9140-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="e9140-105">\[Deprecated.</span></span> <span data-ttu-id="e9140-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="e9140-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e9140-107">`put_Luminance`方法會指定要做為索引鍵的亮度值。</span><span class="sxs-lookup"><span data-stu-id="e9140-107">The `put_Luminance` method specifies the luminance value on which to key.</span></span> <span data-ttu-id="e9140-108">這個屬性只適用于金鑰類型為 DXTKEY \_ 亮度時。</span><span class="sxs-lookup"><span data-stu-id="e9140-108">This property applies only when the key type is DXTKEY\_LUMINANCE.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9140-109">語法</span><span class="sxs-lookup"><span data-stu-id="e9140-109">Syntax</span></span>


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e9140-110">參數</span><span class="sxs-lookup"><span data-stu-id="e9140-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9140-111">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9140-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9140-112">要做為索引鍵的亮度值。</span><span class="sxs-lookup"><span data-stu-id="e9140-112">The luminance value on which to key.</span></span> <span data-ttu-id="e9140-113">有效範圍是從0到100。</span><span class="sxs-lookup"><span data-stu-id="e9140-113">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9140-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9140-114">Return value</span></span>

<span data-ttu-id="e9140-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e9140-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9140-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e9140-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9140-117">備註</span><span class="sxs-lookup"><span data-stu-id="e9140-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e9140-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="e9140-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e9140-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e9140-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e9140-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="e9140-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9140-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9140-121">Requirements</span></span>



| <span data-ttu-id="e9140-122">需求</span><span class="sxs-lookup"><span data-stu-id="e9140-122">Requirement</span></span> | <span data-ttu-id="e9140-123">值</span><span class="sxs-lookup"><span data-stu-id="e9140-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9140-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e9140-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e9140-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9140-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e9140-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9140-126">Library</span></span><br/> | <dl> <span data-ttu-id="e9140-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9140-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9140-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9140-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9140-129">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="e9140-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="e9140-130">**IDxtKey：:p 的 ui \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="e9140-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




