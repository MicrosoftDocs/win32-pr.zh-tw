---
description: 啟用 Microsoft 媒體基礎的 HTTP 位元組資料流程，以使用 URL 名字 (也稱為) 。
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: 'MFPKEY_HTTP_ByteStream_Enable_Urlmon 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998720"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a><span data-ttu-id="c496e-103">MFPKEY \_ HTTP \_ ByteStream \_ Enable \_ urlmon.dll 屬性</span><span class="sxs-lookup"><span data-stu-id="c496e-103">MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon property</span></span>

<span data-ttu-id="c496e-104">啟用 Microsoft 媒體基礎的 HTTP 位元組資料流程，以使用 URL 名字 (也 *稱為)* 。</span><span class="sxs-lookup"><span data-stu-id="c496e-104">Enables the Microsoft Media Foundation HTTP byte stream to use URL monikers (also called *Urlmon*).</span></span>



<span data-ttu-id="c496e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c496e-105">Data type</span></span>

<span data-ttu-id="c496e-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="c496e-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c496e-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="c496e-107">PROPVARIANT member</span></span>

<span data-ttu-id="c496e-108">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c496e-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="c496e-109">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="c496e-109">VT\_BOOL</span></span>

<span data-ttu-id="c496e-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="c496e-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c496e-111">備註</span><span class="sxs-lookup"><span data-stu-id="c496e-111">Remarks</span></span>

<span data-ttu-id="c496e-112">您可以使用這個屬性來設定媒體基礎 HTTP 位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="c496e-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="c496e-113">若要設定屬性，請將 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="c496e-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="c496e-114">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="c496e-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="c496e-115">如果值為 **VARIANT \_ TRUE**，HTTP 位元組資料流程會使用 Http 傳輸的 urlmon.dll。</span><span class="sxs-lookup"><span data-stu-id="c496e-115">If the value is **VARIANT\_TRUE**, the HTTP byte stream uses Urlmon for HTTP transport.</span></span> <span data-ttu-id="c496e-116">否則，如果值為 **VARIANT \_ FALSE**，則位元組資料流程會使用 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="c496e-116">Otherwise, if the value is **VARIANT\_FALSE**, the byte stream uses WinHTTP.</span></span>

<span data-ttu-id="c496e-117">Windows Store 應用程式的預設值為 **variant \_ TRUE** ，windows 傳統型應用程式的預設值為 variant **\_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c496e-117">The default value is **VARIANT\_TRUE** for Windows Store apps and **VARIANT\_FALSE** for Windows desktop application.</span></span>

## <a name="requirements"></a><span data-ttu-id="c496e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c496e-118">Requirements</span></span>



| <span data-ttu-id="c496e-119">需求</span><span class="sxs-lookup"><span data-stu-id="c496e-119">Requirement</span></span> | <span data-ttu-id="c496e-120">值</span><span class="sxs-lookup"><span data-stu-id="c496e-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c496e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c496e-121">Header</span></span><br/> | <dl> <span data-ttu-id="c496e-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c496e-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c496e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c496e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c496e-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="c496e-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
