---
description: 應用程式會流覽 Windows 映像取得 (WIA) 裝置的專案樹狀結構，以尋找並選取該裝置上的影像。 應用程式會使用這項技術來選取並取得影像，而不會向使用者呈現對話方塊。
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: 流覽專案樹狀結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511616"
---
# <a name="navigating-an-item-tree"></a><span data-ttu-id="2a044-104">流覽專案樹狀結構</span><span class="sxs-lookup"><span data-stu-id="2a044-104">Navigating an Item Tree</span></span>

<span data-ttu-id="2a044-105">應用程式會流覽 Windows 映像取得 (WIA) 裝置的專案樹狀結構，以尋找並選取該裝置上的影像。</span><span class="sxs-lookup"><span data-stu-id="2a044-105">An application navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="2a044-106">應用程式會使用這項技術來選取並取得影像，而不會向使用者呈現對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2a044-106">Using this technique, an application selects and acquires an image without presenting a dialog box to the user.</span></span>

<span data-ttu-id="2a044-107">WIA 裝置會表示為 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 或 [**IWiaItem2**](-wia-iwiaitem2.md) 物件樹狀結構中的根專案。</span><span class="sxs-lookup"><span data-stu-id="2a044-107">A WIA device is represented as the root item in a tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="2a044-108">樹狀結構中的子專案代表掃描器的影像，或是掃描器的掃描張床。</span><span class="sxs-lookup"><span data-stu-id="2a044-108">The child items in the tree represent images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="2a044-109">選取 WIA 裝置之後，應用程式會呼叫裝置之 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)或 [**IWiaItem2**](-wia-iwiaitem2.md)介面的 [**IWiaItem：： EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems)方法，以列舉裝置 (影像或掃描張床) 的子專案。</span><span class="sxs-lookup"><span data-stu-id="2a044-109">After a WIA device is selected, an application calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method of the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface of the device to enumerate the child items (the images or scan beds) of the device.</span></span> <span data-ttu-id="2a044-110">如需相關指示，請參閱 [選取裝置](-wia-selecting-a-device.md)。</span><span class="sxs-lookup"><span data-stu-id="2a044-110">For instructions, see [Selecting a Device](-wia-selecting-a-device.md).</span></span>

<span data-ttu-id="2a044-111">[**IWiaItem：： EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems)方法會為裝置的子專案建立列舉物件，並傳回該物件之 [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2a044-111">The [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method creates an enumeration object for the child items of the device, and returns a pointer to that object's [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) interface.</span></span> <span data-ttu-id="2a044-112">然後，應用程式可以使用 **IEnumWiaItem** 介面的方法，取得裝置專案樹狀結構中專案的指標。</span><span class="sxs-lookup"><span data-stu-id="2a044-112">The application can then use the methods of the **IEnumWiaItem** interface to obtain pointers to the items in the device's item tree.</span></span>

 

 



