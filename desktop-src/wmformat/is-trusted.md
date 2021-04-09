---
title: Is_Trusted
description: 是 \_ 受信任的屬性是檔案層級屬性，可指定檔案中的授權取得 URL 是否受信任。
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted windows Media 格式
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932762"
---
# <a name="is_trusted"></a><span data-ttu-id="8c940-104">\_受信任</span><span class="sxs-lookup"><span data-stu-id="8c940-104">Is\_Trusted</span></span>

<span data-ttu-id="8c940-105">**是 \_ 受信任** 的屬性是檔案層級屬性，可指定檔案中的授權取得 URL 是否受信任。</span><span class="sxs-lookup"><span data-stu-id="8c940-105">The **Is\_Trusted** attribute is a file-level attribute specifying whether the license acquisition URL in the file is trusted.</span></span>

## <a name="global-constant"></a><span data-ttu-id="8c940-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="8c940-106">Global Constant</span></span>

<span data-ttu-id="8c940-107">g \_ wszWMTrusted</span><span class="sxs-lookup"><span data-stu-id="8c940-107">g\_wszWMTrusted</span></span>

## <a name="data-type"></a><span data-ttu-id="8c940-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="8c940-108">Data Type</span></span>

<span data-ttu-id="8c940-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="8c940-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="8c940-110">備註</span><span class="sxs-lookup"><span data-stu-id="8c940-110">Remarks</span></span>

<span data-ttu-id="8c940-111">這是程式碼屬性。</span><span class="sxs-lookup"><span data-stu-id="8c940-111">This is a coded attribute.</span></span>

<span data-ttu-id="8c940-112">在流覽至包含在受 DRM 保護之檔案中的授權取得 URL 之前，應用程式應該先確認此屬性為 true。</span><span class="sxs-lookup"><span data-stu-id="8c940-112">Before navigating to a license acquisition URL contained in a DRM-protected file, an application should first verify that this property is true.</span></span> <span data-ttu-id="8c940-113">如果為 false，則應用程式應該通知使用者 URL 可能已遭篡改。</span><span class="sxs-lookup"><span data-stu-id="8c940-113">If it is false, the application should notify the user that the URL has possibly been tampered with.</span></span>

<span data-ttu-id="8c940-114">這個屬性不能在檔案層級複製。</span><span class="sxs-lookup"><span data-stu-id="8c940-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="8c940-115">如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。</span><span class="sxs-lookup"><span data-stu-id="8c940-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c940-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c940-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c940-117">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="8c940-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




