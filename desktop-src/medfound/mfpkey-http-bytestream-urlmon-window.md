---
description: 設定 Microsoft 媒體基礎 HTTP 位元組資料流程的視窗。
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: 'MFPKEY_HTTP_ByteStream_Urlmon_Window 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999507"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a><span data-ttu-id="fb204-103">MFPKEY \_ HTTP \_ ByteStream \_ urlmon.dll \_ 視窗屬性</span><span class="sxs-lookup"><span data-stu-id="fb204-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Window property</span></span>

<span data-ttu-id="fb204-104">設定 Microsoft 媒體基礎 HTTP 位元組資料流程的視窗。</span><span class="sxs-lookup"><span data-stu-id="fb204-104">Sets a window for the Microsoft Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="fb204-105">此視窗會在系結作業期間用來顯示使用者介面中的資訊。</span><span class="sxs-lookup"><span data-stu-id="fb204-105">The window is used to present information in the user interface during a bind operation.</span></span>



<span data-ttu-id="fb204-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="fb204-106">Data type</span></span>

<span data-ttu-id="fb204-107">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="fb204-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="fb204-108">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="fb204-108">PROPVARIANT member</span></span>

<span data-ttu-id="fb204-109">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="fb204-109">**IUnknown\***</span></span>

<span data-ttu-id="fb204-110">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="fb204-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="fb204-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="fb204-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="fb204-112">備註</span><span class="sxs-lookup"><span data-stu-id="fb204-112">Remarks</span></span>

<span data-ttu-id="fb204-113">您可以使用這個屬性來設定媒體基礎 HTTP 位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="fb204-113">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="fb204-114">若要設定屬性，請將 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="fb204-114">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="fb204-115">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="fb204-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="fb204-116">這個屬性的值是 **IWindowForBindingUI** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="fb204-116">The value of this property is a pointer to the **IWindowForBindingUI** interface.</span></span> <span data-ttu-id="fb204-117">這個屬性只適用于 [MFPKEY \_ HTTP \_ ByteStream \_ Enable \_ Urlmon.dll](mfpkey-http-bytestream-enable-urlmon.md) 屬性設為 **VARIANT \_ TRUE** 時。</span><span class="sxs-lookup"><span data-stu-id="fb204-117">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb204-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb204-118">Requirements</span></span>



| <span data-ttu-id="fb204-119">需求</span><span class="sxs-lookup"><span data-stu-id="fb204-119">Requirement</span></span> | <span data-ttu-id="fb204-120">值</span><span class="sxs-lookup"><span data-stu-id="fb204-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb204-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fb204-121">Header</span></span><br/> | <dl> <span data-ttu-id="fb204-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb204-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb204-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb204-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb204-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="fb204-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
