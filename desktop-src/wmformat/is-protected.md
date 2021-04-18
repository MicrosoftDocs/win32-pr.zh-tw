---
title: Is_Protected
description: '\_受保護的屬性是檔案層級屬性，用來指定是否使用數位版權管理 (DRM) 保護檔案中的內容。'
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected windows Media 格式
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ec24eb3e805f93bfd46e40954ce64da73ed774
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965004"
---
# <a name="is_protected"></a><span data-ttu-id="1ef0c-104">\_受保護</span><span class="sxs-lookup"><span data-stu-id="1ef0c-104">Is\_Protected</span></span>

<span data-ttu-id="1ef0c-105">**\_ 受保護** 的屬性是檔案層級屬性，用來指定是否使用數位版權管理 (DRM) 保護檔案中的內容。</span><span class="sxs-lookup"><span data-stu-id="1ef0c-105">The **Is\_Protected** attribute is a file-level attribute specifying whether the content in the file was protected using digital rights management (DRM).</span></span>

## <a name="global-constant"></a><span data-ttu-id="1ef0c-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="1ef0c-106">Global Constant</span></span>

<span data-ttu-id="1ef0c-107">g \_ wszWMProtected</span><span class="sxs-lookup"><span data-stu-id="1ef0c-107">g\_wszWMProtected</span></span>

## <a name="data-type"></a><span data-ttu-id="1ef0c-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="1ef0c-108">Data Type</span></span>

<span data-ttu-id="1ef0c-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="1ef0c-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="1ef0c-110">備註</span><span class="sxs-lookup"><span data-stu-id="1ef0c-110">Remarks</span></span>

<span data-ttu-id="1ef0c-111">這是程式碼屬性。</span><span class="sxs-lookup"><span data-stu-id="1ef0c-111">This is a coded attribute.</span></span> <span data-ttu-id="1ef0c-112">抓取此屬性會提供與呼叫 [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="1ef0c-112">Retrieving this property provides the same information as calling [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected).</span></span>

<span data-ttu-id="1ef0c-113">這個屬性不能在檔案層級複製。</span><span class="sxs-lookup"><span data-stu-id="1ef0c-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="1ef0c-114">如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。</span><span class="sxs-lookup"><span data-stu-id="1ef0c-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ef0c-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ef0c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef0c-116">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="1ef0c-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




