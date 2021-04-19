---
description: 下列 Guid 支援 (CDM) 的內容解密模組。
title: 內容解密模組 (CDM) GUID
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984312"
---
# <a name="content-decryption-module-cdm-guids"></a><span data-ttu-id="d3634-103">內容解密模組 (CDM) GUID</span><span class="sxs-lookup"><span data-stu-id="d3634-103">Content Decryption Module (CDM) GUIDs</span></span>

<span data-ttu-id="d3634-104">下列 Guid 支援 (CDM) 的內容解密模組。</span><span class="sxs-lookup"><span data-stu-id="d3634-104">The following GUIDs support Content Decryption Module (CDM) implementations.</span></span>

<span data-ttu-id="d3634-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span><span class="sxs-lookup"><span data-stu-id="d3634-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span></span>

<span data-ttu-id="d3634-106">用來從 [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) 執行取得介面的服務 GUID，例如 WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) 介面。</span><span class="sxs-lookup"><span data-stu-id="d3634-106">Service GUID used to obtain interfaces from an [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) implementation,such as the WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) interface.</span></span> <span data-ttu-id="d3634-107">**IMFContentDecryptionModule** 的執行應該會執行 [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)並支援此服務 GUID。</span><span class="sxs-lookup"><span data-stu-id="d3634-107">An implementation of **IMFContentDecryptionModule** should implement [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) and support this service GUID.</span></span>


## <a name="requirements"></a><span data-ttu-id="d3634-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3634-108">Requirements</span></span>



| <span data-ttu-id="d3634-109">需求</span><span class="sxs-lookup"><span data-stu-id="d3634-109">Requirement</span></span> | <span data-ttu-id="d3634-110">值</span><span class="sxs-lookup"><span data-stu-id="d3634-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3634-111">標頭</span><span class="sxs-lookup"><span data-stu-id="d3634-111">Header</span></span><br/> | <dl> <span data-ttu-id="d3634-112"><dt>mfcontentdecryptionmodule。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3634-112"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3634-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3634-113">See also</span></span>



- [<span data-ttu-id="d3634-114">媒體基礎常數</span><span class="sxs-lookup"><span data-stu-id="d3634-114">Media Foundation Constants</span></span>](media-foundation-constants.md)
- <span data-ttu-id="d3634-115">[IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span><span class="sxs-lookup"><span data-stu-id="d3634-115">[IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span></span>
- [<span data-ttu-id="d3634-116">IMediaProtectionPMPServer</span><span class="sxs-lookup"><span data-stu-id="d3634-116">IMediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [<span data-ttu-id="d3634-117">IMFGetService</span><span class="sxs-lookup"><span data-stu-id="d3634-117">IMFGetService</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




