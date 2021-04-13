---
title: DRM_DRMHeader_KeyID
description: DRM \_ DRMHeader \_ KeyID 屬性包含檔案的金鑰識別碼。
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- DRM_DRMHeader_KeyID windows Media 格式
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314286"
---
# <a name="drm_drmheader_keyid"></a><span data-ttu-id="03ec9-104">DRM \_ DRMHeader \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="03ec9-104">DRM\_DRMHeader\_KeyID</span></span>

<span data-ttu-id="03ec9-105">**DRM \_ DRMHeader \_ KeyID** 屬性包含檔案的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="03ec9-105">The **DRM\_DRMHeader\_KeyID** attribute contains the key ID for the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="03ec9-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="03ec9-106">Global Constant</span></span>

<span data-ttu-id="03ec9-107">g \_ wszWMDRM \_ DRMHeader \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="03ec9-107">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="03ec9-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="03ec9-108">Data Type</span></span>

<span data-ttu-id="03ec9-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="03ec9-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="03ec9-110">備註</span><span class="sxs-lookup"><span data-stu-id="03ec9-110">Remarks</span></span>

<span data-ttu-id="03ec9-111">這個屬性只有 DRM 版本7內容存在。</span><span class="sxs-lookup"><span data-stu-id="03ec9-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="03ec9-112">您可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出它。</span><span class="sxs-lookup"><span data-stu-id="03ec9-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="03ec9-113">若要使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 在檔案上設定金鑰識別碼，您必須使用 [**DRM \_ KeyID**](drm-keyid.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="03ec9-113">To set the key ID on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_KeyID**](drm-keyid.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="03ec9-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03ec9-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ec9-115">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="03ec9-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




