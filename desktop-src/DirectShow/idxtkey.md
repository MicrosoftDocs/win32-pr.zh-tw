---
description: IDxtKey 介面會設定金鑰轉換的屬性。當 DirectShow 編輯服務在轉譯金鑰轉換時 (DES) ，會在內部使用此介面。
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: 'IDxtKey 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983057"
---
# <a name="idxtkey-interface"></a><span data-ttu-id="feeb3-103">IDxtKey 介面</span><span class="sxs-lookup"><span data-stu-id="feeb3-103">IDxtKey interface</span></span>

> [!Note]  
> <span data-ttu-id="feeb3-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="feeb3-104">\[Deprecated.</span></span> <span data-ttu-id="feeb3-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="feeb3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="feeb3-106">`IDxtKey`介面會設定[金鑰](key-transition.md)轉換的屬性。</span><span class="sxs-lookup"><span data-stu-id="feeb3-106">The `IDxtKey` interface sets properties on the [Key](key-transition.md) transition.</span></span>

<span data-ttu-id="feeb3-107">當 DirectShow 編輯服務在轉譯金鑰轉換時 (DES) ，會在內部使用此介面。</span><span class="sxs-lookup"><span data-stu-id="feeb3-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Key transition.</span></span> <span data-ttu-id="feeb3-108">DES 應用程式不需要使用此介面。</span><span class="sxs-lookup"><span data-stu-id="feeb3-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="feeb3-109">若要在 DES 的轉換上設定屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="feeb3-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="feeb3-110">成員</span><span class="sxs-lookup"><span data-stu-id="feeb3-110">Members</span></span>

<span data-ttu-id="feeb3-111">**IDxtKey** 介面繼承自 **IDXEffect**。</span><span class="sxs-lookup"><span data-stu-id="feeb3-111">The **IDxtKey** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="feeb3-112">**IDxtKey** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="feeb3-112">**IDxtKey** also has these types of members:</span></span>

