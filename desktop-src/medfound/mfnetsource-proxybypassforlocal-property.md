---
description: 指定 proxy 定位器是否應針對本機位址使用 proxy 伺服器。
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: 'MFNETSOURCE_PROXYBYPASSFORLOCAL 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689275"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a><span data-ttu-id="71899-103">MFNETSOURCE \_ PROXYBYPASSFORLOCAL 屬性</span><span class="sxs-lookup"><span data-stu-id="71899-103">MFNETSOURCE\_PROXYBYPASSFORLOCAL property</span></span>

<span data-ttu-id="71899-104">指定 proxy 定位器是否應針對本機位址使用 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="71899-104">Specifies whether the proxy locator should use a proxy server for local addresses.</span></span>



<span data-ttu-id="71899-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="71899-105">Data type</span></span>

<span data-ttu-id="71899-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="71899-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="71899-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="71899-107">PROPVARIANT member</span></span>

<span data-ttu-id="71899-108">布林 (**LONG**) </span><span class="sxs-lookup"><span data-stu-id="71899-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="71899-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="71899-109">VT\_I4</span></span>

<span data-ttu-id="71899-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="71899-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="71899-111">備註</span><span class="sxs-lookup"><span data-stu-id="71899-111">Remarks</span></span>

<span data-ttu-id="71899-112">常數 **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="71899-112">The constant **MFNETSOURCE\_PROXYBYPASSFORLOCAL** defines the GUID for this property key.</span></span> <span data-ttu-id="71899-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="71899-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="71899-114">應用程式可以在建立 proxy 定位器物件時使用這個屬性來設定 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="71899-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="71899-115">若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。</span><span class="sxs-lookup"><span data-stu-id="71899-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="71899-116">如果 proxy 伺服器要用於本機位址，此值必須設定為0。否則，非零值會設定預設 proxy 定位器，以略過本機位址的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="71899-116">The value must be set to 0 if the proxy server is to be used for local addresses; otherwise a nonzero value configures the default proxy locator to skip the proxy server for local addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="71899-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="71899-117">Requirements</span></span>



| <span data-ttu-id="71899-118">需求</span><span class="sxs-lookup"><span data-stu-id="71899-118">Requirement</span></span> | <span data-ttu-id="71899-119">值</span><span class="sxs-lookup"><span data-stu-id="71899-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71899-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71899-120">Minimum supported client</span></span><br/> | <span data-ttu-id="71899-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71899-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="71899-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71899-122">Minimum supported server</span></span><br/> | <span data-ttu-id="71899-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71899-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="71899-124">標頭</span><span class="sxs-lookup"><span data-stu-id="71899-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="71899-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="71899-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71899-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71899-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71899-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="71899-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="71899-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="71899-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="71899-129">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="71899-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




