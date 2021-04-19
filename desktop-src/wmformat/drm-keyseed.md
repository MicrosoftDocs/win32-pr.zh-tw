---
title: DRM_KeySeed
description: DRM \_ KeySeed 屬性包含將與 KeyID 搭配使用來建立金鑰的金鑰種子。
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed windows Media 格式
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106993726"
---
# <a name="drm_keyseed"></a><span data-ttu-id="3b458-104">DRM \_ KeySeed</span><span class="sxs-lookup"><span data-stu-id="3b458-104">DRM\_KeySeed</span></span>

<span data-ttu-id="3b458-105">**DRM \_ KeySeed** 屬性包含將與 KeyID 搭配使用來建立金鑰的金鑰種子。</span><span class="sxs-lookup"><span data-stu-id="3b458-105">The **DRM\_KeySeed** property contains the key seed that will be used in conjunction with the KeyID to create the key.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3b458-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="3b458-106">Global Constant</span></span>

<span data-ttu-id="3b458-107">g \_ wszWMDRM \_ KeySeed</span><span class="sxs-lookup"><span data-stu-id="3b458-107">g\_wszWMDRM\_KeySeed</span></span>

## <a name="data-type"></a><span data-ttu-id="3b458-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="3b458-108">Data Type</span></span>

<span data-ttu-id="3b458-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="3b458-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="3b458-110">備註</span><span class="sxs-lookup"><span data-stu-id="3b458-110">Remarks</span></span>

<span data-ttu-id="3b458-111">您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3b458-111">This property can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span> <span data-ttu-id="3b458-112">讀取器物件無法存取它。</span><span class="sxs-lookup"><span data-stu-id="3b458-112">It is not accessible by the reader object.</span></span>

<span data-ttu-id="3b458-113">金鑰種子通常用來保護多個檔案或檔案集，例如授權伺服器所發行的所有檔案，或特定演出者可能的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="3b458-113">A key seed is typically used to protect multiple files or sets of files, for example all the files issued by a license server, or perhaps all the files by a particular artist.</span></span> <span data-ttu-id="3b458-114">不過，KeyID 對每個檔案而言是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3b458-114">The KeyID, however, is unique for each file.</span></span>

<span data-ttu-id="3b458-115">金鑰種子必須保留只在內容建立者與授權散發者之間共用的秘密。</span><span class="sxs-lookup"><span data-stu-id="3b458-115">The key seed must remain a secret that is shared only between the content creator and the license distributor.</span></span> <span data-ttu-id="3b458-116">此值不會儲存在 DRM 標頭中，也不需要它，也不能存取 DRM 播放機應用程式。</span><span class="sxs-lookup"><span data-stu-id="3b458-116">This value is not stored in the DRM header and it is neither needed by nor accessible to DRM player applications.</span></span>

<span data-ttu-id="3b458-117">您可以使用 [**IWMDRMWriter：： GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) 方法或任何其他適當的方式來產生新的金鑰種子。</span><span class="sxs-lookup"><span data-stu-id="3b458-117">A new key seed can be generated using the [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) method or by any other suitable means.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b458-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b458-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b458-119">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="3b458-119">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




