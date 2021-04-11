---
title: 中繼資料 (instrumentationManifest) 元素
description: 包含您可以在其他資訊清單中參考的全域值。
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- 中繼資料元素 EventLog
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093880"
---
# <a name="metadata-instrumentationmanifest-element"></a><span data-ttu-id="c38a5-104">中繼資料 (instrumentationManifest) 元素</span><span class="sxs-lookup"><span data-stu-id="c38a5-104">metadata (instrumentationManifest) Element</span></span>

<span data-ttu-id="c38a5-105">包含您可以在其他資訊清單中參考的全域值。</span><span class="sxs-lookup"><span data-stu-id="c38a5-105">Contains global values that you can reference in other manifests.</span></span> <span data-ttu-id="c38a5-106">如需範例，請參閱 Windows SDK 的 Include 資料夾中包含的 Winmeta.xml 檔案 \\ 。</span><span class="sxs-lookup"><span data-stu-id="c38a5-106">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span>

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

<span data-ttu-id="c38a5-107">**中繼資料** 元素是由 [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="c38a5-107">The **metadata** element is defined by the [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c38a5-108">備註</span><span class="sxs-lookup"><span data-stu-id="c38a5-108">Remarks</span></span>

<span data-ttu-id="c38a5-109">雖然您可以建立包含中繼資料區段的資訊清單，但服務將不會使用它。服務唯一可辨識的中繼資料是 Winmeta.xml 檔案中找到的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c38a5-109">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c38a5-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c38a5-110">Requirements</span></span>



| <span data-ttu-id="c38a5-111">需求</span><span class="sxs-lookup"><span data-stu-id="c38a5-111">Requirement</span></span> | <span data-ttu-id="c38a5-112">值</span><span class="sxs-lookup"><span data-stu-id="c38a5-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c38a5-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c38a5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c38a5-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c38a5-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c38a5-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c38a5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c38a5-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c38a5-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c38a5-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c38a5-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="c38a5-118">**父元素**</span><span class="sxs-lookup"><span data-stu-id="c38a5-118">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="c38a5-119">**instrumentationManifest**</span><span class="sxs-lookup"><span data-stu-id="c38a5-119">**instrumentationManifest**</span></span>](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





