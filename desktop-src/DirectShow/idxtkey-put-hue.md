---
description: Put \_ 色調方法會指定要做為索引鍵的色調值。 這個屬性只適用于索引鍵類型為 DXTKEY 的 \_ 色調。
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: 'IDxtKey：:p ut_Hue 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9d2b08f3e805edc8b8860495fc105f0cfdf6768f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994033"
---
# <a name="idxtkeyput_hue-method"></a><span data-ttu-id="0d53a-104">IDxtKey：:p 的 ui \_ 色調方法</span><span class="sxs-lookup"><span data-stu-id="0d53a-104">IDxtKey::put\_Hue method</span></span>

> [!Note]  
> <span data-ttu-id="0d53a-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="0d53a-105">\[Deprecated.</span></span> <span data-ttu-id="0d53a-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="0d53a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0d53a-107">`put_Hue`方法會指定要做為索引鍵的色調值。</span><span class="sxs-lookup"><span data-stu-id="0d53a-107">The `put_Hue` method specifies the hue value on which to key.</span></span> <span data-ttu-id="0d53a-108">這個屬性只適用于索引鍵類型為 DXTKEY 的 \_ 色調。</span><span class="sxs-lookup"><span data-stu-id="0d53a-108">This property applies only when the key type is DXTKEY\_HUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d53a-109">語法</span><span class="sxs-lookup"><span data-stu-id="0d53a-109">Syntax</span></span>


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="0d53a-110">參數</span><span class="sxs-lookup"><span data-stu-id="0d53a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d53a-111">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d53a-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d53a-112">要做為索引鍵的色調值。</span><span class="sxs-lookup"><span data-stu-id="0d53a-112">The hue value on which to key.</span></span> <span data-ttu-id="0d53a-113">有效範圍是從0到360。</span><span class="sxs-lookup"><span data-stu-id="0d53a-113">The valid range is from 0 to 360.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d53a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d53a-114">Return value</span></span>

<span data-ttu-id="0d53a-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0d53a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d53a-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0d53a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d53a-117">備註</span><span class="sxs-lookup"><span data-stu-id="0d53a-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0d53a-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="0d53a-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0d53a-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0d53a-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0d53a-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="0d53a-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d53a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d53a-121">Requirements</span></span>



| <span data-ttu-id="0d53a-122">需求</span><span class="sxs-lookup"><span data-stu-id="0d53a-122">Requirement</span></span> | <span data-ttu-id="0d53a-123">值</span><span class="sxs-lookup"><span data-stu-id="0d53a-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d53a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0d53a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0d53a-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d53a-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0d53a-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="0d53a-126">Library</span></span><br/> | <dl> <span data-ttu-id="0d53a-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d53a-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d53a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d53a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d53a-129">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="0d53a-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="0d53a-130">**IDxtKey：:p 的 ui \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="0d53a-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




