---
description: 設定 Microsoft 媒體基礎 HTTP 位元組資料流程的根安全識別碼。
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: 'MFPKEY_HTTP_ByteStream_Urlmon_Security_Id 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980209"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a><span data-ttu-id="7b501-103">MFPKEY \_ HTTP \_ ByteStream \_ urlmon.dll \_ 安全性 \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="7b501-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Security\_Id property</span></span>

<span data-ttu-id="7b501-104">設定 Microsoft 媒體基礎 HTTP 位元組資料流程的根安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b501-104">Sets the root security identifier for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="7b501-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7b501-105">Data type</span></span>

<span data-ttu-id="7b501-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="7b501-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="7b501-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="7b501-107">PROPVARIANT member</span></span>

<span data-ttu-id="7b501-108">**CAUB**</span><span class="sxs-lookup"><span data-stu-id="7b501-108">**CAUB**</span></span>

<span data-ttu-id="7b501-109">VT \_ 向量 \| vt \_ UI1</span><span class="sxs-lookup"><span data-stu-id="7b501-109">VT\_VECTOR \| VT\_UI1</span></span>

<span data-ttu-id="7b501-110">**caub**</span><span class="sxs-lookup"><span data-stu-id="7b501-110">**caub**</span></span>



## <a name="remarks"></a><span data-ttu-id="7b501-111">備註</span><span class="sxs-lookup"><span data-stu-id="7b501-111">Remarks</span></span>

<span data-ttu-id="7b501-112">您可以使用這個屬性來設定媒體基礎 HTTP 位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="7b501-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="7b501-113">若要設定屬性，請將 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="7b501-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="7b501-114">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="7b501-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="7b501-115">這個屬性只適用于 [MFPKEY \_ HTTP \_ ByteStream \_ Enable \_ Urlmon.dll](mfpkey-http-bytestream-enable-urlmon.md) 屬性設為 **VARIANT \_ TRUE** 時。</span><span class="sxs-lookup"><span data-stu-id="7b501-115">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b501-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b501-116">Requirements</span></span>



| <span data-ttu-id="7b501-117">需求</span><span class="sxs-lookup"><span data-stu-id="7b501-117">Requirement</span></span> | <span data-ttu-id="7b501-118">值</span><span class="sxs-lookup"><span data-stu-id="7b501-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b501-119">標頭</span><span class="sxs-lookup"><span data-stu-id="7b501-119">Header</span></span><br/> | <dl> <span data-ttu-id="7b501-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b501-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b501-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b501-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b501-122">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="7b501-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
