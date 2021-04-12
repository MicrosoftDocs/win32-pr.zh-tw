---
description: 指定應用程式是否需要來源讀取器或接收寫入器中的 Microsoft Direct3D 支援。
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: 'MF_READWRITE_D3D_OPTIONAL 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194983"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a><span data-ttu-id="3654a-103">MF \_ READWRITE \_ D3D \_ 選用屬性</span><span class="sxs-lookup"><span data-stu-id="3654a-103">MF\_READWRITE\_D3D\_OPTIONAL attribute</span></span>

<span data-ttu-id="3654a-104">指定應用程式是否需要 [來源讀取](source-reader.md) 器或 [接收寫入器](sink-writer.md)中的 Microsoft Direct3D 支援。</span><span class="sxs-lookup"><span data-stu-id="3654a-104">Specifies whether the application requires Microsoft Direct3D support in the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="3654a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3654a-105">Data type</span></span>

<span data-ttu-id="3654a-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3654a-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3654a-107">備註</span><span class="sxs-lookup"><span data-stu-id="3654a-107">Remarks</span></span>

<span data-ttu-id="3654a-108">只有當應用程式使用 [mf \_ 來源 \_ 讀取器 \_ d3d \_ 管理員](mf-source-reader-d3d-manager.md) 或 [mf \_ 接收 \_ 寫入器 \_ d3d \_ 管理員](mf-sink-writer-d3d-manager.md) 屬性啟用 Direct3D 支援時，才適用此屬性。</span><span class="sxs-lookup"><span data-stu-id="3654a-108">This attribute applies only if the application enables Direct3D support using the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) or [MF\_SINK\_WRITER\_D3D\_MANAGER](mf-sink-writer-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="3654a-109">如果應用程式啟用 Direct3D 支援，來源讀取器和接收寫入器都會嘗試配置適用于影片的 Direct3D 表面。</span><span class="sxs-lookup"><span data-stu-id="3654a-109">If the application enables Direct3D support, the Source Reader and Sink Writer will both try to allocate Direct3D surfaces for video.</span></span> <span data-ttu-id="3654a-110">如果失敗，而 MF \_ READWRITE \_ D3D \_ 選擇性屬性為 **TRUE**，則來源讀取器/接收寫入器會切換回配置系統記憶體中的影片表面。</span><span class="sxs-lookup"><span data-stu-id="3654a-110">If this fails, and the MF\_READWRITE\_D3D\_OPTIONAL attribute is **TRUE**, the Source Reader/Sink Writer will fall back to allocating video surfaces in system memory.</span></span> <span data-ttu-id="3654a-111">否則，如果無法配置 Direct3D 介面，且 MF \_ READWRITE \_ D3D \_ 選用為 **FALSE**，則在處理期間會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3654a-111">Otherwise, if Direct3D surfaces cannot be allocated and MF\_READWRITE\_D3D\_OPTIONAL is **FALSE**, an error occurs during processing.</span></span>

<span data-ttu-id="3654a-112">如果應用程式沒有啟用 Direct3D 支援，來源讀取器/接收寫入器會使用系統記憶體，並忽略 MF \_ READWRITE \_ D3D 選擇性的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3654a-112">If the application does not enable Direct3D support, the Source Reader/Sink Writer uses system memory, and ignores the value of MF\_READWRITE\_D3D\_OPTIONAL.</span></span>

<span data-ttu-id="3654a-113">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="3654a-113">This attribute is optional.</span></span> <span data-ttu-id="3654a-114">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3654a-114">The default value is **FALSE**.</span></span> <span data-ttu-id="3654a-115">當您建立來源讀取器或接收寫入器時，請設定屬性。</span><span class="sxs-lookup"><span data-stu-id="3654a-115">Set the attribute when you create the Source Reader or Sink Writer.</span></span>

## <a name="requirements"></a><span data-ttu-id="3654a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3654a-116">Requirements</span></span>



| <span data-ttu-id="3654a-117">需求</span><span class="sxs-lookup"><span data-stu-id="3654a-117">Requirement</span></span> | <span data-ttu-id="3654a-118">值</span><span class="sxs-lookup"><span data-stu-id="3654a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3654a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3654a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3654a-120">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3654a-120">Windows 8 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3654a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3654a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3654a-122">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3654a-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3654a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3654a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3654a-124"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="3654a-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3654a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3654a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3654a-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3654a-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3654a-127">接收寫入器屬性</span><span class="sxs-lookup"><span data-stu-id="3654a-127">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="3654a-128">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="3654a-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




