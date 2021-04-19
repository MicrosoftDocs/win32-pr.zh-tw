---
description: 設定範例的金鑰識別碼。
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: 'MFSampleExtension_Content_KeyID 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989938"
---
# <a name="mfsampleextension_content_keyid-attribute"></a><span data-ttu-id="dcb02-103">MFSampleExtension \_ 內容 \_ KeyID 屬性</span><span class="sxs-lookup"><span data-stu-id="dcb02-103">MFSampleExtension\_Content\_KeyID attribute</span></span>

<span data-ttu-id="dcb02-104">設定範例的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="dcb02-104">Sets the Key ID for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="dcb02-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="dcb02-105">Data type</span></span>

<span data-ttu-id="dcb02-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="dcb02-106">**GUID**</span></span>

## <a name="examples"></a><span data-ttu-id="dcb02-107">範例</span><span class="sxs-lookup"><span data-stu-id="dcb02-107">Examples</span></span>

<span data-ttu-id="dcb02-108">下列範例顯示如何設定範例的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="dcb02-108">The following example shows how to set the Key ID for the sample.</span></span>


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a><span data-ttu-id="dcb02-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcb02-109">Requirements</span></span>



| <span data-ttu-id="dcb02-110">需求</span><span class="sxs-lookup"><span data-stu-id="dcb02-110">Requirement</span></span> | <span data-ttu-id="dcb02-111">值</span><span class="sxs-lookup"><span data-stu-id="dcb02-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb02-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dcb02-112">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb02-113">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dcb02-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="dcb02-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dcb02-114">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb02-115">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dcb02-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="dcb02-116">標頭</span><span class="sxs-lookup"><span data-stu-id="dcb02-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcb02-117"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="dcb02-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcb02-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcb02-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb02-119">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="dcb02-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dcb02-120">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="dcb02-120">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="dcb02-121">MFSampleExtension \_ 加密 \_ SubSampleMappingSplit</span><span class="sxs-lookup"><span data-stu-id="dcb02-121">MFSampleExtension\_Encryption\_SubSampleMappingSplit</span></span>](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




