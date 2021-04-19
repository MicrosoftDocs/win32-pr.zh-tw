---
description: 指定本機外掛程式控制原則。
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: 'MF_LOCAL_PLUGIN_CONTROL_POLICY 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999952"
---
# <a name="mf_local_plugin_control_policy-attribute"></a><span data-ttu-id="7bf17-103">MF \_ 本機 \_ 外掛程式 \_ 控制 \_ 原則屬性</span><span class="sxs-lookup"><span data-stu-id="7bf17-103">MF\_LOCAL\_PLUGIN\_CONTROL\_POLICY attribute</span></span>

<span data-ttu-id="7bf17-104">指定本機外掛程式控制原則。</span><span class="sxs-lookup"><span data-stu-id="7bf17-104">Specifies a local plugin control policy.</span></span>

## <a name="data-type"></a><span data-ttu-id="7bf17-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7bf17-105">Data type</span></span>

<span data-ttu-id="7bf17-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7bf17-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7bf17-107">備註</span><span class="sxs-lookup"><span data-stu-id="7bf17-107">Remarks</span></span>

<span data-ttu-id="7bf17-108">將此屬性設定為其中一個 [**MF \_ 外掛程式 \_ 控制 \_ 原則**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) 值。</span><span class="sxs-lookup"><span data-stu-id="7bf17-108">Set this attribute to one of the [**MF\_PLUGIN\_CONTROL\_POLICY**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) values.</span></span>

<span data-ttu-id="7bf17-109">此屬性可讓應用程式指定比 [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)所設定的整個進程原則更嚴格的本機原則。</span><span class="sxs-lookup"><span data-stu-id="7bf17-109">This attributes allows the app to specify a more restrictive local policy than the process-wide policy configured by [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf17-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bf17-110">Requirements</span></span>



| <span data-ttu-id="7bf17-111">需求</span><span class="sxs-lookup"><span data-stu-id="7bf17-111">Requirement</span></span> | <span data-ttu-id="7bf17-112">值</span><span class="sxs-lookup"><span data-stu-id="7bf17-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf17-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7bf17-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf17-114">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7bf17-114">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7bf17-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7bf17-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf17-116">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7bf17-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7bf17-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7bf17-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bf17-118"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7bf17-118"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf17-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7bf17-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf17-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7bf17-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7bf17-121">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="7bf17-121">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




