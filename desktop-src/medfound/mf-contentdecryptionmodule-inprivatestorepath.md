---
description: 指定檔案路徑，代表內容解密模組 (CDM) 可用於內容特定資料的儲存位置。
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511928"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a><span data-ttu-id="c5f12-103">MF \_ CONTENTDECRYPTIONMODULE \_ INPRI加值稅ESTOREPATH 屬性</span><span class="sxs-lookup"><span data-stu-id="c5f12-103">MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH property</span></span>

<span data-ttu-id="c5f12-104">指定檔案路徑，代表內容解密模組 (CDM) 可用於內容特定資料的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="c5f12-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>


## <a name="data-type"></a><span data-ttu-id="c5f12-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c5f12-105">Data type</span></span>

<span data-ttu-id="c5f12-106">**LPWSTR** (VT_LPWSTR) </span><span class="sxs-lookup"><span data-stu-id="c5f12-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c5f12-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="c5f12-107">Property GUID</span></span>

<span data-ttu-id="c5f12-108">**MF \_ CONTENTDECRYPTIONMODULE \_ INPRI加值稅ESTOREPATH**</span><span class="sxs-lookup"><span data-stu-id="c5f12-108">**MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="c5f12-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="c5f12-109">Property value</span></span>

<span data-ttu-id="c5f12-110">檔案路徑，代表內容解密模組 (CDM) 可用於內容特定資料的儲存位置。</span><span class="sxs-lookup"><span data-stu-id="c5f12-110">A file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5f12-111">備註</span><span class="sxs-lookup"><span data-stu-id="c5f12-111">Remarks</span></span>

<span data-ttu-id="c5f12-112">應用程式應該在 CDM 物件發行之後，刪除存放區位置。</span><span class="sxs-lookup"><span data-stu-id="c5f12-112">The app should delete the store location after the CDM object has been released.</span></span>

<span data-ttu-id="c5f12-113">如果未設定此屬性，系統將會使用以內容特定資料的 [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) 屬性指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="c5f12-113">If this property isn't set, the system will use the path specified with the [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) property for content-specific data.</span></span>

<span data-ttu-id="c5f12-114">當您藉由呼叫 [IMFContentDecryptionModuleAccess：： CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)來建立 CDM 時，請設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c5f12-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5f12-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5f12-115">Requirements</span></span>



| <span data-ttu-id="c5f12-116">需求</span><span class="sxs-lookup"><span data-stu-id="c5f12-116">Requirement</span></span> | <span data-ttu-id="c5f12-117">值</span><span class="sxs-lookup"><span data-stu-id="c5f12-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f12-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5f12-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c5f12-119">Windows 10 2020 年4月更新</span><span class="sxs-lookup"><span data-stu-id="c5f12-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="c5f12-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c5f12-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5f12-121"><dt>mfcontentdecryptionmodule。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5f12-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5f12-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5f12-122">See also</span></span>

- [<span data-ttu-id="c5f12-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="c5f12-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="c5f12-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span><span class="sxs-lookup"><span data-stu-id="c5f12-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




