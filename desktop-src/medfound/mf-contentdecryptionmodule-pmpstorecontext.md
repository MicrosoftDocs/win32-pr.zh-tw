---
description: 指定內容解密模組所使用的內容字串 (CDM 使用 MediaProtectionPMPServer 的) 。
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969269"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a><span data-ttu-id="9a112-103">MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT 屬性</span><span class="sxs-lookup"><span data-stu-id="9a112-103">MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT property</span></span>

<span data-ttu-id="9a112-104">指定內容解密模組所使用的內容字串 (CDM 使用 [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)的) 。</span><span class="sxs-lookup"><span data-stu-id="9a112-104">Specifies a context string used by Content Decryption Module (CDM) implementations that use [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span></span>


## <a name="data-type"></a><span data-ttu-id="9a112-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9a112-105">Data type</span></span>

<span data-ttu-id="9a112-106">**LPWSTR** (VT_LPWSTR) </span><span class="sxs-lookup"><span data-stu-id="9a112-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9a112-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="9a112-107">Property GUID</span></span>

<span data-ttu-id="9a112-108">**MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT**</span><span class="sxs-lookup"><span data-stu-id="9a112-108">**MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT**</span></span>

## <a name="property-value"></a><span data-ttu-id="9a112-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="9a112-109">Property value</span></span>

<span data-ttu-id="9a112-110">內容解密模組所使用的內容字串 (CDM) 的實作為。</span><span class="sxs-lookup"><span data-stu-id="9a112-110">A  a context string used by Content Decryption Module (CDM) implementations.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a112-111">備註</span><span class="sxs-lookup"><span data-stu-id="9a112-111">Remarks</span></span>

<span data-ttu-id="9a112-112">CDM 實作者應該尋找此值，並使用屬性名稱 "PMPStoreCoNtext" 將值傳遞至 [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) 函式。</span><span class="sxs-lookup"><span data-stu-id="9a112-112">The CDM implementer should look for this value and pass the value to the [MediaProtectionPMPServer constructor](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) using the property name "Windows.Media.Protection.PMPStoreContext".</span></span>


<span data-ttu-id="9a112-113">呼叫 [IMFContentDecryptionModuleAccess：： CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)時，應用程式不應該建立這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9a112-113">Apps should not create this property when calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a112-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a112-114">Requirements</span></span>



| <span data-ttu-id="9a112-115">需求</span><span class="sxs-lookup"><span data-stu-id="9a112-115">Requirement</span></span> | <span data-ttu-id="9a112-116">值</span><span class="sxs-lookup"><span data-stu-id="9a112-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a112-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a112-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9a112-118">Windows 10 2020 年4月更新</span><span class="sxs-lookup"><span data-stu-id="9a112-118">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="9a112-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9a112-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a112-120"><dt>mfcontentdecryptionmodule。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a112-120"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a112-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a112-121">See also</span></span>

- [<span data-ttu-id="9a112-122">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="9a112-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="9a112-123">MediaProtectionPMPServer</span><span class="sxs-lookup"><span data-stu-id="9a112-123">MediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




