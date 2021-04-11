---
description: 包含 IMFNetCredentialManager 介面的指標。
ms.assetid: c0826956-9df1-40ec-8ad1-9e0dca34d847
title: 'MFNETSOURCE_CREDENTIAL_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3447369cedfa5c516e1d7696aae70834c6ce89a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114000"
---
# <a name="mfnetsource_credential_manager-property"></a><span data-ttu-id="04659-103">MFNETSOURCE \_ CREDENTIAL \_ MANAGER 屬性</span><span class="sxs-lookup"><span data-stu-id="04659-103">MFNETSOURCE\_CREDENTIAL\_MANAGER property</span></span>

<span data-ttu-id="04659-104">包含 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="04659-104">Contains a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="04659-105">使用這個屬性，將應用程式的 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 執行傳遞至網路來源。</span><span class="sxs-lookup"><span data-stu-id="04659-105">Use this property to pass the application's implementation of [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) to the network source.</span></span>



<span data-ttu-id="04659-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="04659-106">Data type</span></span>

<span data-ttu-id="04659-107">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="04659-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="04659-108">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="04659-108">PROPVARIANT member</span></span>

<span data-ttu-id="04659-109">**IUnknown** 指標</span><span class="sxs-lookup"><span data-stu-id="04659-109">**IUnknown** pointer</span></span>

<span data-ttu-id="04659-110">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="04659-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="04659-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="04659-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="04659-112">備註</span><span class="sxs-lookup"><span data-stu-id="04659-112">Remarks</span></span>

<span data-ttu-id="04659-113">常數 **MFNETSOURCE \_ CREDENTIAL \_ MANAGER** 會定義屬性索引鍵的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="04659-113">The constant **MFNETSOURCE\_CREDENTIAL\_MANAGER** defines the **GUID** for the property key.</span></span> <span data-ttu-id="04659-114"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="04659-114">The property identifier (PID) is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="04659-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="04659-115">Requirements</span></span>



| <span data-ttu-id="04659-116">需求</span><span class="sxs-lookup"><span data-stu-id="04659-116">Requirement</span></span> | <span data-ttu-id="04659-117">值</span><span class="sxs-lookup"><span data-stu-id="04659-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04659-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04659-118">Minimum supported client</span></span><br/> | <span data-ttu-id="04659-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04659-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="04659-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04659-120">Minimum supported server</span></span><br/> | <span data-ttu-id="04659-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04659-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="04659-122">標頭</span><span class="sxs-lookup"><span data-stu-id="04659-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="04659-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="04659-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04659-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04659-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04659-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="04659-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="04659-126">網路來源驗證</span><span class="sxs-lookup"><span data-stu-id="04659-126">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> <dt>

[<span data-ttu-id="04659-127">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="04659-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




