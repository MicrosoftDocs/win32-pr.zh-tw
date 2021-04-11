---
title: DRM_KeyID
description: DRM \_ KeyID 屬性包含金鑰識別碼。
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID windows Media 格式
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023074"
---
# <a name="drm_keyid"></a><span data-ttu-id="5ae1b-104">DRM \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="5ae1b-104">DRM\_KeyID</span></span>

<span data-ttu-id="5ae1b-105">**DRM \_ KeyID** 屬性包含金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-105">The **DRM\_KeyID** attribute contains the key identifier.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5ae1b-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="5ae1b-106">Global Constant</span></span>

<span data-ttu-id="5ae1b-107">g \_ wszWMDRM \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="5ae1b-107">g\_wszWMDRM\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="5ae1b-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="5ae1b-108">Data Type</span></span>

<span data-ttu-id="5ae1b-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="5ae1b-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="5ae1b-110">備註</span><span class="sxs-lookup"><span data-stu-id="5ae1b-110">Remarks</span></span>

<span data-ttu-id="5ae1b-111">只有 DRM 版本7內容有此屬性。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-111">This attribute is present for DRM Version 7 content only.</span></span> <span data-ttu-id="5ae1b-112">您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定它，也可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="5ae1b-113">您可以使用 [**DRM \_ DRMHeader \_ KeyID**](drm-drmheader-keyid.md)來取出相同的檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

<span data-ttu-id="5ae1b-114">金鑰識別碼會與金鑰種子搭配使用，以建立用來加密和解密檔案的內容金鑰。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-114">The key ID is used in conjunction with the key seed to create the content key which is used to encrypt and decrypt the file.</span></span> <span data-ttu-id="5ae1b-115">寫入器應用程式會使用金鑰識別碼來加密檔案，然後將金鑰識別碼儲存在檔案標頭中。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-115">The writer application uses the key ID to encrypt the file and then it stores the key ID in the file header.</span></span> <span data-ttu-id="5ae1b-116">當播放程式應用程式要求檔案的授權時，DRM 元件會將金鑰識別碼 (以及 DRM 標頭的其餘部分傳送) 至授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-116">When a player application requests a license for a file, the DRM component sends the key ID (along with the rest of the DRM header) to the license server.</span></span> <span data-ttu-id="5ae1b-117">具有秘密金鑰種子的授權伺服器會使用它和金鑰識別碼來建立檔案的金鑰，然後將它插入授權，以及將套用至該檔案的各種許可權。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-117">The license server, which has the secret key seed, uses it and the key ID to create a key for the file, which it then inserts into a license along with the various rights that will be applied to the file.</span></span>

<span data-ttu-id="5ae1b-118">通常會搭配許多金鑰識別碼使用一個金鑰種子。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-118">Typically, one key seed is used with many key IDs.</span></span> <span data-ttu-id="5ae1b-119">金鑰種子是唯一由內容建立者和授權散發者共用的秘密。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-119">The key seed is a secret shared only by the content creator and the license distributor.</span></span> <span data-ttu-id="5ae1b-120">金鑰識別碼是由 DRM 用戶端應用程式使用，並以純文字儲存在 DRM 標頭中。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-120">The key ID is used by DRM client applications and is stored in the DRM header in the clear.</span></span>

<span data-ttu-id="5ae1b-121">這個屬性與 [**DRM \_ DRMHeader \_ KeyID**](drm-drmheader-keyid.md)相同。</span><span class="sxs-lookup"><span data-stu-id="5ae1b-121">This attribute is the same as [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5ae1b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ae1b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae1b-123">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="5ae1b-123">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




