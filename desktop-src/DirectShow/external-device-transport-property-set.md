---
description: 外部裝置傳輸屬性集
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: 外部裝置傳輸屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909216"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="20ab8-103">外部裝置傳輸屬性集</span><span class="sxs-lookup"><span data-stu-id="20ab8-103">External Device Transport Property Set</span></span>

<span data-ttu-id="20ab8-104">這個屬性集會控制資料與外部裝置之間的傳輸。</span><span class="sxs-lookup"><span data-stu-id="20ab8-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="20ab8-105">在大部分情況下，應用程式不應該直接使用這個屬性集。</span><span class="sxs-lookup"><span data-stu-id="20ab8-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="20ab8-106">請改用 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) 介面。</span><span class="sxs-lookup"><span data-stu-id="20ab8-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="20ab8-107">下表列出與使用者模式應用程式相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="20ab8-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="20ab8-108">如需此屬性集的完整說明，請參閱 Microsoft Windows 驅動程式開發工具組 DDK。</span><span class="sxs-lookup"><span data-stu-id="20ab8-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



| <span data-ttu-id="20ab8-109">標籤</span><span class="sxs-lookup"><span data-stu-id="20ab8-109">Label</span></span> | <span data-ttu-id="20ab8-110">值</span><span class="sxs-lookup"><span data-stu-id="20ab8-110">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="20ab8-111">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="20ab8-111">Property Set GUID</span></span> | <span data-ttu-id="20ab8-112">PROPSETID \_ EXT \_ TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="20ab8-112">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="20ab8-113">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="20ab8-113">Property ID</span></span>                                                                           | <span data-ttu-id="20ab8-114">描述</span><span class="sxs-lookup"><span data-stu-id="20ab8-114">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="20ab8-115">**KSPROPERTY \_ EXTXPORT \_ ATN \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="20ab8-115">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="20ab8-116">搜尋 (ATN) 的絕對曲目編號。</span><span class="sxs-lookup"><span data-stu-id="20ab8-116">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="20ab8-117">**KSPROPERTY \_ EXTXPORT 時間 \_ 碼 \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="20ab8-117">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="20ab8-118">搜尋時間碼。</span><span class="sxs-lookup"><span data-stu-id="20ab8-118">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="20ab8-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="20ab8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20ab8-120">屬性集</span><span class="sxs-lookup"><span data-stu-id="20ab8-120">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



