---
description: Put \_ 倒轉方法會指定是否反轉索引鍵作業。 這個屬性會套用至 DXTKEY ALPHA 以外的所有索引鍵類型 \_ 。
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: 'IDxtKey：:p ut_Invert 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3e4b807770d0eeb985c982b61b8390695cc42327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001882"
---
# <a name="idxtkeyput_invert-method"></a><span data-ttu-id="a9296-104">IDxtKey：:p 的 ui \_ 反轉方法</span><span class="sxs-lookup"><span data-stu-id="a9296-104">IDxtKey::put\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="a9296-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="a9296-105">\[Deprecated.</span></span> <span data-ttu-id="a9296-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="a9296-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a9296-107">`put_Invert`方法會指定金鑰作業是否反轉。</span><span class="sxs-lookup"><span data-stu-id="a9296-107">The `put_Invert` method specifies whether the key operation is inverted.</span></span> <span data-ttu-id="a9296-108">這個屬性會套用至 DXTKEY ALPHA 以外的所有索引鍵類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a9296-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9296-109">語法</span><span class="sxs-lookup"><span data-stu-id="a9296-109">Syntax</span></span>


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="a9296-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9296-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9296-111">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9296-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9296-112">指定布林值。</span><span class="sxs-lookup"><span data-stu-id="a9296-112">Specifies a Boolean value.</span></span> <span data-ttu-id="a9296-113">若 **為 TRUE**，則會根據預設作業反轉過量影像中的圖元。</span><span class="sxs-lookup"><span data-stu-id="a9296-113">If **TRUE**, pixels in the overlying image are inverted with respect to the default operation.</span></span> <span data-ttu-id="a9296-114">如果 **為 FALSE**，則會以預設方式將上層影像中的圖元變成透明。</span><span class="sxs-lookup"><span data-stu-id="a9296-114">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9296-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9296-115">Return value</span></span>

<span data-ttu-id="a9296-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a9296-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9296-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a9296-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9296-118">備註</span><span class="sxs-lookup"><span data-stu-id="a9296-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a9296-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="a9296-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a9296-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a9296-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a9296-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="a9296-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a9296-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9296-122">Requirements</span></span>



| <span data-ttu-id="a9296-123">需求</span><span class="sxs-lookup"><span data-stu-id="a9296-123">Requirement</span></span> | <span data-ttu-id="a9296-124">值</span><span class="sxs-lookup"><span data-stu-id="a9296-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9296-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a9296-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a9296-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="a9296-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a9296-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9296-127">Library</span></span><br/> | <dl> <span data-ttu-id="a9296-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9296-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9296-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9296-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9296-130">**IDxtKey 介面**</span><span class="sxs-lookup"><span data-stu-id="a9296-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="a9296-131">**IDxtKey：:p 的 ui \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="a9296-131">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




