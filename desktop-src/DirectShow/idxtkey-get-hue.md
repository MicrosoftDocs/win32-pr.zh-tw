---
description: 「取得 \_ 色調」方法會抓取要做為索引鍵的色調值。 這個屬性只適用于索引鍵類型為 DXTKEY 的 \_ 色調。
ms.assetid: d37fedd6-f29f-4f16-821b-c5f8520c4e12
title: 'IDxtKey：： get_Hue 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72058076e87f1a8738f3153ee8095eefb4ebce8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994658"
---
# <a name="idxtkeyget_hue-method"></a><span data-ttu-id="d4891-104">IDxtKey：： get \_ 色調方法</span><span class="sxs-lookup"><span data-stu-id="d4891-104">IDxtKey::get\_Hue method</span></span>

> [!Note]  
> <span data-ttu-id="d4891-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d4891-105">\[Deprecated.</span></span> <span data-ttu-id="d4891-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d4891-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d4891-107">方法會抓取 `get_Hue` 要做為索引鍵的色調值。</span><span class="sxs-lookup"><span data-stu-id="d4891-107">The `get_Hue` method retrieves the hue value on which to key.</span></span> <span data-ttu-id="d4891-108">這個屬性只適用于索引鍵類型為 DXTKEY 的 \_ 色調。</span><span class="sxs-lookup"><span data-stu-id="d4891-108">This property applies only when the key type is DXTKEY\_HUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4891-109">語法</span><span class="sxs-lookup"><span data-stu-id="d4891-109">Syntax</span></span>


```C++
HRESULT get_Hue(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d4891-110">參數</span><span class="sxs-lookup"><span data-stu-id="d4891-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4891-111">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="d4891-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d4891-112">接收到索引鍵上的色調值。</span><span class="sxs-lookup"><span data-stu-id="d4891-112">Receives the hue value on which to key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4891-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4891-113">Return value</span></span>

<span data-ttu-id="d4891-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d4891-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d4891-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d4891-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4891-116">備註</span><span class="sxs-lookup"><span data-stu-id="d4891-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d4891-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d4891-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d4891-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d4891-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d4891-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d4891-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d4891-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4891-120">Requirements</span></span>



| <span data-ttu-id="d4891-121">需求</span><span class="sxs-lookup"><span data-stu-id="d4891-121">Requirement</span></span> | <span data-ttu-id="d4891-122">值</span><span class="sxs-lookup"><span data-stu-id="d4891-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4891-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d4891-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d4891-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4891-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d4891-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4891-125">Library</span></span><br/> | <dl> <span data-ttu-id="d4891-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4891-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4891-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4891-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4891-128">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="d4891-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="d4891-129">**IDxtKey：：取得 \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="d4891-129">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




