---
description: 指定 proxy 伺服器的主機名稱。
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: 'MFNETSOURCE_PROXYHOSTNAME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc59d5b827276eb5063febf7a8cb7647002ca72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970216"
---
# <a name="mfnetsource_proxyhostname-property"></a><span data-ttu-id="bc049-103">MFNETSOURCE \_ PROXYHOSTNAME 屬性</span><span class="sxs-lookup"><span data-stu-id="bc049-103">MFNETSOURCE\_PROXYHOSTNAME property</span></span>

<span data-ttu-id="bc049-104">指定 proxy 伺服器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="bc049-104">Specifies the host name of the proxy server.</span></span>



<span data-ttu-id="bc049-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="bc049-105">Data type</span></span>

<span data-ttu-id="bc049-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="bc049-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="bc049-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="bc049-107">PROPVARIANT member</span></span>

<span data-ttu-id="bc049-108">寬字元字串 (**WCHAR** \*) </span><span class="sxs-lookup"><span data-stu-id="bc049-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="bc049-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="bc049-109">VT\_LPWSTR</span></span>

<span data-ttu-id="bc049-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="bc049-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="bc049-111">備註</span><span class="sxs-lookup"><span data-stu-id="bc049-111">Remarks</span></span>

<span data-ttu-id="bc049-112">常數 **MFNETSOURCE \_ PROXYHOSTNAME** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="bc049-112">The constant **MFNETSOURCE\_PROXYHOSTNAME** defines the GUID for this property key.</span></span> <span data-ttu-id="bc049-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="bc049-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="bc049-114">當建立 proxy 定位器物件時，應用程式可以使用這個屬性來設定預設 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="bc049-114">Applications can use this property to configure the default proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="bc049-115">若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。</span><span class="sxs-lookup"><span data-stu-id="bc049-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="bc049-116">當 proxy 定位器設定成以手動模式操作時，應用程式必須設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="bc049-116">This property must be set by the application when the proxy locator is configured to operate in the manual mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc049-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc049-117">Requirements</span></span>



| <span data-ttu-id="bc049-118">需求</span><span class="sxs-lookup"><span data-stu-id="bc049-118">Requirement</span></span> | <span data-ttu-id="bc049-119">值</span><span class="sxs-lookup"><span data-stu-id="bc049-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bc049-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc049-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bc049-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc049-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bc049-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc049-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bc049-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc049-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bc049-124">標頭</span><span class="sxs-lookup"><span data-stu-id="bc049-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc049-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc049-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc049-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc049-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc049-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="bc049-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="bc049-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="bc049-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="bc049-129">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="bc049-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




