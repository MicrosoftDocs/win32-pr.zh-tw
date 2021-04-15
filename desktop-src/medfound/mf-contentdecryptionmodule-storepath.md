---
description: 指定檔案路徑，代表內容解密模組 (CDM) 可用於初始化的儲存位置。
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469196"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a><span data-ttu-id="22238-103">MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH 屬性</span><span class="sxs-lookup"><span data-stu-id="22238-103">MF\_CONTENTDECRYPTIONMODULE\_STOREPATH property</span></span>

<span data-ttu-id="22238-104">指定檔案路徑，代表內容解密模組 (CDM) 可用於初始化的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="22238-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>


## <a name="data-type"></a><span data-ttu-id="22238-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="22238-105">Data type</span></span>

<span data-ttu-id="22238-106">**LPWSTR** (VT_LPWSTR) </span><span class="sxs-lookup"><span data-stu-id="22238-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="22238-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="22238-107">Property GUID</span></span>

<span data-ttu-id="22238-108">**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**</span><span class="sxs-lookup"><span data-stu-id="22238-108">**MF\_CONTENTDECRYPTIONMODULE\_STOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="22238-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="22238-109">Property value</span></span>

<span data-ttu-id="22238-110">檔案路徑，代表內容解密模組 (CDM) 可用於初始化的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="22238-110">A file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>

## <a name="remarks"></a><span data-ttu-id="22238-111">備註</span><span class="sxs-lookup"><span data-stu-id="22238-111">Remarks</span></span>

<span data-ttu-id="22238-112">如果未設定 [MF_CONTENTDECRYPTIONMODULE_INPRI加值稅ESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) 屬性，則使用這個屬性指定的路徑也將用於內容特定資料。</span><span class="sxs-lookup"><span data-stu-id="22238-112">The path specified with this property will also be used for content-specific data if the [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) property isn't set.</span></span>

<span data-ttu-id="22238-113">為了改善 COM 效能，應用程式不應該在釋放 CDM 物件後刪除存放區位置。</span><span class="sxs-lookup"><span data-stu-id="22238-113">To improve COM performance, the app should not delete the store location after the CDM object has been released.</span></span>



<span data-ttu-id="22238-114">當您藉由呼叫 [IMFContentDecryptionModuleAccess：： CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)來建立 CDM 時，請設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="22238-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="22238-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="22238-115">Requirements</span></span>



| <span data-ttu-id="22238-116">需求</span><span class="sxs-lookup"><span data-stu-id="22238-116">Requirement</span></span> | <span data-ttu-id="22238-117">值</span><span class="sxs-lookup"><span data-stu-id="22238-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22238-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22238-118">Minimum supported client</span></span><br/> | <span data-ttu-id="22238-119">Windows 10 2020 年4月更新</span><span class="sxs-lookup"><span data-stu-id="22238-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="22238-120">標頭</span><span class="sxs-lookup"><span data-stu-id="22238-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="22238-121"><dt>mfcontentdecryptionmodule。h</dt></span><span class="sxs-lookup"><span data-stu-id="22238-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22238-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22238-122">See also</span></span>

- [<span data-ttu-id="22238-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="22238-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="22238-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span><span class="sxs-lookup"><span data-stu-id="22238-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




