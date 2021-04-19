---
description: 設定 Microsoft 媒體基礎 HTTP 位元組資料流程的標記系結旗標。
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: 'MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975982"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a><span data-ttu-id="2e38e-103">MFPKEY \_ HTTP \_ ByteStream \_ Urlmon.dll 系結 \_ \_ 旗標屬性</span><span class="sxs-lookup"><span data-stu-id="2e38e-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Bind\_Flags property</span></span>

<span data-ttu-id="2e38e-104">設定 Microsoft 媒體基礎 HTTP 位元組資料流程的標記系結旗標。</span><span class="sxs-lookup"><span data-stu-id="2e38e-104">Sets the moniker binding flags for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="2e38e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="2e38e-105">Data type</span></span>

<span data-ttu-id="2e38e-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="2e38e-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2e38e-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="2e38e-107">PROPVARIANT member</span></span>

<span data-ttu-id="2e38e-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="2e38e-108">**ULONG**</span></span>

<span data-ttu-id="2e38e-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="2e38e-109">VT\_UI4</span></span>

<span data-ttu-id="2e38e-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="2e38e-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2e38e-111">備註</span><span class="sxs-lookup"><span data-stu-id="2e38e-111">Remarks</span></span>

<span data-ttu-id="2e38e-112">您可以使用這個屬性來設定媒體基礎 HTTP 位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="2e38e-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="2e38e-113">若要設定屬性，請將 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="2e38e-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="2e38e-114">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="2e38e-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="2e38e-115">這個屬性的值是 **BINDF** 列舉中的位 **or** 旗標。</span><span class="sxs-lookup"><span data-stu-id="2e38e-115">The value of this property is a bitwise **OR** of flags from the **BINDF** enumeration.</span></span> <span data-ttu-id="2e38e-116">這個屬性只適用于 [MFPKEY \_ HTTP \_ ByteStream \_ Enable \_ Urlmon.dll](mfpkey-http-bytestream-enable-urlmon.md) 屬性設為 **VARIANT \_ TRUE** 時。</span><span class="sxs-lookup"><span data-stu-id="2e38e-116">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e38e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e38e-117">Requirements</span></span>



| <span data-ttu-id="2e38e-118">需求</span><span class="sxs-lookup"><span data-stu-id="2e38e-118">Requirement</span></span> | <span data-ttu-id="2e38e-119">值</span><span class="sxs-lookup"><span data-stu-id="2e38e-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e38e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2e38e-120">Header</span></span><br/> | <dl> <span data-ttu-id="2e38e-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e38e-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e38e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e38e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e38e-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="2e38e-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
