---
title: DRM_Flags
description: '[DRM \_ 旗標] 屬性僅適用于 drm 第1版內容，以指定將包含在本機授權中的許可權。'
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags windows Media 格式
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932927"
---
# <a name="drm_flags"></a><span data-ttu-id="c211f-104">DRM \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="c211f-104">DRM\_Flags</span></span>

<span data-ttu-id="c211f-105">[ **Drm \_ 旗標** ] 屬性僅適用于 drm 第1版內容，以指定將包含在本機授權中的許可權。</span><span class="sxs-lookup"><span data-stu-id="c211f-105">The **DRM\_Flags** property is used with DRM version 1 content only to specify the rights that will be contained in the local license.</span></span> <span data-ttu-id="c211f-106">許可權是使用 **WMT \_ 許可權** 列舉類型所定義的值來指定。</span><span class="sxs-lookup"><span data-stu-id="c211f-106">Rights are specified with values defined by the **WMT\_RIGHTS** enumeration type.</span></span> <span data-ttu-id="c211f-107">藉由將一個以上的值與位 **or** 運算子結合，即可選取多個值。</span><span class="sxs-lookup"><span data-stu-id="c211f-107">More than one value can be selected by combining them with the bitwise **OR** operator.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c211f-108">全域常數</span><span class="sxs-lookup"><span data-stu-id="c211f-108">Global Constant</span></span>

<span data-ttu-id="c211f-109">g \_ wszWMDRM \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="c211f-109">g\_wszWMDRM\_Flags</span></span>

## <a name="data-type"></a><span data-ttu-id="c211f-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="c211f-110">Data Type</span></span>

<span data-ttu-id="c211f-111">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c211f-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="c211f-112">備註</span><span class="sxs-lookup"><span data-stu-id="c211f-112">Remarks</span></span>

<span data-ttu-id="c211f-113">存取寫入器物件的 **IWMHeaderInfo3** 介面時，您可以加入或變更此值。</span><span class="sxs-lookup"><span data-stu-id="c211f-113">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="c211f-114">在其他物件 (中繼資料編輯器、讀取器和同步讀取器) ，此值是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c211f-114">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span> <span data-ttu-id="c211f-115">建立 DRM 第1版內容時，請使用 [**IWMHeaderInfo：： SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) 來設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="c211f-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when creating DRM version 1 content.</span></span>

## <a name="see-also"></a><span data-ttu-id="c211f-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c211f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c211f-117">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="c211f-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




