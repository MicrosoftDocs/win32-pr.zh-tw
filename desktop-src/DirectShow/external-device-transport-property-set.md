---
description: 外部裝置傳輸屬性集
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: 外部裝置傳輸屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109901"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="5392d-103">外部裝置傳輸屬性集</span><span class="sxs-lookup"><span data-stu-id="5392d-103">External Device Transport Property Set</span></span>

<span data-ttu-id="5392d-104">這個屬性集會控制資料與外部裝置之間的傳輸。</span><span class="sxs-lookup"><span data-stu-id="5392d-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="5392d-105">在大部分情況下，應用程式不應該直接使用這個屬性集。</span><span class="sxs-lookup"><span data-stu-id="5392d-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="5392d-106">請改用 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) 介面。</span><span class="sxs-lookup"><span data-stu-id="5392d-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="5392d-107">下表列出與使用者模式應用程式相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="5392d-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="5392d-108">如需此屬性集的完整說明，請參閱 Microsoft Windows 驅動程式開發工具組 DDK。</span><span class="sxs-lookup"><span data-stu-id="5392d-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="5392d-109">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="5392d-109">Property Set GUID</span></span> | <span data-ttu-id="5392d-110">PROPSETID \_ EXT \_ TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="5392d-110">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="5392d-111">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="5392d-111">Property ID</span></span>                                                                           | <span data-ttu-id="5392d-112">描述</span><span class="sxs-lookup"><span data-stu-id="5392d-112">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="5392d-113">**KSPROPERTY \_ EXTXPORT \_ ATN \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="5392d-113">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="5392d-114">搜尋 (ATN) 的絕對曲目編號。</span><span class="sxs-lookup"><span data-stu-id="5392d-114">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="5392d-115">**KSPROPERTY \_ EXTXPORT 時間 \_ 碼 \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="5392d-115">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="5392d-116">搜尋時間碼。</span><span class="sxs-lookup"><span data-stu-id="5392d-116">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="5392d-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="5392d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5392d-118">屬性集</span><span class="sxs-lookup"><span data-stu-id="5392d-118">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



