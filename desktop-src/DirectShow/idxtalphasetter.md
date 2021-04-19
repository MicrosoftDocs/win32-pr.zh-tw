---
description: IDxtAlphaSetter 介面會設定 Alpha Setter 效果的屬性。當 DirectShow 編輯服務轉譯 Alpha Setter 效果時，會在內部使用此介面 (DES) 。
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: 'IDxtAlphaSetter 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985779"
---
# <a name="idxtalphasetter-interface"></a><span data-ttu-id="b1ae5-103">IDxtAlphaSetter 介面</span><span class="sxs-lookup"><span data-stu-id="b1ae5-103">IDxtAlphaSetter interface</span></span>

> [!Note]  
> <span data-ttu-id="b1ae5-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-104">\[Deprecated.</span></span> <span data-ttu-id="b1ae5-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b1ae5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1ae5-106">`IDxtAlphaSetter`介面會設定[Alpha Setter](alpha-setter-effect.md)效果上的屬性。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-106">The `IDxtAlphaSetter` interface sets properties on the [Alpha Setter](alpha-setter-effect.md) effect.</span></span>

<span data-ttu-id="b1ae5-107">當 DirectShow 編輯服務轉譯 Alpha Setter 效果時，會在內部使用此介面 (DES) 。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Alpha Setter effect.</span></span> <span data-ttu-id="b1ae5-108">DES 應用程式不需要使用此介面。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="b1ae5-109">若要在 DES 的轉換上設定屬性，請使用 [**IPropertySetter**](ipropertysetter.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="b1ae5-110">成員</span><span class="sxs-lookup"><span data-stu-id="b1ae5-110">Members</span></span>

<span data-ttu-id="b1ae5-111">**IDxtAlphaSetter** 介面繼承自 **IDXEffect**。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-111">The **IDxtAlphaSetter** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="b1ae5-112">**IDxtAlphaSetter** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b1ae5-112">**IDxtAlphaSetter** also has these types of members:</span></span>

-   [<span data-ttu-id="b1ae5-113">方法</span><span class="sxs-lookup"><span data-stu-id="b1ae5-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b1ae5-114">方法</span><span class="sxs-lookup"><span data-stu-id="b1ae5-114">Methods</span></span>

<span data-ttu-id="b1ae5-115">**IDxtAlphaSetter** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-115">The **IDxtAlphaSetter** interface has these methods.</span></span>



| <span data-ttu-id="b1ae5-116">方法</span><span class="sxs-lookup"><span data-stu-id="b1ae5-116">Method</span></span>                                                  | <span data-ttu-id="b1ae5-117">描述</span><span class="sxs-lookup"><span data-stu-id="b1ae5-117">Description</span></span>                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="b1ae5-118">**取得 \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="b1ae5-118">**get\_Alpha**</span></span>](idxtalphasetter-get-alpha.md)         | <span data-ttu-id="b1ae5-119">抓取整個影像的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-119">Retrieves the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="b1ae5-120">**取得 \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="b1ae5-120">**get\_AlphaRamp**</span></span>](idxtalphasetter-get-alpharamp.md) | <span data-ttu-id="b1ae5-121">抓取 Alpha 曲線的屬性。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-121">Retrieves the alpha ramp property.</span></span><br/>              |
| [<span data-ttu-id="b1ae5-122">**put \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="b1ae5-122">**put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)         | <span data-ttu-id="b1ae5-123">指定整個影像的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-123">Specifies the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="b1ae5-124">**put \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="b1ae5-124">**put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md) | <span data-ttu-id="b1ae5-125">指定 Alpha 曲線的屬性。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-125">Specifies the alpha ramp property.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="b1ae5-126">備註</span><span class="sxs-lookup"><span data-stu-id="b1ae5-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b1ae5-127">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b1ae5-128">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b1ae5-129">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b1ae5-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1ae5-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1ae5-130">Requirements</span></span>



| <span data-ttu-id="b1ae5-131">需求</span><span class="sxs-lookup"><span data-stu-id="b1ae5-131">Requirement</span></span> | <span data-ttu-id="b1ae5-132">值</span><span class="sxs-lookup"><span data-stu-id="b1ae5-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ae5-133">標頭</span><span class="sxs-lookup"><span data-stu-id="b1ae5-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b1ae5-134"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1ae5-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b1ae5-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1ae5-135">Library</span></span><br/> | <dl> <span data-ttu-id="b1ae5-136"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1ae5-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