-   [<span data-ttu-id="feeb3-113">方法</span><span class="sxs-lookup"><span data-stu-id="feeb3-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="feeb3-114">方法</span><span class="sxs-lookup"><span data-stu-id="feeb3-114">Methods</span></span>

<span data-ttu-id="feeb3-115">**IDxtKey** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="feeb3-115">The **IDxtKey** interface has these methods.</span></span>



| <span data-ttu-id="feeb3-116">方法</span><span class="sxs-lookup"><span data-stu-id="feeb3-116">Method</span></span>                                            | <span data-ttu-id="feeb3-117">描述</span><span class="sxs-lookup"><span data-stu-id="feeb3-117">Description</span></span>                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="feeb3-118">**取得 \_ 色調**</span><span class="sxs-lookup"><span data-stu-id="feeb3-118">**get\_Hue**</span></span>](idxtkey-get-hue.md)               | <span data-ttu-id="feeb3-119">抓取要做為索引鍵的色調值。</span><span class="sxs-lookup"><span data-stu-id="feeb3-119">Retrieves the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="feeb3-120">**取得 \_ 反轉**</span><span class="sxs-lookup"><span data-stu-id="feeb3-120">**get\_Invert**</span></span>](idxtkey-get-invert.md)         | <span data-ttu-id="feeb3-121">抓取布林值，指出金鑰作業是否反轉。</span><span class="sxs-lookup"><span data-stu-id="feeb3-121">Retrieves a Boolean value indicating whether the key operation is inverted.</span></span><br/> |
| [<span data-ttu-id="feeb3-122">**取得 \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="feeb3-122">**get\_KeyType**</span></span>](idxtkey-get-keytype.md)       | <span data-ttu-id="feeb3-123">捕獲索引鍵的類型。</span><span class="sxs-lookup"><span data-stu-id="feeb3-123">Retrieves the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="feeb3-124">**取得 \_ 亮度**</span><span class="sxs-lookup"><span data-stu-id="feeb3-124">**get\_Luminance**</span></span>](idxtkey-get-luminance.md)   | <span data-ttu-id="feeb3-125">抓取要作為索引鍵的亮度值。</span><span class="sxs-lookup"><span data-stu-id="feeb3-125">Retrieves the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="feeb3-126">**取得 \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="feeb3-126">**get\_RGB**</span></span>](idxtkey-get-rgb.md)               | <span data-ttu-id="feeb3-127">抓取要作為索引鍵的 RGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="feeb3-127">Retrieves the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="feeb3-128">**取得 \_ 相似性**</span><span class="sxs-lookup"><span data-stu-id="feeb3-128">**get\_Similarity**</span></span>](idxtkey-get-similarity.md) | <span data-ttu-id="feeb3-129">抓取變成透明的色彩資料範圍。</span><span class="sxs-lookup"><span data-stu-id="feeb3-129">Retrieves the range of color data that becomes transparent.</span></span><br/>                 |
| [<span data-ttu-id="feeb3-130">**put \_ 色調**</span><span class="sxs-lookup"><span data-stu-id="feeb3-130">**put\_Hue**</span></span>](idxtkey-put-hue.md)               | <span data-ttu-id="feeb3-131">指定要做為索引鍵的色調值。</span><span class="sxs-lookup"><span data-stu-id="feeb3-131">Specifies the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="feeb3-132">**put \_ 反轉**</span><span class="sxs-lookup"><span data-stu-id="feeb3-132">**put\_Invert**</span></span>](idxtkey-put-invert.md)         | <span data-ttu-id="feeb3-133">指定索引鍵作業是否反轉。</span><span class="sxs-lookup"><span data-stu-id="feeb3-133">Specifies whether the key operation is inverted.</span></span><br/>                            |
| [<span data-ttu-id="feeb3-134">**put \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="feeb3-134">**put\_KeyType**</span></span>](idxtkey-put-keytype.md)       | <span data-ttu-id="feeb3-135">指定索引鍵的類型。</span><span class="sxs-lookup"><span data-stu-id="feeb3-135">Specifies the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="feeb3-136">**put \_ 亮度**</span><span class="sxs-lookup"><span data-stu-id="feeb3-136">**put\_Luminance**</span></span>](idxtkey-put-luminance.md)   | <span data-ttu-id="feeb3-137">指定要做為索引鍵的亮度值。</span><span class="sxs-lookup"><span data-stu-id="feeb3-137">Specifies the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="feeb3-138">**put \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="feeb3-138">**put\_RGB**</span></span>](idxtkey-put-rgb.md)               | <span data-ttu-id="feeb3-139">指定要做為索引鍵的 RGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="feeb3-139">Specifies the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="feeb3-140">**放置 \_ 相似性**</span><span class="sxs-lookup"><span data-stu-id="feeb3-140">**put\_Similarity**</span></span>](idxtkey-put-similarity.md) | <span data-ttu-id="feeb3-141">指定變成透明的色彩資料範圍。</span><span class="sxs-lookup"><span data-stu-id="feeb3-141">Specifies the range of color data that becomes transparent.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="feeb3-142">備註</span><span class="sxs-lookup"><span data-stu-id="feeb3-142">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="feeb3-143">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="feeb3-143">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="feeb3-144">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="feeb3-144">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="feeb3-145">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="feeb3-145">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="feeb3-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="feeb3-146">Requirements</span></span>



| <span data-ttu-id="feeb3-147">需求</span><span class="sxs-lookup"><span data-stu-id="feeb3-147">Requirement</span></span> | <span data-ttu-id="feeb3-148">值</span><span class="sxs-lookup"><span data-stu-id="feeb3-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="feeb3-149">標頭</span><span class="sxs-lookup"><span data-stu-id="feeb3-149">Header</span></span><br/>  | <dl> <span data-ttu-id="feeb3-150"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="feeb3-150"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="feeb3-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="feeb3-151">Library</span></span><br/> | <dl> <span data-ttu-id="feeb3-152"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="feeb3-152"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




