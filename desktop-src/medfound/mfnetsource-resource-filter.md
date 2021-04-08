---
description: 包含 Microsoft 媒體基礎 HTTP 位元組資料流程的 IMFNetResourceFilter 回呼介面指標。
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: 'MFNETSOURCE_RESOURCE_FILTER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691807"
---
# <a name="mfnetsource_resource_filter-property"></a><span data-ttu-id="785df-103">MFNETSOURCE \_ 資源 \_ 篩選屬性</span><span class="sxs-lookup"><span data-stu-id="785df-103">MFNETSOURCE\_RESOURCE\_FILTER property</span></span>

<span data-ttu-id="785df-104">包含 Microsoft 媒體基礎 HTTP 位元組資料流程的 [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) 回呼介面指標。</span><span class="sxs-lookup"><span data-stu-id="785df-104">Contains a pointer to the [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) callback interface for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="785df-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="785df-105">Data type</span></span>

<span data-ttu-id="785df-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="785df-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="785df-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="785df-107">PROPVARIANT member</span></span>

<span data-ttu-id="785df-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="785df-108">\**IUnknown\** _</span></span>

<span data-ttu-id="785df-109">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="785df-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="785df-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="785df-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="785df-111">備註</span><span class="sxs-lookup"><span data-stu-id="785df-111">Remarks</span></span>

<span data-ttu-id="785df-112">您可以使用這個屬性來設定媒體基礎 HTTP 位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="785df-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="785df-113">若要設定屬性，請將 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="785df-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="785df-114">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="785df-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="785df-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="785df-115">Requirements</span></span>



| <span data-ttu-id="785df-116">需求</span><span class="sxs-lookup"><span data-stu-id="785df-116">Requirement</span></span> | <span data-ttu-id="785df-117">值</span><span class="sxs-lookup"><span data-stu-id="785df-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="785df-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="785df-118">Minimum supported client</span></span><br/> | <span data-ttu-id="785df-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="785df-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="785df-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="785df-120">Minimum supported server</span></span><br/> | <span data-ttu-id="785df-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="785df-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="785df-122">標頭</span><span class="sxs-lookup"><span data-stu-id="785df-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="785df-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="785df-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="785df-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="785df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="785df-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="785df-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
